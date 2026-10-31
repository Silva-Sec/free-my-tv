> 🇺🇸 This page in English: [README.en.md](README.en.md)

<div align="center">

<img src="docs/assets/icon-512.png" width="96" alt="">

# Free My TV

**Uma tela inicial rápida e sem anúncios para TVs Google TV, LG e Samsung.**

Recomendações em alta dos seus próprios apps, o tempo na hora, e um visual que acompanha o pôr do sol.<br>
Código aberto. Feito com Claude Code. Um botão para desfazer.

[**freemytv.io**](https://freemytv.io) · [Instalação](#instalação) · [TVs LG](#tvs-lg-webos) · [TVs Samsung](#tvs-samsung-tizen) · [Qualquer TV](#qualquer-tv) · [Deixe com a sua cara](#deixe-com-a-sua-cara)

<img src=".github/preview.webp" width="880" alt="A tela inicial do Free My TV: uma prateleira de vidro com apps, recomendações em alta e uma gaveta com o tempo e os preços das criptos">

</div>

## O que você ganha

- **Sem anúncios.** Nenhuma linha patrocinada, banner ou promoção com reprodução automática. Nem um.
- **Seus apps, em primeiro plano.** Os apps de streaming que você realmente usa, numa prateleira de vidro. Escolha quais e em que ordem na própria TV.
- **Em alta, não patrocinado.** Três recomendações novas a cada hora (até seis, em Ajustes da Tela Inicial) entre o que está em alta na semana e os lançamentos, só de apps que você já tem, e dos serviços que você escolher. A selecionada abre em destaque e as outras mostram seus pôsteres. Filmes e Séries têm abas próprias, e na Google TV a sua [biblioteca Plex](#sua-biblioteca-plex-opcional) pode entrar junto.
- **Continuar Assistindo** (Google TV e Android TV). *Ajustes da Tela Inicial* → *Topo da tela* põe o que você deixou pela metade nos seus apps no topo, com o progresso, e o OK continua no app. Ou um grande relógio, ou as recomendações.
- **Sua chave do TMDB pelo celular.** *Ajustes da Tela Inicial* → *Chave TMDB* mostra um QR code: escaneie e cole a chave. Na LG e Samsung, digite com o controle.
- **Tempo e mercados, a um toque.** A previsão hora a hora (ou os próximos 5 dias), nascer e pôr do sol, e preços de criptomoedas ao vivo.
- **O que está tocando.** Música, podcast ou rádio rodando em segundo plano aparece na tela inicial e no protetor de tela: título, artista e app, de qualquer app que informa ao Android o que toca (*Ajustes da Tela Inicial*, desligado até você ativar).
- **O status num relance, e mouse** (Google TV e Android TV). *Ajustes da Tela Inicial* → *Ícones de status* põe Wi‑Fi ou Ethernet, áudio Bluetooth e um drive USB no topo da tela inicial; desligado, nada fica escutando por eles. Um mouse ou controle air-mouse também funciona: o hover move o foco, a roda rola a tela, o clique seleciona.
- **Claro de dia, escuro à noite.** Segue o pôr do sol real da sua cidade, como no seu celular.
- **Um protetor de tela à altura.** Fotos em tela cheia das recomendações com um grande relógio de vidro. Na LG e Samsung, *Ajustes da Tela Inicial* → *Protetor de tela* pode torná-lo um grande relógio com o tempo, deslizando devagar para não queimar a tela OLED. Opcionalmente (*Assistir do protetor de tela*, nos Ajustes da Tela Inicial), o OK abre o título na tela, no app dele, e qualquer outro botão só fecha.
- **Escurecimento para sala escura** (LG e Samsung). *Ajustes da Tela Inicial* → *Escurecer* escurece as telas do próprio Free My TV, não os apps que você abre: baixo, médio, alto, ou automático (médio das 22:00 às 07:00). Desligado até você escolher.
- **Suas próprias fotos** (Google TV e Android TV). Envie do seu computador (até 100): o protetor de tela as mostra, e sem recomendações uma delas é o fundo da tela inicial a cada hora.
- **Rápido.** 60 fps, cada quadro em 16,6 ms, no chip da própria TV. A tela inicial usa 96 MB de memória em vez de 242 MB (−60%).<br><sub>Medido em uma TCL Google TV de 98″ rodando Android 14.</sub>
- **Configurável na TV.** Idioma, sua cidade, temperatura, tema, quantas recomendações e de quais serviços de streaming elas vêm, os cartões de tempo e preços, a previsão em horas ou dias, quais moedas e os apps da prateleira, nos ajustes do próprio Free My TV.
- **Seguro.** Sem root. Nada é desinstalado. Um botão traz de volta a tela inicial de fábrica.

## Instalação

Cerca de dez minutos. Você precisa de uma Google TV ou Android TV (Android 8 ou mais novo) e um computador no mesmo Wi‑Fi. O APK vai na TV, não no celular (no celular, os ajustes avisam e nada troca).

### O caminho fácil: um assistente de IA

1. **Na TV**, ligue o modo desenvolvedor: Configurações → Sistema → Sobre → pressione *Android TV OS build* 7 vezes. Depois Configurações → Sistema → Opções do desenvolvedor → ligue a **Depuração USB**. Anote o endereço IP da TV (Configurações → Rede e Internet).
2. **No computador**, abra um assistente de codificação por IA ([Claude Code](https://claude.com/claude-code), Codex ou Antigravity) e diga:
   > Instale o Free My TV (github.com/simbasjungles/free-my-tv) na minha TV em 192.168.1.50. Eu moro em Lisboa.

   Ele baixa o código, instala as ferramentas necessárias, compila o app e põe na sua TV, e pergunta antes de qualquer coisa importante. Troque pelo IP da sua TV e pela sua cidade.
3. **Na TV**, abra *Free My TV* → *Tela Inicial* → *Free My TV*. É quando a TV pergunta *Permitir depuração USB?* para o Free My TV: marque *Sempre permitir* e aceite.

### O APK pronto

Nenhuma ferramenta para instalar além do adb. O APK da [última release](https://github.com/simbasjungles/free-my-tv/releases/latest) não tem chave TMDB: adicione a sua na TV para ter as recomendações (*Ajustes da Tela Inicial* → *Chave TMDB*, [abaixo](#a-chave-do-tmdb)). Ele tira a sua cidade do fuso horário da TV (mude em *Ajustes da Tela Inicial* → *Cidade*).

Se você já compilou o Free My TV você mesmo antes, volte para o *Original* e desinstale primeiro: o seu build e a release são assinados com chaves diferentes.

1. **Na TV**, faça o passo 1 acima.
2. **No computador**, baixe o `FreeMyTV.apk` da release e instale:
   ```bash
   adb connect 192.168.1.50:5555
   adb install -r FreeMyTV.apk
   ```
   No Android 14, o Google Play Protect pode travar a instalação com *App arriscado bloqueado*: escolha *Mais detalhes* → *Instalar mesmo assim*.

   Instale pelo adb assim, não abrindo o APK na TV: de um gerenciador de arquivos ou navegador, o Play Protect pode recusar de vez com *App bloqueado para proteger seu dispositivo* (em alguns países ele bloqueia apps instalados por fora que têm um serviço de acessibilidade ou um listener de notificações, que o Free My TV usa para os botões do controle e o Tocando Agora; #378).

   Em TVs TCL, deixe também o app rodar em segundo plano (a TCL bloqueia por padrão, e a troca nunca começa). Uma desinstalação devolve a permissão, então rode de novo após cada nova instalação:
   ```bash
   adb shell "appops set io.freemytv AUTO_START allow || appops set io.freemytv APP_AUTO_START allow"
   ```
3. **Na TV**, faça o passo 3 acima.

Para as recomendações, adicione sua chave TMDB em *Ajustes da Tela Inicial* → *Chave TMDB* (abaixo).

**As atualizações chegam na TV.** Uma vez por semana o APK da release procura por uma release mais nova e baixa; a tela inicial avisa uma vez, e *Ajustes da Tela Inicial* → *Atualizações* (a última linha) instala pelo instalador do Android, que pergunta antes (e, na primeira vez, pede para permitir que o Free My TV instale apps). O OK em *Atualizações* também verifica na hora. O download precisa virar das releases deste repositório, bater com o tamanho e o SHA-256 que o GitHub lista, ser mais novo e estar assinado com a chave do projeto. Um build feito por você só verifica quando você aperta *Atualizações*, e só avisa quando sai versão nova: compile de novo para atualizar.

### O caminho manual

1. **Na TV**, faça o passo 1 acima.
2. **Ferramentas:** um JDK (17+), as ferramentas de linha de comando do SDK do Android (build-tools 34, platform android-34) e o adb. No Mac:
   ```bash
   brew install --cask temurin android-commandlinetools android-platform-tools
   sdkmanager "build-tools;34.0.0" "platforms;android-34"
   ```
   No Linux, pegue o OpenJDK 17, as ferramentas de linha de comando do Android e o adb no gerenciador de pacotes, e rode a mesma linha do `sdkmanager`. No Windows, use o Git Bash (que o Claude Code usa lá) ou o WSL.
3. **Compile:**
   ```bash
   ./build.sh
   ```
   A primeira execução cria o `config.properties`. Ponha sua cidade e sua [chave TMDB](#a-chave-do-tmdb) lá, e rode de novo.
4. **Instale:**
   ```bash
   adb connect 192.168.1.50:5555
   adb install -r FreeMyTV.apk
   ```
   Se a instalação parecer travada, olhe a TV: no Android 14, o Google Play Protect pode segurá-la com *App arriscado bloqueado* ("feito para uma versão mais antiga do Android"), já que o Free My TV mira o Android 13. Escolha *Mais detalhes* → *Instalar mesmo assim*. Atualizações não perguntam de novo.

   O Chromecast com Google TV no Android 14 mantém a porta 5555 fechada mesmo com a depuração USB ligada: ligue a *Depuração por Wi-Fi* (Opções do desenvolvedor), pareie com `adb pair <endereço:porta> <código>`, e rode `adb tcpip 5555` por essa conexão. A porta 5555 fecha de novo a cada reinício, então depois de um, o *Original*, o watchdog e a checagem de boot não alcançam o ADB até você rodar `adb tcpip 5555` de novo (o pareamento fica).

   Em TVs TCL, deixe também o app rodar em segundo plano (a TCL bloqueia por padrão, e a troca nunca começa). Uma desinstalação devolve a permissão, então rode de novo após cada nova instalação:
   ```bash
   adb shell "appops set io.freemytv AUTO_START allow || appops set io.freemytv APP_AUTO_START allow"
   ```
5. **Na TV**, abra *Free My TV* → *Tela Inicial* → *Free My TV*. A TV pergunta *Permitir depuração USB?* mais uma vez, agora para o próprio Free My TV: marque *Sempre permitir* e aceite. (Rode `adb disconnect 192.168.1.50:5555` antes: no Android 8 a 10 a TV pode entregar essa resposta a um computador ainda conectado.)

   Em algumas TVs TCL (Android 11, Realtek), um segundo matador de segundo plano, o TGuard, pode parar a troca enquanto ela mede a tela original: a tela de ajustes fecha e a tela inicial da TV fica. O Android roda a troca de novo sozinho em um ou dois minutos; depois aperte Home: o Free My TV abrindo significa que deu certo.

## TVs LG (webOS)

A mesma tela inicial como um app da LG: as recomendações, a prateleira de vidro com seus apps, a gaveta com entradas, tempo e preços, dia e noite, Ajustes da Tela Inicial e o editor da prateleira. Instala pelo modo Developer Mode da própria LG, sem root e sem mudar nada na TV. A tela inicial da LG fica onde está, e o Free My TV está a um toque de uma tecla de número (ou na lista de apps da LG, em controles sem elas).

Você precisa de uma TV LG (webOS 3 ou mais nova) e um computador no mesmo Wi‑Fi, com Python 3.

1. **Na TV**, abra a LG Content Store e instale o **Developer Mode**. Entre com uma [conta de desenvolvedor LG](https://webostv.developer.lge.com) gratuita, ligue o **Dev Mode Status** (a TV reinicia) e depois ligue o **Key Server**. Anote o endereço IP e a passphrase que aparecerem.
2. **No computador**, pegue o código e compile. O `config.properties` funciona como na Google TV (sua cidade, sua [chave TMDB](#a-chave-do-tmdb)):
   ```bash
   git clone https://github.com/simbasjungles/free-my-tv && cd free-my-tv
   python3 webos/build.py
   ```
3. **Instale.** Na primeira vez, ele pede a passphrase da TV; atualizações não. Numa TV que não é 4K, ele põe o app em 1280 × 720, o tamanho em que essas TVs desenham apps:
   ```bash
   python3 webos/install.py 192.168.1.50
   ```
4. **Na TV**, com o Free My TV aberto, segure uma tecla de número no controle. Daí em diante, essa tecla o abre de qualquer lugar. Num controle sem teclas de número, abra pela lista de apps da LG na tela inicial, como qualquer outro app.

Com um assistente de IA, diga *"Instale o Free My TV (github.com/simbasjungles/free-my-tv) na minha TV LG em 192.168.1.50. Eu moro em Lisboa."* Ele compila o app e te passa o comando de instalação, e a passphrase você mesmo digita.

Com o [webOS Homebrew Channel](https://github.com/webosbrew/webos-homebrew-channel), dá para dispensar o computador: adicione o repositório `https://freemytv.io/webos/apps.json` nas configurações do Channel, e o Free My TV aparece na lista. Esse é o build da release: ele tira a cidade do fuso horário da TV (mude em *Ajustes da Tela Inicial* → *Cidade*), e para as recomendações você digita sua [chave TMDB](#a-chave-do-tmdb) em *Ajustes da Tela Inicial* → *Chave TMDB*. Se você instalou o seu próprio build, não o atualize por lá, ou a release o substitui. Em algumas TVs LG que não são 4K, esse build preenche só a parte de cima à esquerda da tela: o `install.py` o instala no tamanho certo nelas.

Na webOS 6 e mais novas, a LG não deixa apps instalados pelo Developer Mode verem quais apps a TV tem. O Free My TV então mostra os conhecidos que ele encontra (Netflix, YouTube, Prime Video, Disney+, Apple TV, Plex e outros) e pergunta a TV, uma vez, pelo acesso que o app de celular da LG usa: uma mensagem na TV pergunta se permite o Free My TV. Permita, e do próximo início todos os seus apps aparecem, com seus ícones.

TVs LG mais antigas (webOS 3) não deixam o Free My TV ver seus apps de jeito nenhum, e a prateleira fica vazia. Aí o computador pergunta à TV no lugar do app (a TV pergunta uma vez se permite), e a lista e os ícones vão embutidos no app. Rode de novo depois de instalar apps novos na TV:
```bash
python3 webos/apps.py 192.168.1.50 && python3 webos/build.py && python3 webos/install.py 192.168.1.50
```

O Developer Mode dura cerca de 40 dias: abra o app Developer Mode de vez em quando e aperte **EXTEND**. Para remover o Free My TV, rode `python3 webos/install.py 192.168.1.50 --uninstall`.

## TVs Samsung (Tizen)

A mesma tela inicial como um app da Samsung, com tudo o que a da LG tem: as recomendações, a prateleira, a gaveta com as entradas, o tempo e os preços, dia e noite, e os ajustes próprios. Instala pelo modo Developer Mode da própria Samsung, sem root e sem mudar nada na TV, e a tela inicial da Samsung fica onde está.

Você precisa de uma TV Samsung com Tizen, de 2015 ou mais nova, e um computador no mesmo Wi‑Fi (uma UE48JU6100 de 2015 no Tizen 2.3 foi reportada funcionando, #317, enquanto uma UE49K5670 Full HD de 2016 recusa instalações de desenvolvedor por completo, com `failed[118]` até do `tizen install` da própria Samsung, #349: numa UE49KU6640 e numa UN49KU6400 a mesma resposta foi uma cópia deixada por uma instalação anterior que falhou, que `python3 tizen/install.py <IP> --uninstall` removeu (assine com um certificado Tizen lá: um da Samsung continuava dando o erro na KU6400); modelos Orsay não rodam, mas um streamer Google TV no HDMI roda). TVs de 2015 e 2016 não rodam o TizenBrew, então nelas compile você mesmo (abaixo); os Ajustes da TV não ficam na gaveta nelas, já que apps não conseguem abrir os ajustes da TV, nem nas TVs de 2017 e 2018 (Tizen 3 e 4), que travam tentando (#257); o botão Settings do próprio controle funciona em todas.

1. **Na TV**, abra **Apps** e digite `1 2 3 4 5` no controle. Ligue o **Developer mode**, digite o IP do seu computador em **Host PC IP** e reinicie a TV.
2. **No computador**, baixe o [TizenBrew Installer](https://github.com/reisxd/TizenBrewInstaller/releases/latest), o instalador da comunidade para TVs Samsung, abra-o e conecte à sua TV.
3. **Instale do GitHub:** digite `simbasjungles/free-my-tv`. Em TVs de 2023 e mais novas ele pede para entrar na sua conta Samsung uma vez, para assinar o app para a sua TV.
4. **Direto ao ponto:** nos ajustes da TV, em Start Screen Options, ligue o **Autorun Last App**: a TV liga já no Free My TV (testado numa TV de 2017; TVs de 2019 e 2020 não o reabrem, #356). Aí, mova o Free My TV para o primeiro lugar da barra Home, para ficar a um toque.

Esse build tira a sua cidade do fuso horário da TV (mude em *Ajustes da Tela Inicial* → *Cidade*), e para as recomendações você digita sua [chave TMDB](#a-chave-do-tmdb) em *Ajustes da Tela Inicial* → *Chave TMDB*. Para compilá-lo com o seu próprio `config.properties`, abra a pasta no Claude Code e diga *"Instale o Free My TV na minha TV Samsung em 192.168.1.50. Eu moro em Lisboa."* Ele configura as ferramentas da Samsung e, em TVs de 2023 e mais novas, você entra na sua conta Samsung no navegador para criar o certificado. O seu build assinado instala com `python3 tizen/install.py 192.168.1.50`, que só precisa de Python: sem Tizen Studio, e sem Rosetta em Macs Apple Silicon.

## Configurações

Os valores iniciais vêm do `config.properties`, criado pelo primeiro build (Google TV, LG e Samsung usam o mesmo arquivo). A maioria também pode ser mudada na TV, em *Free My TV* → *Ajustes da Tela Inicial*, e a escolha feita na TV vence:

| Chave | O que faz | Padrão |
|---|---|---|
| `tmdb_key` | Sua chave gratuita do TMDB, para as recomendações | vazia |
| `tmdb_region` | Seu país (duas letras): quais títulos estão em qual app | `US` |
| `watchmode_key` | Opcional, chave gratuita do [Watchmode](https://api.watchmode.com/): uma recomendação abre a página do título no app dele. Na Google TV e Android TV você também pode enviá-la do celular | vazia |
| `plex_url` e `plex_token` | Opcional, o endereço `plex.direct` e o token do seu servidor Plex: os títulos mais novos dele entram nas recomendações e abrem na página deles | vazia |
| `trakt_client_id` | Opcional: o Client ID do seu próprio app gratuito de API do [Trakt](https://trakt.tv/oauth/applications). Ajustes da Tela Inicial > Recomendações ganha então uma linha Trakt para entrar com um código, e as recomendações começam com o que você está no meio, trazem sua watchlist e deixam de fora o que você já assistiu. Só na Google TV | vazia |
| `home_assistant_url`, `home_assistant_entities` | Opcional: botões para o seu [Home Assistant](#botões-do-home-assistant-opcional) na gaveta de baixo (só na Google TV; o token vai do computador, nunca aqui) | vazia |
| `latitude`, `longitude` | Sua cidade, para o tempo e o pôr do sol | Nova York |
| `city` | O nome no cartão do tempo | `Weather` |
| `hide_animation` | Deixa desenhos e animes fora das recomendações; *Desenhos e animes* nos Ajustes da Tela Inicial (em *Recomendações* na Google TV) muda isso na TV | `false` |
| `open_in_stremio` | Uma recomendação abre na página do título no [Stremio](https://www.stremio.com/), quando o app Stremio está na TV, em vez de no app que a transmite. As recomendações continuam as mesmas: só dos apps da própria TV. Só na Google TV | `false` |
| `language` | `auto` (segue a TV), ou um idioma com [tradução](#traduções) (`en`, `pt`, `es`, `de`, `ru`, `fr`, `ja`…) | `auto` |
| `show_crypto` | Mostra preços de cripto da Binance na tela inicial e no protetor de tela | `true` |
| `currency` | Preços das criptos em `USD`, `EUR`, `BRL`… | `USD` |
| `temperature` | `C`, `F` ou `auto` | `auto` |
| `theme` | `auto` (escuro do pôr do sol ao nascer do sol), `light` ou `dark` | `auto` |
| `disable_assistant` | Também desliga o Google Assistente | `false` |
| `screensaver` | `false` mantém o protetor de tela da TV: o Free My TV então muda só a tela inicial e os apps promocionais (Google TV) | `true` |
| `hide_services` | Serviços de streaming para deixar fora das recomendações mesmo com o app na TV (`netflix`, `prime`, `disney`…), separados por vírgula; para apps que a TV traz e você não assina. Na Google TV e Android TV, um serviço que o TMDB lista no seu país com o mesmo nome de um app da TV também aparece em *Recomendações de*, desligado até você ativar. É de onde partem as chaves em Ajustes da Tela Inicial › Recomendações › Recomendações de; o que você mudar na TV vence. Só na Google TV | vazia |
| `hide_apps` | Apps para deixar fora da prateleira, Todos os Apps e das recomendações, por id ou nome (parte dele), separados por vírgula; para apps que a TV traz e não podem ser desinstalados, como a Netflix embutida da Samsung. Só LG e Samsung | vazia |
| `shelf_apps` | Os apps da prateleira nessa ordem, por id ou nome (parte dele), separados por vírgula; mudar isso vence uma vez sobre a prateleira escolhida na TV. Na Samsung, um id completo de app também traz um app que a TV deixa fora da lista, como um instalado em Developer Mode. Só LG e Samsung | vazia |
| `drawer_first` | `true` abre a tela inicial com a gaveta já aberta (apps no meio, entradas, tempo e preços embaixo), para não precisar rolar até as entradas; Voltar a fecha para a página completa. Para uma TV cujos apps de streaming moram numa caixa, e as recomendações ficam vazias. Só LG e Samsung | `false` |
| `immich_server` | Opcional: seu servidor [Immich](https://immich.app): [suas próprias fotos](#de-um-servidor-immich) vêm dele, em cada TV para a qual você envia a chave (com `tools/send_key.py`, nunca aqui). Só na Google TV | vazia |
| `open_picks_in` | Onde uma recomendação abre: `apps` (o app de streaming que a tem) ou `nuvio` (a página do título no Nuvio, quando a TV o tem); Ajustes da Tela Inicial muda isso na TV. Só na LG (a Samsung ainda não passa link) | `apps` |

Mudou algo? Rode `./build.sh` e instale de novo. Guarde o `freemytv.keystore`: as atualizações são assinadas com ele.

### A chave do TMDB

Grátis, e leva dois minutos: crie uma conta em [themoviedb.org](https://www.themoviedb.org/signup), abra [Configurações → API](https://www.themoviedb.org/settings/api) e peça uma chave de desenvolvedor. Cole o *API Read Access Token* (ou a *API Key*) depois de `tmdb_key=`. A chave é sua: o `config.properties` fica fora do git.

Na Google TV e Android TV você também pode adicioná-la na TV, o que o APK das releases precisa: *Ajustes da Tela Inicial* → *Chave TMDB* mostra um QR code. Escaneie com o celular (no mesmo Wi‑Fi), cole a chave e envie; a TV a verifica com o TMDB e a guarda. O código vale uma vez, por 5 minutos, e só enquanto está na tela. A página do celular é HTTP puro no seu Wi‑Fi: numa rede em que não confia (a de um hotel), digite a chave. Sem celular à mão? *Digite com o controle*: a *API Key* curta (32 caracteres) é a mais fácil de digitar. Uma chave adicionada na TV vence a do `config.properties`, e *Remover a chave* volta para ela.

Na LG e Samsung você também pode digitá-la na TV, em *Ajustes da Tela Inicial* → *Chave TMDB*: a *API Key* curta (32 caracteres) é a mais fácil de digitar no controle. O TMDB a verifica antes de salvar, ela fica na TV, e vence a do `config.properties` (*Remover a chave* volta para essa).

### Abrindo o título, não só o app (opcional)

Com uma chave gratuita do [Watchmode](https://api.watchmode.com/) (*Ajustes da Tela Inicial* → *Chave Watchmode* na Google TV e Android TV: um QR code para o celular, ou digitada, como a do TMDB; ou `watchmode_key=` no `config.properties`, e a da TV vence), uma recomendação abre a página própria do título no app de streaming em vez da home do app. O plano gratuito (2.500 créditos por mês) basta: cada título custa dois pedidos na primeira vez e fica memorizado depois. Funciona onde o app aceita o endereço web do título (testado: Prime Video, JioHotstar, Netflix e Disney+); onde não aceita, a recomendação só abre o app, como sem chave.

### Botões do Home Assistant (opcional)

Na Google TV e Android TV, a gaveta de baixo pode guardar botões para o seu [Home Assistant](https://www.home-assistant.io/): uma luz, uma cena de noite de filme, um ventilador. No `config.properties`:

```properties
home_assistant_url=http://homeassistant.local:8123
home_assistant_entities=light.living_room, scene.movie_night, switch.fan
```

Compile e instale de novo: *Ajustes da Tela Inicial* ganha uma linha *Home Assistant* (só builds com um endereço a têm). Depois envie o token do computador, um long-lived access token (no Home Assistant: seu perfil → Segurança → Long-lived access tokens):

```bash
python3 tools/send_key.py 192.168.1.50 home_assistant_token
```

Ele pede o token sem mostrá-lo, verifica no seu servidor, lista o que cada entidade vira, envia por adb para os arquivos privados do app, e pergunta à TV se chegou (Android 9 e mais novos). Ele nunca vai para o APK nem para o `config.properties`, já que qualquer app na TV pode ler um APK instalado, e um token do Home Assistant alcança todos os serviços, cadeados incluídos. Um usuário do Home Assistant próprio que não seja administrador ainda é o mais seguro. `--remove` o tira da TV de novo.

Depois ligue *Ajustes da Tela Inicial* → *Home Assistant* na TV: ele começa desligado. Um grupo de botões entra entre Entradas e Atalhos, um por entidade (até 8, na sua ordem), com o nome que vem do Home Assistant; todo ladrilho da gaveta divide a mesma largura, então mais botões os deixam todos mais estreitos. O OK liga e desliga uma luz, tomada, ventilador ou cortina, acende uma cena ou script, roda uma automação ou aperta um botão; um que está desligado aparece esmaecido. Cadeados e alarmes nunca são oferecidos, já que qualquer um na sala pode apertar um controle de TV, e cortinas só quando sombreiam uma janela (toldo, persiana, cortina, shade ou shutter): não portões de garagem, portões nem portas, nem uma cortina sem classe, como muitos portões de garagem são. Um script, cena, automação ou botão roda o que estiver configurado, então não liste um que destranca uma porta, abre a garagem ou desliga um alarme: a mesma promessa dos cadeados. O endereço pode ser `http://` só na sua rede (um endereço privado como `192.168.1.20`, ou um nome `.local`, `.lan` ou `.home.arpa`); qualquer outra coisa precisa de `https://`, e redirecionamentos não são seguidos.

### Suas próprias fotos (opcional)

Na Google TV e Android TV, com a TV conectada pelo adb (veja *Instalação*), envie fotos ou pastas inteiras do seu computador:

```bash
python3 tools/photos.py <IP da TV> praia.jpg morros.jpg Ferias/
```

Elas chegam na pasta do próprio app na TV (sem precisar de permissão); no Android 11, que impede o adb de entrar em pastas de outros apps, elas passam pelo próprio Free My TV. Na próxima vez que a tela inicial, o protetor de tela ou os ajustes do Free My TV abrirem, o app importa cada uma: endireitada, cortada para 16:9, redimensionada para a TV e salva sem o GPS dela e outras marcações; o que foi enviado é então apagado. O protetor de tela as mostra na ordem em que você as enviou, no lugar das fotos das recomendações; sem chave TMDB, uma delas é o fundo da tela inicial, uma nova a cada hora. *Ajustes da Tela Inicial* → *Minhas Fotos*: as setas ligam e desligam, o OK remove. Até 100; JPEG, PNG e WebP, e HEIC no Android 9 e mais novos.

#### De um servidor Immich

Com um servidor [Immich](https://immich.app), a TV pode buscá-las sozinha. No `config.properties`, ponha em `immich_server` o endereço dele (`http://192.168.1.20:2283` na sua rede, ou o endereço `https://`), e compile e instale de novo. Depois crie uma chave em Immich → *Account Settings* → *API Keys* (`asset.read`, `asset.view`, `asset.download` e `album.read` bastam) e envie a cada TV que deve mostrar suas fotos (Android 9 e mais novos):

```bash
python3 tools/send_key.py <IP da TV> immich_api_key
```

Ele pede a chave sem mostrá-la, verifica no seu servidor (uma busca, um preview e um original, como a TV faz), a põe no armazenamento privado do app na TV por adb, e pergunta à TV se chegou. Ela nunca vai para o APK, que qualquer app na TV pode ler, nem para o `config.properties`; `--remove` a tira da TV. Uma TV sem a chave mantém *Minhas Fotos* como acima.

A cada 6 horas, quando a tela inicial abre, uma nova escolha aleatória de até 40 fotos entra (pelo menos 1080 pixels no lado curto), uma por vez, pela mesma importação. Nada sai antes de algo novo chegar: nas 100, as mais antigas do Immich dão lugar, e as fotos que você enviou com `tools/photos.py` sempre ficam. *Ajustes da Tela Inicial* → *Minhas Fotos* escolhe então de onde vêm: *Padrão* (nenhuma sua: as fotos das recomendações), *Immich: todas as fotos* ou um dos álbuns; depois da mudança, as anteriores saem conforme as novas chegam. TVs com pouca memória ou tela 720p pegam o preview do Immich de cada foto em vez do original.

Um servidor dado como `http://` deve estar na sua rede (um endereço privado como `192.168.1.20`, ou um nome `.local`, `.lan` ou `.home.arpa`; o build recusa outra coisa), e só o endereço dele pode ser alcançado sem HTTPS; qualquer outra coisa precisa de `https://` (no Tailscale, o endereço `https://<máquina>.<tailnet>.ts.net` do servidor, que o Tailscale pode servir com certificado). O app nunca segue um redirecionamento dele, então a chave só vai para aquele endereço.

### Sua biblioteca Plex (opcional)

Ponha `plex_url` e `plex_token` no `config.properties`, e um dos filmes mais novos e uma das séries mais novas do seu servidor Plex (outros a cada vez que a lista é feita, algumas vezes por dia, entre os 8 mais recentes de cada tipo) entram nas recomendações, com pôster e backdrop próprios, marcados "Plex". Uma aba mostra no máximo um. Selecionar um abre a página do título no app do Plex. Se o servidor não puder ser alcançado quando a lista é feita, os títulos dele ficam de fora.

Isso é para Google TV e Android TV, e precisa da chave TMDB e de pelo menos um app de streaming na TV: sem isso nenhuma recomendação vem, Plex incluído.

- **`plex_url`** é o endereço `plex.direct` do próprio servidor, que tem certificado válido (a TV o verifica como qualquer site; `http` puro e qualquer outro endereço são ignorados, então um erro de digitação nunca manda seu token para lugar nenhum). Ele tem a forma `https://192-168-1-20.0123456789abcdef0123456789abcdef.plex.direct:32400`: o IP local do seu servidor com travessões, e depois o id dele. Abra qualquer item no app web do Plex, *Get Info → View XML*, e a barra de endereço o tem, antes de `/library/...`.
- **`plex_token`** está no mesmo endereço, depois de `X-Plex-Token=`. Ele dá acesso à sua conta Plex, e qualquer app na TV pode ler o APK em que é embutido, então use o token de um *managed user* do Plex Home com acesso às suas bibliotecas, não o seu, e nunca o commite.

A TV fala com o seu servidor direto, na sua rede. Se o servidor não puder ser alcançado, as outras recomendações carregam como sempre.

## Voltando atrás

Na TV: *Free My TV* → *Tela Inicial* → *Original*. A tela inicial de fábrica, o protetor de tela e todos os apps voltam exatamente como eram. Se a nova tela inicial travar três vezes em cinco minutos, ela volta sozinha.

Para remover de vez, volte para o *Original* primeiro, e desinstale o *Free My TV* (Configurações → Apps). Desinstalou com ele ligado? Instale de novo e escolha *Original*: a lista do que ele desligou fica guardada nos ajustes da TV, e tudo volta.

## O que ele muda

- Ele vira a tela inicial e, a menos que `screensaver=false`, o protetor de tela.
- Escolher Continuar Assistindo nos Ajustes da Tela Inicial concede `READ_TV_LISTINGS` com `pm grant` pelo ADB da própria TV; o *Original* o revoga com `pm revoke`. As imagens vêm só da TV (`content://`, `android.resource://`), nunca da rede.
- Ele desliga, sem desinstalar:
  - a tela inicial e o protetor de tela de fábrica (o protetor fica com `screensaver=false`);
  - a tela de recuperação da Google TV, o Play Games e o YouTube Music;
  - em TVs TCL, apps de mensagens, demo de loja, menu de hotel, manuais, espelhamento e logs;
  - em TVs Philco, AI PONT (canais promocionais e downloads de apps) e o manual;
  - em TVs Multilaser, o reconhecimento de conteúdo de tela da Anoki (ACR), o demo de loja e o manual;
  - em TVs feitas pela KTC (NextStar), o reconhecimento de conteúdo de tela da Anoki (ACR), o demo de loja e o manual;
  - o Google Assistente, só com `disable_assistant=true`.
- Na Google TV, os resultados do Assistente para filmes e séries vêm do app de tela inicial da Google TV, que fica desligado no modo Free My TV: pedir para reproduzir uma série pode acabar em "Desculpe, não entendi", e uma busca pode mostrar só vídeos do YouTube. Abrir apps, perguntas e a busca por voz dos próprios apps (a do YouTube, por exemplo) continuam funcionando; o *Original* traz tudo de volta.
- Em TVs TCL, os botões Netflix, YouTube e Prime do controle continuam funcionando por um pequeno serviço de acessibilidade que só lê esses botões. Escolha o que cada um abre em *Free My TV* → *Botões do Controle*; o *Original* desliga o serviço. O botão Settings abre os Ajustes da TV; em *Botões do Controle* ele pode abrir *Quick Settings* em vez disso, um painel sobre o que está passando (Entradas, Imagem, Som, Rede, Bluetooth, Acessibilidade e todos os ajustes) no lugar do da Google TV, que é parte da tela inicial dela. Em TVs TCL com Android 11 o serviço fica desligado, já que com ele a TV movia o volume dois passos por toque: lá os botões funcionam na tela inicial do Free My TV. Em TVs feitas pela Vestel (F&U e outras marcas de loja) e projetores Xiaomi (Formovie) o mesmo vale para o botão Netflix, e em TVs feitas pela KTC (NextStar) para o botão Tabii. Em TVs Sony, os botões BRAVIA CORE, Netflix, Disney+, Prime Video, YouTube e Crunchyroll (e Google Play ou SonyLIV, nos controles que os têm) podem cada um abrir o app que você escolher, ou manter o padrão da Sony. Nos modelos Google TV da Sony, em que esses botões passavam pela tela inicial da Google TV, eles abrem os próprios apps a menos que você escolha outro. Em TVs Xiaomi cujo controle tem um botão Mi no lugar do Home, esse botão abre o Free My TV em vez do PatchWall (ou, se você escolher, o PatchWall como antes, ou outro app). Em TVs Xiaomi, o botão YouTube abre o YouTube de novo (a tela inicial da Google TV o respondia), e o botão PatchWall pode abrir o app que você escolher. Em TVs Xiaomi vendidas na Rússia, o mesmo vale para os botões Okko, VK, Rutube, KION, Wink e IVI, que mantêm o padrão da Xiaomi até você escolher outro app. Em TVs Hisense, os botões Prime Video, YouTube, Disney+, Todos os Apps, Ajustes e perfil, que a tela inicial da Google TV respondia, abrem o que você escolher (Todos os Apps abre o próprio do Free My TV; a Netflix fica com a TV). No Google TV Streamer, os botões YouTube, Netflix e ★ podem cada um abrir o app que você escolher ou o Todos os Apps do Free My TV: o YouTube abre o YouTube (a tela inicial da Google TV o respondia, e o ★ também), e a Netflix e o ★ mantêm o padrão do Google até você escolher algo, então o ★ não faz nada no modo Free My TV até lá. No JVC G24 (Skyworth), cujos botões Entradas e Ajustes precisam da tela inicial da Google TV, Entradas abre a lista de entradas da TV e Ajustes um pequeno painel de Quick Settings (Imagem, Som, Entradas, Wi‑Fi, Bluetooth e Ajustes da TV). Em qualquer uma dessas TVs, pôr todos os botões em *Nada* (ou no padrão da marca) desliga o serviço.
- Com *Ajustes da Tela Inicial* → *Widget Tocando Agora* ligado (começa desligado), o que um app está tocando aparece no lugar dos preços enquanto toca, na tela inicial e no protetor de tela. O Android entrega isso só a um notification listener, então ligar o widget permite o nosso pelo ADB da TV; desligá-lo, o *Original* e a volta após travamentos o levam embora. Onde a TV o recusa, a linha avisa.
- Em projetores HY300, cuja tela inicial de fábrica era o único caminho até ela, a gaveta de baixo ganha *Keystone* (keystone, zoom e modo de projeção) e *Espelhamento de Tela* (o receiver Miracast do projetor), e o HDMI abre pelo player do próprio projetor.
- *Ajustes da Tela Inicial* → *Apps Recentes* (desligado por padrão, Google TV e Android TV) põe *Apps Recentes* na gaveta de baixo, e na tecla de troca de app do controle onde ela existe; *Gaveta e Home duas vezes* também o abre com dois toques rápidos em Home (não em TVs Xiaomi, cujo controle envia um toque como vários), e *Botões do Topo* pode adicioná-lo como um botão redondo. Ele mostra os apps abertos sobre a tela inicial borrada: o OK abre um, ▲ o fecha. Fechar encerra o app (`am force-stop`), então ele começa do zero na próxima vez; as peças próprias da TV, o que as entradas e o controle dela precisam, apps cujo serviço de acessibilidade está ligado e o teclado não podem ser fechados. Ele lê a lista só enquanto está aberto, com `dumpsys activity recents` e `ps -A` pelo ADB da TV.
- Na Google TV, Android TV e Fire TV, segure OK num botão do topo ou num app da prateleira para movê-lo direto na Home: ◀ ▶ muda a posição, OK salva, e Voltar cancela. Sair da Home também cancela uma movimentação incompleta. Um toque curto ainda abre o item; os editores de Prateleira e Botões do Topo nos Ajustes continuam disponíveis.
- *Free My TV* → *Botões do Topo* → *Loja de Apps* (Google TV, Android TV e Fire TV) adiciona um atalho de sacola de compras no topo da tela inicial. Ele abre a Google Play ou, no Fire TV, a Amazon Appstore. OK adiciona ou remove; ◀ ▶ o move para perto da TV ao vivo, ou onde você preferir. Começa desligado, e fica indisponível quando nenhuma loja suportada pode ser aberta.
- *Ajustes da Tela Inicial* → *Ao ligar* (Google TV e Android TV, onde a TV tem TV ao vivo) decide o que aparece depois de a TV ligar; acordar do standby é deixado de lado. *Escolha da TV* (o padrão) não muda nada. *Tela inicial* devolve a tela ao Free My TV quando o app de TV ao vivo da TV se põe na frente durante o início, como algumas TVs MediaTek fazem, mas só se nenhuma tecla foi apertada desde que a tela inicial surgiu. *TV ao vivo* abre a TV ao vivo uns 10 segundos depois de a tela inicial surgir, a menos que uma tecla tenha sido apertada antes (na Sony, o app de TV da Sony, que lembra a última entrada e o último canal).
- *Free My TV* → *Temporizador* desliga a TV depois de 5 minutos a 4 horas, com os minutos que faltam sobre qualquer app (no topo, ao centro, ou no canto que você escolher). Ele aperta a tecla Sleep do controle pelo ADB da própria TV, então funciona no modo Free My TV; o *Original* o para.
- Imagem, som, entradas, pareamento do controle, serviços do Google e a Play Store estão numa lista protegida, verificada antes de cada mudança, e as peças do próprio Android e menus de fábrica também. Antes de algo desligar, a TV é perguntada se as entradas dela ou a tecla Input do controle dependem disso; essas ficam ligadas.
- Na Google TV, o app de configuração desliga antes da tela inicial de fábrica e volta depois dela, então a tela de recuperação dele nunca toma o botão Home no meio do caminho.
- Apps que salvaram uma rede Wi‑Fi nunca são desligados, já que o Android apagaria a rede. Se a configuração inicial da TV salvou a sua, a troca pede para você esquecer a rede e conectar de novo nos Ajustes primeiro (redes salvas fora de alcance não aparecem lá; o Claude Code pode removê-las).

## Qualquer TV

O Free My TV roda na Google TV e Android TV: TCL, Sony, Hisense, Philips, Xiaomi, TVs feitas pela Vestel (F&U), feitas pela KTC (NextStar) e outras, além de streamers como o Chromecast com Google TV, o Google TV Streamer, onn 4K, o Xiaomi Mi TV Stick e NVIDIA Shield, e projetores como o Wanbo T2 Ultra. E em TVs [LG](#tvs-lg-webos) e [Samsung](#tvs-samsung-tizen), como um app.

**TVs Huawei (HarmonyOS) e a Kalley 43G200:** nelas o Free My TV fica como um app para abrir. Depois da troca, uma de cada não ligou de novo (a Huawei só voltou com uma restauração de fábrica), então a troca recusa nelas, e uma já trocada por uma versão mais antiga volta para o *Original* sozinha. No Fire TV também é um app: a tela inicial da Amazon guarda o botão Home.

**Qualquer outra TV:** ligue um streamer Google TV no HDMI e liberte essa. Mesmos passos, mesma tela inicial.

**Outra marca ou modelo:** pergunte ao Claude. O Free My TV é feito para ser adaptado por IA. Abra a pasta no Claude Code e diga *"configure para a minha Sony"*: ele lê a sua TV, acha a tela inicial dela e os apps promocionais, atualiza as listas abaixo e te guia num teste. O [CLAUDE.md](CLAUDE.md) diz como.

| O quê | Onde |
|---|---|
| Apps para desligar | `DEBLOAT` no [`HomeMode.java`](app/src/io/freemytv/HomeMode.java) |
| Apps para nunca tocar | `PROTECTED` no mesmo arquivo |
| Apps da prateleira | `SHELF` no [`HomeApps.java`](app/src/io/freemytv/HomeApps.java) |
| O app de TV ao vivo da sua marca | `LIVE_TV_APPS` no mesmo arquivo |

## Deixe com a sua cara

É o seu código, e o Claude Code se acha nele. Experimente:

- *"Adiciona o Crunchyroll à prateleira."*
- *"Mostra os preços em euros."*
- *"Adiciona catalão."*
- *"Muda para o visual noturno uma hora depois do pôr do sol."*

## Como funciona

- **Um app Android comum, sem Gradle, sem bibliotecas.** O [`build.sh`](build.sh) roda aapt2 → javac → d8 → zipalign → apksigner e faz um APK de 2 MB.
- **Ele usa o ADB da própria TV, de dentro da TV.** O app conecta a `127.0.0.1:5555` com a chave dele (é o aviso *Permitir depuração USB?*) e roda os mesmos comandos que você: `cmd package set-home-activity`, `settings put secure screensaver_components`, `pm disable-user`, `pm grant` / `pm revoke` para o Continuar Assistindo e, com os Apps Recentes abertos (começa desligado), `dumpsys activity recents`, `ps -A -o NAME`, `settings get secure enabled_accessibility_services` e `default_input_method`, e `am force-stop` para um app que você fecha. Nada escuta a rede.
- **Desenhado à mão num único Canvas**, com shaders do Android 13 para o vidro fosco e o céu (preenchimentos simples no Android 8 a 12, com sombras mais leves e sem camadas de GPU no 8 a 11, pelas GPUs mais antigas deles).
- **Uma rede de segurança.** Um watchdog num processo separado traz de volta a tela inicial de fábrica depois de três travamentos em cinco minutos, e uma checagem de boot guarda a sua escolha depois das atualizações da TV.
- **Na LG e Samsung, o mesmo design em HTML, CSS e JavaScript puros** ([`web/`](web)), escrito para o Chromium de TVs antigas, sem frameworks. O [`webos/build.py`](webos/build.py) empacota com o `config.properties` num `.ipk` sem as ferramentas da LG, e o [`webos/install.py`](webos/install.py) instala pelo Developer Mode; na LG ele lista e abre apps pelo barramento de serviços da própria TV (Luna), como o launcher da LG faz. O [`tizen/build.py`](tizen/build.py) empacota o mesmo app num `.wgt` da Samsung, que usa as APIs web do Tizen para os apps e as entradas. Para prever no computador: `python3 webos/build.py --preview`, e abra `out/webos/index.html` (um substituto lista apps de exemplo).
- **Continuar Assistindo** lê a lista Watch Next do Android TV (o que os apps compartilham sobre o que você assiste). Só escolher concede `READ_TV_LISTINGS` pelo ADB da TV; o *Original* o revoga. As imagens carregam só da TV (`content://`, `android.resource://`), nunca da rede.
- **Os dados** vêm só do TMDB (títulos em alta, lançamentos e qual app transmite o quê no seu país), Open-Meteo (previsão, nascer e pôr do sol), opcionalmente da Binance (preços de 24 horas quando `show_crypto=true`), opcionalmente do Watchmode (as páginas próprias das recomendações nos apps, com uma `watchmode_key`), opcionalmente do seu servidor Plex (com um `plex_url`), opcionalmente do seu servidor Immich (suas fotos, com um `immich_server` e a chave dele) e opcionalmente do Trakt (o que você assiste e sua watchlist, com um `trakt_client_id`, uma vez que você entre na TV).

| Arquivo | O que é |
|---|---|
| [`HomeView.java`](app/src/io/freemytv/HomeView.java) | A tela inicial |
| [`HomeMode.java`](app/src/io/freemytv/HomeMode.java) | A troca entre Free My TV e Original |
| [`Adb.java`](app/src/io/freemytv/Adb.java) | O ADB da própria TV, de dentro da TV |
| [`Recs.java`](app/src/io/freemytv/Recs.java) | As recomendações (TMDB) |
| [`KeyPage.java`](app/src/io/freemytv/KeyPage.java), [`Qr.java`](app/src/io/freemytv/Qr.java) | As chaves TMDB e Watchmode enviadas do celular, e o QR code |
| [`WatchNext.java`](app/src/io/freemytv/WatchNext.java) | Continuar Assistindo, das listas da TV |
| [`WatchArt.java`](app/src/io/freemytv/WatchArt.java) | As imagens do Continuar Assistindo, só da TV |
| [`HomeData.java`](app/src/io/freemytv/HomeData.java) | Tempo e preços |
| [`HomeApps.java`](app/src/io/freemytv/HomeApps.java) | A prateleira, as entradas e Todos os Apps |
| [`DreamView.java`](app/src/io/freemytv/DreamView.java) | O protetor de tela |
| [`SettingsActivity.java`](app/src/io/freemytv/SettingsActivity.java) | A tela de ajustes (o ícone do app) |
| [`Prefs.java`](app/src/io/freemytv/Prefs.java) | Ajustes mudados na TV |
| [`RemoteKeys.java`](app/src/io/freemytv/RemoteKeys.java) | Os botões de app do controle (TCL, Sony, Xiaomi e outros) |
| [`RecentApps.java`](app/src/io/freemytv/RecentApps.java), [`ScreenBlur.java`](app/src/io/freemytv/ScreenBlur.java) | Apps Recentes, sobre uma cópia borrada da tela |
| [`Watchdog.java`](app/src/io/freemytv/Watchdog.java) | A rede de segurança |
| [`web/home.js`](web/home.js) | A tela inicial nas TVs LG |
| [`web/tv.js`](web/tv.js) | Os apps e as entradas da TV, na LG e Samsung |
| [`webos/build.py`](webos/build.py), [`webos/install.py`](webos/install.py) | O pacote do app LG e a instalação dele |
| [`tizen/build.py`](tizen/build.py) | O pacote do app Samsung |

O site ([freemytv.io](https://freemytv.io)) está em [`docs/`](docs): HTML, CSS e JS puros no GitHub Pages.

## Traduções

Na Google TV, LG e Samsung, cada idioma é um arquivo, [`app/assets/i18n/<lang>.json`](app/assets/i18n), chaveado pelo
texto em inglês no código. *Automático* segue o idioma da TV e usa qualquer idioma que tenha arquivo (inglês caso contrário); *Ajustes
da Tela Inicial* → *Idioma* lista todos. Hoje: inglês, português, espanhol, alemão, francês, italiano, holandês, polonês,
sueco, dinamarquês, norueguês, finlandês, tcheco, romeno, turco, russo, ucraniano, grego, japonês, coreano, chinês
simplificado e tradicional, híndi, indonésio, vietnamita e tailandês. Português, espanhol, alemão, russo, tailandês e turco foram traduzidos à mão e são a
referência (corrija-os à mão); os outros foram feitos por máquina, e correções de falantes nativos são bem-vindas.

- **Adicionar um idioma:** `python3 tools/translate.py --new ca`, e preencha `app/assets/i18n/ca.json` à mão, ou, com
  `ANTHROPIC_API_KEY` definida, `python3 tools/translate.py --fill --lang ca` (só as strings vão para a API).
- **Depois de mudar texto no código:** `python3 tools/translate.py` lista o que falta a cada idioma; `--fill` traduz
  só isso (os traduzidos à mão — português, espanhol, alemão, russo, tailandês e turco — ficam para uma pessoa,
  a menos que `--lang` os nomeie), `--prune` descarta strings que o código não usa mais.
  Rode `python3 tools/translate.py --check` para validar todos os catálogos sem escrever arquivos.
- Texto construído em tempo de execução tem placeholders (`"{n} min ago"`), então cada idioma põe as palavras na
  ordem dele. Uma chave como `"unit|Automatic"` é o mesmo inglês em outro lugar, onde um idioma pode precisar de
  outra palavra.
- Contagens têm formas de plural: `"plural|one:{n} season|other:{n} seasons"` é traduzido com uma forma por
  categoria de plural que o idioma usa (russo `"one:{n} сезон|few:{n} сезона|many:{n} сезонов|other:{n} сезона"`,
  japonês só `"other:{n}シーズン"`), e as regras de plural do Android escolhem a de cada número.
- **Limites:** idiomas da direita para a esquerda (árabe, hebraico, persa) precisariam do layout espelhado, então
  ainda não estão lá. Chinês, japonês, coreano e híndi são desenhados com a fonte do sistema da TV (a Inter não tem
  tais letras).

## Privacidade

Sem contas, sem analytics, sem rastreamento. O app fala com o TMDB, o Open-Meteo (com as coordenadas que você definiu, ou a cidade principal do seu fuso horário) e a Binance só quando `show_crypto=true`, com o Watchmode só quando você define uma chave, com o seu servidor Plex só quando você define um `plex_url`, com o seu servidor Immich só quando você define um, e com o Trakt (api.trakt.tv) só quando você define um `trakt_client_id` e entra na TV. Com `home_assistant_url` definido e *Ajustes da Tela Inicial* → *Home Assistant* ligado, ele fala com aquele servidor, seu, e com nenhum outro: só enquanto a gaveta de baixo está aberta, para ler os estados das entidades que você listou e chamar a que você aperta. Desligado, nada é pedido a ele, e os nomes que ele leu são esquecidos. Na Google TV e Android TV, o APK da release pergunta ao GitHub (api.github.com) uma vez por semana, ou quando você aperta *Atualizações*, pela última release, e quando há uma mais nova a baixa de github.com e do servidor de downloads do GitHub (release-assets.githubusercontent.com); um build feito por você pergunta só quando você aperta *Atualizações*. O *Widget Tocando Agora* lê o que os apps estão tocando (título, artista, o app) por um notification listener, o único jeito com que o Android compartilha isso: o Free My TV permite o listener só enquanto o widget está ligado, nunca lê uma notificação com ele, e pede ao Android para desvinculá-lo assim que conecta, então ele fica desvinculado. O que está tocando nunca sai da TV. Enquanto *Ajustes da Tela Inicial* → *Chave TMDB* ou *Chave Watchmode* mostra o QR code (5 minutos no máximo), a TV responde na sua rede doméstica no endereço daquele código, para uma chave; a chave vai só para aquele serviço, para verificação. O Continuar Assistindo (Ajustes da Tela Inicial) lê o que seus apps anotam na própria TV e mostra só imagens que já estão na TV: não baixa nada. *Ajustes da Tela Inicial* → *Ícones de status* lê só se a TV tem Wi‑Fi ou Ethernet, um dispositivo de áudio Bluetooth e um drive USB montado, e só enquanto a linha está ligada: no Android 12 e mais novos pede *Dispositivos próximos* (BLUETOOTH_CONNECT) para a parte do Bluetooth, e nada disso sai da TV. Suas configurações ficam no seu computador e na sua TV.

## Créditos

- Feito com [Claude Code](https://claude.com/claude-code).
- A versão LG se apoia no que [@danielthejoker18](https://github.com/danielthejoker18) achou no [FreeMyTvWebOS](https://github.com/danielthejoker18/FreeMyTvWebOS) (MIT): instalar pelo Developer Mode e abrir apps pelo barramento de serviços da TV.
- Em TVs Samsung ele instala com o [TizenBrew Installer](https://github.com/reisxd/TizenBrewInstaller) de [@reisxd](https://github.com/reisxd).
- Este produto usa a API do TMDB, mas não é endossado ou certificado pelo [TMDB](https://www.themoviedb.org/).
- Links para os títulos nos apps de streaming pelo [Watchmode](https://api.watchmode.com/).
- Dados de tempo por [Open-Meteo.com](https://open-meteo.com/) (CC BY 4.0). Preços da API pública da [Binance](https://www.binance.com/).
- Ícones: [Material Symbols](https://fonts.google.com/icons) (Apache 2.0). Fonte: [Inter](https://rsms.me/inter/) (SIL OFL 1.1). Logos das moedas: [cryptocurrency-icons](https://github.com/spothq/cryptocurrency-icons) (CC0). Logos dos apps Samsung: [Simple Icons](https://simpleicons.org) (CC0).
- O codificador de QR code segue o [QR Code generator](https://www.nayuki.io/page/qr-code-generator-library) do Project Nayuki (MIT).
- Sem afiliação com Google, TCL, LG, Samsung ou qualquer serviço de streaming. Nomes e logos de apps pertencem aos seus donos.

## Licença

[MIT](LICENSE). Fork it, change it, ship it.
