# AURALIS: The Pale Curse

**Português (BR)** · [English below](#english)

> Metroidvania sombrio de ação e exploração, feito por **Bruno Assunção Dias**.
> Versão atual: **0.99.x** (pré-lançamento) · Engine: Godot 4.3
> Jogue a versão web: **https://auralisgame.vercel.app/**

## O que é

Uma maldição pálida cobre o reino e só Auralis pode enfrentá-la. AURALIS é um metroidvania 2D sombrio: explore cavernas
e ruínas, enfrente chefes, desbloqueie habilidades e descubra segredos que mudam o rumo da história.

### Recursos principais

- **10 fases** com **chefes nomeados**
- **Árvore de habilidades** para montar o seu estilo de luta
- **Aparo (parry)**: defenda no tempo certo e contra-ataque
- **Poços e segredos** escondidos pelo mapa
- **Dois finais**
- **Vozes em português e inglês**
- **Legendas em 8 idiomas** (em breve)

### Controles básicos

A/D ou setas: mover · Espaço ou W: pular · J, X ou Z: atacar · P: pausa · Esc: menu · M: mini mapa.
As teclas podem ser redefinidas em Opções → Controles. Também há suporte a controle.

## Notas de desenvolvimento

AURALIS é desenvolvido por Bruno, com **apoio de inteligência artificial na criação de arte e código**.
Feito com **Godot 4.3** (GDScript), com ferramentas de apoio em Python. O jogo está em desenvolvimento ativo e ainda podem existir bugs.

## Requisitos

- Windows 10 ou 11, **64 bits**
- Placa de vídeo com suporte a OpenGL 3.3 (renderizador de compatibilidade do Godot)
- Cerca de **170 MB de download** e **250 MB livres** em disco
- Internet apenas para instalar (o jogo roda offline)
- Não precisa de administrador: instala só para o seu usuário

## Como instalar (passo a passo)

1. Baixe o instalador: **[releases/AURALIS-Setup.exe](releases/AURALIS-Setup.exe)** (botão *Download raw file* na página do arquivo).
2. (Recomendado) Confira o SHA-256, veja [Verificação do instalador](#verificação-do-instalador).
3. Execute o `AURALIS-Setup.exe`. Se aparecer a tela azul do SmartScreen, veja [Aviso azul do Windows](#aviso-azul-do-windows-smartscreen).
4. Escolha o idioma (Português ou English) e clique em **Avançar**.
5. Na tela de **autorização**, leia de onde os arquivos serão baixados e o tamanho, marque **"Autorizo o download dos arquivos do jogo"** e avance. Sem a autorização a instalação não continua.
6. Escolha a pasta (padrão: `%LOCALAPPDATA%\Programs\AURALIS`) e os atalhos (Menu Iniciar e/ou Área de Trabalho).
7. Aguarde: o instalador baixa as partes, confere o SHA-256 de cada uma e do pacote completo, junta, descompacta e instala.
   Se a internet cair, ele tenta de novo 3 vezes por parte; ao executar de novo, as partes já baixadas e verificadas são reaproveitadas.
8. Marque **Executar AURALIS** e clique em **Concluir**.

Instalação silenciosa (para automação): `AURALIS-Setup.exe /S /ACCEPT` (opcionais: `/D=C:\Pasta`, `/LANG=en`).
`/ACCEPT` significa que você autoriza o download.

### Aviso azul do Windows (SmartScreen)

Enquanto o instalador não for **assinado digitalmente**, o Windows mostra "O Windows protegeu seu computador".
Isso acontece com qualquer programa de um autor independente que ainda não tem reputação, não significa que há vírus.
Assinar exige um certificado de assinatura de código (pago, com verificação de identidade); o instalador ainda não é assinado.
Para continuar: clique em **Mais informações** e depois em **Executar assim mesmo**.
Se preferir, confira o SHA-256 do instalador (abaixo) antes de executar.

### Verificação do instalador

O SHA-256 oficial fica em [releases/SHA256.txt](releases/SHA256.txt). No PowerShell, na pasta do download:

```powershell
Get-FileHash .\AURALIS-Setup.exe -Algorithm SHA256
```

(ou no Prompt de Comando: `certutil -hashfile AURALIS-Setup.exe SHA256`). O resultado deve ser idêntico ao do arquivo.

### Instalação manual / offline (alternativa)

Sem o instalador, você pode montar o jogo à mão:

1. Baixe de [dados/](dados/) todos os arquivos `AURALIS-<versão>.partNNN.<hash>` e o `manifesto.json`.
2. No Prompt de Comando, na pasta dos arquivos, junte as partes em ordem: `copy /b AURALIS-*.part* AURALIS.zip`
3. Confira: `certutil -hashfile AURALIS.zip SHA256` deve ser igual ao campo `sha256_zip` do `manifesto.json`.
4. Extraia o zip (botão direito → Extrair tudo) numa pasta sua e execute `AURALIS.exe`.

Para instalar a partir de um espelho/rede local use `AURALIS-Setup.exe /BASEURL=http://servidor/pasta/` (a pasta deve ter `latest.json` e `dados/`).

## Desinstalar

Configurações → Aplicativos → Aplicativos instalados → **AURALIS: The Pale Curse** → Desinstalar
(ou o atalho *Desinstalar AURALIS* no Menu Iniciar). Seus saves em `%APPDATA%\Godot\app_userdata\AURALIS- The Pale Curse` são mantidos; apague essa pasta se quiser removê-los.

## Problemas comuns

| Sintoma | O que fazer |
|---|---|
| Aviso azul do SmartScreen | Mais informações → Executar assim mesmo (veja acima) |
| "Não foi possível consultar o servidor" | Verifique internet, proxy e firewall; clique em *Tentar novamente* |
| Falha de rede no meio do download | Execute o instalador de novo; partes já verificadas não são baixadas outra vez |
| "A verificação SHA-256 falhou" | Execute de novo; se persistir, baixe o instalador de novo e confira o hash. Nada é instalado com dados inválidos |
| "Arquivo em uso" | Feche o AURALIS e tente novamente |
| Espaço insuficiente | O instalador usa a pasta temporária (cerca de 2x o download) e a pasta do jogo; libere espaço |
| Antivírus bloqueia o PowerShell | O download usa o PowerShell do Windows; permita a execução ou use a instalação manual |
| Tela preta/erro gráfico ao abrir o jogo | Atualize o driver da placa de vídeo |

## Créditos

Jogo, história, design, texto e direção: **Bruno Assunção Dias**.
Arte e código com apoio de IA, sob direção do autor. Engine: [Godot](https://godotengine.org/) (licença MIT).
Fonte Gelasio (OFL). Autor: [github.com/bruno-a-dias](https://github.com/bruno-a-dias) · [uiclap.bio/badmask_84](https://uiclap.bio/badmask_84)

## Licença e uso

© 2026 Bruno Assunção Dias. **Todos os direitos reservados.** AURALIS: The Pale Curse, seu código, arte, textos, vozes e músicas
pertencem ao autor. Fica permitido **jogar e distribuir o instalador (`AURALIS-Setup.exe`) sem modificações**, gratuitamente.
Não é permitido modificar, revender, redistribuir separadamente os dados do jogo, nem usar o material em outros projetos sem autorização por escrito.
O Godot Engine é distribuído sob licença MIT.

---

<a id="english"></a>

# AURALIS: The Pale Curse (English)

> A dark action-exploration metroidvania by **Bruno Assunção Dias**.
> Current version: **0.99.x** (pre-release) · Engine: Godot 4.3
> Play the web version: **https://auralisgame.vercel.app/**

## What it is

A pale curse covers the realm and only Auralis can face it. AURALIS is a dark 2D metroidvania: explore caves and ruins,
fight bosses, unlock abilities and uncover secrets that change the story.

### Key features

- **10 stages** with **named bosses**
- **Skill tree** to build your own fighting style
- **Parry**: block with the right timing, then counter-attack
- **Wells and secrets** hidden across the map
- **Two endings**
- **Voice acting in Portuguese and English**
- **Subtitles in 8 languages** (coming soon)

### Basic controls

A/D or arrows: move · Space or W: jump · J, X or Z: attack · P: pause · Esc: menu · M: minimap.
Keys can be remapped in Options → Controls. Gamepad is supported.

## Development notes

AURALIS is made by Bruno with **AI assistance for art and code**. Built with **Godot 4.3** (GDScript) plus Python helper tools.
The game is under active development: expect some bugs.

## Requirements

- Windows 10 or 11, **64-bit**
- A GPU with OpenGL 3.3 support (Godot compatibility renderer)
- About **170 MB download** and **250 MB free** disk space
- Internet only for installing (the game runs offline)
- No administrator rights needed: installs for your user only

## How to install (step by step)

1. Download the installer: **[releases/AURALIS-Setup.exe](releases/AURALIS-Setup.exe)** (*Download raw file* on the file page).
2. (Recommended) Check its SHA-256, see [Verifying the installer](#verifying-the-installer).
3. Run `AURALIS-Setup.exe`. If the blue SmartScreen screen appears, see [Blue Windows warning](#blue-windows-warning-smartscreen).
4. Pick the language (Português or English) and click **Next**.
5. On the **authorization** page, read where the files are downloaded from and how big they are, tick **"I authorize downloading the game files"** and continue. Without it, the installation does not proceed.
6. Choose the folder (default `%LOCALAPPDATA%\Programs\AURALIS`) and shortcuts (Start Menu and/or Desktop).
7. Wait: the installer downloads the parts, verifies the SHA-256 of each part and of the whole package, joins, unpacks and installs.
   If the connection drops it retries 3 times per part; when you run it again, parts already downloaded and verified are reused.
8. Tick **Run AURALIS** and click **Finish**.

Silent install (automation): `AURALIS-Setup.exe /S /ACCEPT` (optional: `/D=C:\Folder`, `/LANG=en`). `/ACCEPT` means you authorize the download.

### Blue Windows warning (SmartScreen)

Until the installer is **digitally signed**, Windows shows "Windows protected your PC". This happens to any program from an
independent author that has no reputation yet; it does not mean there is malware. Signing requires a paid code-signing certificate
with identity verification; the installer is not signed yet. To proceed click **More info**, then **Run anyway**.

### Verifying the installer

The official SHA-256 is in [releases/SHA256.txt](releases/SHA256.txt). In PowerShell, in the download folder:

```powershell
Get-FileHash .\AURALIS-Setup.exe -Algorithm SHA256
```

(or in Command Prompt: `certutil -hashfile AURALIS-Setup.exe SHA256`). The result must match the file.

### Manual / offline install (alternative)

1. Download from [dados/](dados/) every `AURALIS-<version>.partNNN.<hash>` file and `manifesto.json`.
2. In Command Prompt, in that folder, join the parts in order: `copy /b AURALIS-*.part* AURALIS.zip`
3. Check: `certutil -hashfile AURALIS.zip SHA256` must equal `sha256_zip` in `manifesto.json`.
4. Extract the zip (right-click → Extract all) to a folder of your own and run `AURALIS.exe`.

To install from a mirror/local network use `AURALIS-Setup.exe /BASEURL=http://server/folder/` (the folder must contain `latest.json` and `dados/`).

## Uninstall

Settings → Apps → Installed apps → **AURALIS: The Pale Curse** → Uninstall (or the *Uninstall AURALIS* Start Menu shortcut).
Your saves in `%APPDATA%\Godot\app_userdata\AURALIS- The Pale Curse` are kept; delete that folder to remove them.

## Troubleshooting

| Symptom | What to do |
|---|---|
| Blue SmartScreen warning | More info → Run anyway (see above) |
| "Could not reach the server" | Check internet, proxy and firewall; click *Try again* |
| Network failure mid-download | Run the installer again; verified parts are not downloaded twice |
| "SHA-256 verification failed" | Run again; if it persists, re-download the installer and check its hash. Nothing is installed with invalid data |
| "File in use" | Close AURALIS and try again |
| Not enough space | The installer uses the temp folder (about 2x the download) and the game folder; free some space |
| Antivirus blocks PowerShell | The download uses Windows PowerShell; allow it or use the manual install |
| Black screen / graphics error | Update your graphics driver |

## Credits

Game, story, design, writing and direction: **Bruno Assunção Dias**. Art and code made with AI assistance under the author's direction.
Engine: [Godot](https://godotengine.org/) (MIT). Font Gelasio (OFL).
Author: [github.com/bruno-a-dias](https://github.com/bruno-a-dias) · [uiclap.bio/badmask_84](https://uiclap.bio/badmask_84)

## License and use

© 2026 Bruno Assunção Dias. **All rights reserved.** AURALIS: The Pale Curse, its code, art, text, voices and music belong to the author.
You may **play and distribute the unmodified installer (`AURALIS-Setup.exe`)** free of charge. Modifying, reselling, redistributing the game data separately,
or reusing the material in other projects requires written permission. Godot Engine is distributed under the MIT license.
