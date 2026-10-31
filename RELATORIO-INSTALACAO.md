# Relatório de instalação — TCL Smart TV Pro (Android 12 / Google TV)

> Registro de uma instalação real do Free My TV em uma TCL Brasil, feita seguindo o
> [CLAUDE.md](CLAUDE.md). Dados pessoais anonimizados: IPs (`192.168.x.x`), SSIDs
> (`Rede*`), coordenadas aproximadas e nenhuma chave incluída. O TV model é citado
> porque é o objetivo deste relatório.

## TV testada

| Campo | Valor |
|---|---|
| Marca / modelo | TCL **Smart TV Pro** (vendida no Brasil) |
| Sistema | Google TV, **Android 12** |
| Conexão usada | ADB pela rede (TCP 5555), Wi‑Fi 5 GHz |
| Launcher nativo | `com.google.android.apps.tv.launcherx` (Google TV) |
| Setup app | `com.google.android.tungsten.setupwraith` |
| Screensaver nativo | `com.google.android.apps.tv.dreamx/.service.Backdrop` |

## O que foi feito (resumo)

1. **Build no Linux (AlmaLinux 10)** sem Gradle, com `./build.sh`:
   - JDK **17** (Temurin) — ver dificuldade 1 abaixo sobre o Java 21;
   - Android SDK command‑line tools + `build-tools;34.0.0` + `platforms;android-34`;
   - `config.properties`: cidade do Sudeste do Brasil (coords aproximadas
     `-23.55, -46.63`), `tmdb_region=BR`, `currency=BRL`, chave TMDB do dono da TV
     (colada por ele mesmo no arquivo; nunca em chat nem no APK).
2. **Instalação**: `adb connect 192.168.x.x:5555` → `adb install -r FreeMyTV.apk`.
3. **Passo obrigatório TCL** — liberar o auto‑start (o `TclAppBoot` da TCL bloqueia
   jobs em segundo plano e a troca nunca rodaria):
   ```bash
   adb shell "appops set io.freemytv AUTO_START allow || appops set io.freemytv APP_AUTO_START allow"
   ```
   Nesta TV, o nome aceito foi `APP_AUTO_START` (`AUTO_START` respondeu
   `Unknown operation string` — normal, o comando tenta os dois).
4. **Troca de modo feita na própria TV** (nunca pelo computador):
   *Free My TV* → *Home Screen* → *Free My TV*, autorizando a depuração interna
   quando pedida. Resultado confirmado por `adb logcat -s FreeMyTV` e por
   `cmd package query-activities` (a `HOME` virou `io.freemytv/.HomeActivity`).

## Dificuldades encontradas e como resolver

### 1. `d8` quebra com Java 21 (`NullPointerException` no R8/D8)
- **Sintoma:** o build morre no passo dex com um stack trace do R8
  (`Cannot invoke "String.length()" because "<parameter1>" is null`).
- **Causa:** o `d8` do build-tools 34 tem um bug com JDKs ≥ 21; o projeto pede JDK 17.
- **Solução:** JDK 17 do Adoptium na home do usuário, sem root:
  ```bash
  curl -L -o jdk17.tar.gz "https://api.adoptium.net/v3/binary/latest/17/ga/linux/x64/jdk/hotspot/normal/eclipse"
  mkdir -p ~/jdk17 && tar -xzf jdk17.tar.gz -C ~/jdk17 --strip-components=1 && rm jdk17.tar.gz
  cd ~/free-my-tv && ANDROID_HOME=~/android-sdk JAVA_HOME=~/jdk17 ./build.sh
  ```

### 2. A troca para no Wi‑Fi: "a configuração inicial da TV salvou o Wi‑Fi"
- **Sintoma:** ao trocar de modo, o app recusa e avisa que desligar o setup apagaria
  redes Wi‑Fi salvas.
- **Causa:** o `setupwraith` (app de configuração inicial do Google TV) é o *dono*
  do registro de algumas redes salvas. Como ele precisa ser desligado na troca,
  o Android apagaria essas redes — o Free My TV se recusa a fazer isso de propósito.
- **Diagnóstico:** procurar `cname=com.google.android.tungsten.setupwraith` no
  `adb shell dumpsys wifi` (cada bloco de rede começa com o `ID:` dele).
- **Solução nesta TV:** apagar pelo computador as redes com esse dono (as fora de
  alcance não aparecem nas Configurações da TV):
  ```bash
  adb shell cmd wifi forget-network <ID>
  ```
  Foram apagadas a rede 5 GHz oculta (ID 1) e a rede em uso (ID 6) — a TV caiu do
  Wi‑Fi, foi reconectada pelas Configurações da TV digitando a senha, e a rede nova
  ficou salva apenas por `com.android.tv.settings` (dono que **não** é desligado).
  Depois disso a troca passou de primeira. **Detalhe importante:** esquecer e
  reconectar só pelas Configurações da TV **não resolveu** — o Android reaproveitou
  o registro antigo com o `setupwraith` como dono; foi preciso o `forget-network`
  via ADB.

### 3. Porta 5555 fechada mesmo com "modo desenvolvedor" ligado
- **Causa:** estar em modo desenvolvedor não liga o ADB de rede.
- **Solução:** em *Opções do desenvolvedor*, ligar **Depuração USB** (abre o 5555
  na rede). A TV pede autorização do computador na primeira conexão.

### 4. Sem `unzip`/`nc`/`ping` no sistema mínimo (AlmaLinux)
- **Solução:** `python3 -m zipfile -e` no lugar do `unzip`, teste de porta com um
  mini script `python3` (socket) no lugar do `nc`, e `adb devices` no lugar do ping.

## Estado final verificado

- `HOME` → `io.freemytv/.HomeActivity` (Free My TV ativo).
- `launcherx`, `setupwraith` e os apps promocionais da TCL: **desativados**
  (`pm disable-user`, nunca desinstalados).
- Screensaver → `io.freemytv/io.freemytv.ScreensaverAlone`.
- Wi‑Fi reconectado e estável; `APP_AUTO_START: allow` persiste para o
  Free My TV (troca e watchdog sobrevivem a reinícios).

## Como voltar atrás

App **Free My TV** na TV → *Home Screen* → **Original** (restaura launcher,
screensaver e reativa os apps desativados). Se o app for desinstalado sem voltar
antes, restaurar pelo computador:

```bash
adb shell pm enable <pacote>          # launcher e apps da lista DEBLOAT
adb shell cmd package set-home-activity com.google.android.apps.tv.launcherx/.home.HomeActivity
adb shell settings put secure screensaver_components com.google.android.apps.tv.dreamx/.service.Backdrop
```

## Lições para a próxima instalação

1. Instalar o **JDK 17** desde o início (evita o bug do `d8`).
2. Já verificar os *donos* das redes Wi‑Fi (`dumpsys wifi`) **antes** de tentar a
   troca e limpar o que pertence ao `setupwraith`.
3. Em TCL, rodar o `appops` de auto‑start **sempre** depois de cada
   `adb install` (uma desinstalação devolve o padrão bloqueado).
4. Guardar o `freemytv.keystore` gerado no primeiro build: atualizações só
   instalam com a mesma assinatura.
