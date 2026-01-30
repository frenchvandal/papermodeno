---
title: "Installer / Mettre à jour PaperMod"
summary: Lire les instructions d’installation et de mise à jour ainsi que des exemples de configuration
date: 2021-01-20
weight: 1
aliases: ["/papermod-installation"]
tags: ["PaperMod", "Docs"]
author: ["Aditya Telange"]
cover:
  image: images/papermod-cover.png
  hiddenInList: true
social:
  fediverse_creator: "@adityatelange@mastodon.social"
---

> - **Tous les exemples ci-dessous utilisent le format `yml/yaml`. Il est recommandé d’utiliser `yaml` plutôt que `toml`, car il est plus lisible.**
> - Vous pouvez trouver des convertisseurs [YML vers TOML](https://www.google.com/search?q=yml+to+toml) si nécessaire.

---

## Bien démarrer 🚀

1. Suivez le guide **[Hugo Docs – Démarrage rapide](https://gohugo.io/getting-started/quick-start/)** pour installer {{< inTextImg url="https://raw.githubusercontent.com/gohugoio/hugoDocs/master/static/img/hugo-logo.png" height="14" >}}.
   <br>(Assurez-vous d’installer **Hugo >= v0.112.4**)

2. Créez un nouveau site {{< inTextImg url="https://raw.githubusercontent.com/gohugoio/hugoDocs/master/static/img/hugo-logo.png" height="14" >}}
   ```sh
   hugo new site MyFreshWebsite --format yaml
   # remplacez MyFreshWebsite par le nom de votre site
   ```
   Remarque :
   - Les versions plus anciennes de Hugo peuvent ne pas prendre en charge `--format yaml`
   - Pour plus d’informations, consultez [Hugo Docs – commande hugo new site](https://gohugo.io/commands/hugo_new_site/#synopsis)

Après avoir créé un nouveau site, suivez les étapes ci-dessous pour ajouter **PaperMod**.

### Installer / Mettre à jour PaperMod

- Les thèmes se trouvent dans le dossier `MyFreshWebsite/themes`.
- PaperMod sera installé dans `MyFreshWebsite/themes/PaperMod`.

> {{< collapse summary="**Afficher la méthode 1 – Git Clone**" >}}

**INSTALLATION** : Dans le dossier de votre site Hugo `MyFreshWebsite`, exécutez :

```bash
git clone https://github.com/adityatelange/hugo-PaperMod themes/PaperMod --depth=1
```

Vous pouvez ajouter ` --branch v7.0` à la fin de la commande ci-dessus si vous souhaitez rester sur une version spécifique.

**MISE À JOUR** : Dans le dossier de votre site Hugo `MyFreshWebsite`, exécutez :

```bash
cd themes/PaperMod
git pull
```

{{</ collapse >}}

> {{< collapse summary="**Afficher la méthode 2 – Git Submodule (recommandée)**" >}}

**INSTALLATION** : Dans le dossier de votre site Hugo `MyFreshWebsite`, exécutez :

```bash
git submodule add --depth=1 https://github.com/adityatelange/hugo-PaperMod.git themes/PaperMod
git submodule update --init --recursive # nécessaire lorsque vous re-clonez votre dépôt (les submodules peuvent ne pas être clonés automatiquement)
```

Vous pouvez ajouter ` --branch v7.0` à la fin de la commande ci-dessus si vous souhaitez rester sur une version spécifique.  
Pour en savoir plus sur les submodules Git, consultez la documentation [ici](https://www.atlassian.com/git/tutorials/git-submodule).

**MISE À JOUR** : Dans le dossier de votre site Hugo `MyFreshWebsite`, exécutez :

```bash
git submodule update --remote --merge
```

{{</ collapse >}}

> {{< collapse summary="**Afficher la méthode 3 – Télécharger une archive ZIP**" >}}

Téléchargez le code source de PaperMod au format ZIP depuis les versions GitHub, puis extrayez-le dans le dossier `MyFreshWebsite/themes/PaperMod`.

Liens directs :

- [Branche master (dernière version)](https://github.com/adityatelange/hugo-PaperMod/archive/master.zip)
- [v7.0](https://github.com/adityatelange/hugo-PaperMod/archive/v7.0.zip)
- [v6.0](https://github.com/adityatelange/hugo-PaperMod/archive/v6.0.zip)
- [v5.0](https://github.com/adityatelange/hugo-PaperMod/archive/v5.0.zip)
- [v4.0](https://github.com/adityatelange/hugo-PaperMod/archive/v4.0.zip)
- [v3.0](https://github.com/adityatelange/hugo-PaperMod/archive/v3.0.zip)
- [v2.0](https://github.com/adityatelange/hugo-PaperMod/archive/v2.0.zip)
- [v1.0](https://github.com/adityatelange/hugo-PaperMod/archive/v1.0.zip)

{{</ collapse >}}

> {{< collapse summary="**Afficher la méthode 4 – Module Hugo**" >}}

**INSTALLATION** :

- Installez le [langage de programmation Go](https://go.dev/doc/install) sur votre système.

- Initialisez votre propre module Hugo :

```
hugo mod init VOTRE_DEPOT_GIT
```

- Ajoutez PaperMod dans votre fichier `hugo.yaml` :

```go {linenos=true}
module:
  imports:
  - path: github.com/adityatelange/hugo-PaperMod
```

**MISE À JOUR** :

```
hugo mod get -u
```

Pour en savoir plus : [Hugo Docs – Modules Hugo](https://gohugo.io/hugo-modules/use-modules/)

{{</ collapse >}}

### Définir PaperMod comme thème de votre site

Dans `hugo.yaml`, ajoutez :

```yml {linenos=true}
theme: ["PaperMod"]
```

### Étape suivante – Personnaliser PaperMod selon vos préférences

- Votre site sera vide lors de la première configuration.
- Vous pouvez consulter le code source de ce site : [exempleSite de PaperMod](https://github.com/adityatelange/hugo-PaperMod/tree/exampleSite)
- Faites défiler cette page pour trouver des informations détaillées sur chaque section.
- Parcourez l’ensemble des pages suivantes afin de comprendre comment configurer PaperMod.

---

## Support 🫶

- Ajoutez une étoile 🌟 au dépôt GitHub de PaperMod.
- Aidez à faire connaître PaperMod en le partageant sur les réseaux sociaux et en le recommandant à vos proches. 🗣️
- Vous pouvez également soutenir le projet via [GitHub Sponsors](https://github.com/sponsors/adityatelange) ou [Ko-Fi](https://ko-fi.com/adityatelange).

---

## Vidéos présentant PaperMod

Vous pouvez consulter plusieurs vidéos disponibles sur YouTube pour découvrir la vision du créateur ainsi que le processus d’installation.

▶️ https://youtube.com/playlist?list=PLeiDFxcsdhUrzkK5Jg9IZyiTsIMvXxKZP

---

## Liens rapides

- ### [PaperMod – Fonctionnalités](../papermod-features)
- ### [PaperMod – FAQ](../papermod-how-to)
- ### [PaperMod – Variables](../papermod-variables)
- ### [PaperMod – Icônes](../papermod-icons)
- ### [Journal des versions](https://github.com/adityatelange/hugo-PaperMod/releases)

---

## Exemple de `hugo.yaml`

> **La structure de l’exemple de site est disponible ici** : [exampleSite](https://github.com/adityatelange/hugo-PaperMod/tree/exampleSite/)

**À utiliser de manière appropriée**

```yml
baseURL: "https://examplesite.com/"
title: ExampleSite
paginate: 5
theme: PaperMod

enableRobotsTXT: true
buildDrafts: false
buildFuture: false
buildExpired: false

googleAnalytics: UA-123-45

minify:
  disableXML: true
  minifyOutput: true

params:
  env: production
  title: ExampleSite
  description: "Description de ExampleSite"
  keywords: [Blog, Portfolio, PaperMod]
  author: Me
  images: ["<lien ou chemin de l’image pour opengraph, twitter-cards>"]
  DateFormat: "January 2, 2006"
  defaultTheme: auto
  disableThemeToggle: false

  ShowReadingTime: true
  ShowShareButtons: true
  ShowPostNavLinks: true
  ShowBreadCrumbs: true
  ShowCodeCopyButtons: false
  ShowWordCount: true
  ShowRssButtonInSectionTermList: true
  UseHugoToc: true
  disableSpecial1stPost: false
  disableScrollToTop: false
  comments: false
  hidemeta: false
  hideSummary: false
  showtoc: false
  tocopen: false

  assets:
    favicon: "<lien / url absolue>"
    favicon16x16: "<lien / url absolue>"
    favicon32x32: "<lien / url absolue>"
    apple_touch_icon: "<lien / url absolue>"
    safari_pinned_tab: "<lien / url absolue>"

  label:
    text: "Home"
    icon: /apple-touch-icon.png
    iconHeight: 35
```
