![Node build](https://github.com/eritislami/evobot/actions/workflows/node.yml/badge.svg)
![Docker build](https://github.com/eritislami/evobot/actions/workflows/docker.yml/badge.svg)
[![Commitizen friendly](https://img.shields.io/badge/commitizen-friendly-brightgreen.svg)](http://commitizen.github.io/cz-cli/)

![logo](https://repository-images.githubusercontent.com/186841818/8aa95700-7730-11e9-84be-e80f28520325)

# 🤖 DJSteven (Bot de Discord de musica)
> Steven es un Discord Music Bot construido con discord.js y usa Command Handler de [discordjs.guide](https://discordjs.guide)

## Requirements

1. Discord Bot Token **[Guide](https://discordjs.guide/preparations/setting-up-a-bot-application.html#creating-your-bot)**
2. YouTube Data API v3 Key **[Guide](https://developers.google.com/youtube/v3/getting-started)**  
2.1 **(Optional)** Soundcloud Client ID **[Guide](https://github.com/zackradisic/node-soundcloud-downloader#client-id)**
3. Node.js v14.0.0 o nueva

## 🚀 Comenzando

```sh
git clone https://github.com/eritislami/evobot.git
cd evobot
npm install
```

Una vez finalizada la instalación, siga las instrucciones de configuración y luego ejecute `node index.js` para iniciar el bot.

## ⚙️ Configuracion

Copy o Rename `config.json.example` to `config.json` y complete los valores:

⚠️ **Note: Nunca comprometa ni comparta públicamente sus claves de token o API** ⚠️

```json
{
  "TOKEN": "",
  "YOUTUBE_API_KEY": "",
  "SOUNDCLOUD_CLIENT_ID": "",
  "MAX_PLAYLIST_SIZE": 10,
  "PREFIX": "/",
  "PRUNING": false,
  "LOCALE": "en",
  "DEFAULT_VOLUME": 100,
  "STAY_TIME": 30
}
```

## 🐬 Docker Configuracion

Para aquellos que prefieren usar nuestro [Docker container](https://hub.docker.com/repository/docker/eritislami/evobot), puede proporcionar valores de `config.json` como variables de entorno.

```shell
docker run -e "TOKEN=<discord-token>" -e "YOUTUBE_API_KEY=<youtube-key>" eritislami/evobot
```

## 📝 Funciones y comandos

> Npta: El prefix por default es '/'

* 🎶 Play music por YouTube via url

`/play https://www.youtube.com/watch?v=GLvohMXgcBo`

* 🔎 Play music por YouTube via search query

`/play under the bridge red hot chili peppers`

* 🎶 Play music por Soundcloud via url

`/play https://soundcloud.com/blackhorsebrigade/pearl-jam-alive`

* 🔎 Search and select music to play

`/search Pearl Jam`

Responda con el número de la canción o los números separados por comas que desea reproducir
Examples: `1` or `1,2,3`

* 📃 Play youtube playlists via url

`/playlist https://www.youtube.com/watch?v=YlUKcNNmywk&list=PL5RNCwK3GIO13SR_o57bGJCEmqFAwq82c`

* 🔎 Play youtube playlists via search query

`/playlist linkin park meteora`
* Now Playing (/np)
* Queue system (/queue, /q)
* Loop / Repeat (/loop)
* Shuffle (/shuffle)
* Volume control (/volume, /v)
* Lyrics (/lyrics, /ly)
* Pause (/pause)
* Resume (/resume, /r)
* Skip (/skip, /s)
* Skip to song # in queue (/skipto, /st)
* Move a song in the queue (/move, /mv)
* Remove song # from queue (/remove, /rm)
* Play an mp3 clip (/clip song.mp3) (poner el archivo en la carpeta de sonidos)
* List all clips (/clips)
* Show ping to Discord API (/ping)
* Show bot uptime (/uptime)
* Toggle pruning of bot messages (/pruning)
* Help (/help, /h)
* Command Handler from [discordjs.guide](https://discordjs.guide/)
* Controles de medios a través de reacciones

![reactions](https://i.imgur.com/9S7Omf9.png)

## 🌎 Locales

Currently available locales are:
- English (en)
- Arabic (ar)
- Brazilian Portuguese (pt_br)
- Dutch (nl)
- French (fr)
- German (de)
- Greek (el)
- Indonesian (id)
- Italian (it)
- Japanese (ja)
- Korean (ko)
- Polish (pl)
- Russian (ru)
- Simplified Chinese (zh_cn)
- Singaporean Mandarin (zh_sg)
- Spanish (es)
- Swedish (sv)
- Traditional Chinese (zh_tw)
- Thai (th)
- Turkish (tr)
- Ukrainian (uk)
- Vietnamese (vi)
- Check [Contributing](#-contributing) if you wish to help add more languages!
- For languages please use [ISO 639-1](https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes) two letter format

## 🤝 Contributing

1. [Fork the repository](https://github.com/eritislami/evobot/fork)
2. Clone your fork: `git clone https://github.com/your-username/evobot.git`
3. Create your feature branch: `git checkout -b my-new-feature`
4. Stage changes `git add .`
5. Commit your changes: `cz` OR `npm run commit` do not use `git commit`
6. Push to the branch: `git push origin my-new-feature`
7. Submit a pull request

## 📝 Creditos

[@iCrawl](https://github.com/iCrawl) Para el sistema de colas utilizado en esta aplicación, que fue adaptado de [@iCrawl/discord-music-bot](https://github.com/iCrawl/discord-music-bot)
