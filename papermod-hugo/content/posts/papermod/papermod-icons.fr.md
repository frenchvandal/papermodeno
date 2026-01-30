---
title: "Icônes sociales / Icônes de partage"
summary: Liste de toutes les icônes prises en charge par PaperMod
date: 2021-01-20
weight: 4
aliases: ["/papermod-icons"]
tags: ["PaperMod", "Docs"]
author: ["Aditya Telange"]
draft: true
social:
  fediverse_creator: "@adityatelange@mastodon.social"
---

## Icônes sociales

| Nom             | Lien de la plateforme            |
| --------------- | -------------------------------- |
| `123rf`         | 123rf.com                        |
| `adobestock`    | stock.adobe.com                  |
| `applemusic`    | music.apple.com                  |
| `behance`       | behance.net                      |
| `bilibili`      | bilibili.com                     |
| `bitcoin`       | -                                |
| `buymeacoffee`  | buymeacoffee.com                 |
| `codepen`       | codepen.io                       |
| `cryptohack`    | cryptohack.org                   |
| `ctftime`       | ctftime.org                      |
| `cv`            | -                                |
| `deezer`        | deezer.com                       |
| `dev`           | dev.to                           |
| `discogs`       | discogs.com                      |
| `discord`       | discord.com                      |
| `dreamstime`    | dreamstime.com                   |
| `dribbble`      | dribbble.com                     |
| `email`         | -                                |
| `facebook`      | facebook.com                     |
| `flickr`        | flickr.com                       |
| `freepik`       | freepik.com                      |
| `gitea`         | gitea.io                         |
| `github`        | github.com                       |
| `gitlab`        | gitlab.com                       |
| `goodreads`     | goodreads.com                    |
| `googlescholar` | scholar.google.com               |
| `guruShots`     | gurushots.com                    |
| `hackerone`     | hackerone.com                    |
| `hackerrank`    | hackerrank.com                   |
| `hackthebox`    | hackthebox.eu                    |
| `instagram`     | instagram.com                    |
| `itchio`        | itch.io                          |
| `kaggle`        | -                                |
| `kakaotalk`     | kakaocorp.com/service/KakaoTalk  |
| `key`           | -                                |
| `keybase`       | keybase.io                       |
| `kofi`          | ko-fi.com                        |
| `komoot`        | -                                |
| `lastfm`        | last.fm                          |
| `letterboxd`    | -                                |
| `liberapay`     | liberapay.com                    |
| `linkedin`      | linkedin.com                     |
| `mastodon`      | mastodon.social                  |
| `matrix`        | matrix.org                       |
| `medium`        | medium.com                       |
| `monero`        | -                                |
| `mixcloud`      | mixcloud.com                     |
| `nostr`         | nostr.org                        |
| `nuget`         | nuget.org                        |
| `paypal`        | paypal.com                       |
| `peertube`      | -                                |
| `pgp`           | -                                |
| `phone`         | -                                |
| `ploywork`      | ploywork.com                     |
| `qq`            | qq.com                           |
| `reddit`        | reddit.com                       |
| `researchgate`  | researchgate.net                 |
| `rss`           | -                                |
| `serverfault`   | serverfault.com                  |
| `soundcloud`    | soundcloud.com                   |
| `shutterstock`  | shutterstock.com                 |
| `slack`         | slack.com                        |
| `snapchat`      | snapchat.com/add                 |
| `spotify`       | spotify.com                      |
| `stackoverflow` | stackoverflow.com                |
| `steam`         | steampowered.com                 |
| `strava`        | strava.com                       |
| `telegram`      | telegram.org                     |
| `tiktok`        | tiktok.com                       |
| `twitch`        | twitch.tv                        |
| `twitter`       | twitter.com                      |
| `unsplash`      | unsplash.com                     |
| `x`             | x.com                            |
| `xda`           | xda-developers.com               |
| `xing`          | xing.com                         |
| `ycombinator`   | ycombinator.com                  |
| `youtube`       | youtube.com                      |
| `zcal`          | zcal.co                          |
| `other`         | -                                |

Utilisation :

```yml {linenos=true}
socialIcons:
  - name: "kofi"
    url: "https://kofi.com"
  - name: "x"
    url: "https://x.com"
```

---

## Icônes de partage

| Plateforme                                                         |
| ------------------------------------------------------------------ |
| `x` (génère également des `#hashtags` à partir des _tags_ liés à l’article) |
| `linkedin`                                                         |
| `reddit`                                                           |
| `facebook`                                                         |
| `whatsapp`                                                         |
| `telegram`                                                         |

Utilisation :

```yml {linenos=true}
params:
  ShowShareButtons: true
```

```yml {linenos=true}
params:
  ShareButtons: ["linkedin", "twitter"] # Pour personnaliser les boutons de partage activés sur la page
```
