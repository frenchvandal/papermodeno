---
title: "Fonctionnalités / Modules"
summary: Découvrir toutes les fonctionnalités de PaperMod
date: 2021-01-20
weight: 2
aliases: ["/papermod-features"]
tags: ["PaperMod", "Docs"]
author: ["Aditya Telange"]
social:
  fediverse_creator: "@adityatelange@mastodon.social"
---

### Introduction

- **Tous les exemples ci-dessous utilisent le format `yml/yaml`. Il est recommandé d’utiliser `yml` plutôt que `toml`, car il est plus lisible.**
- Vous pouvez trouver des convertisseurs [YML vers TOML](https://www.google.com/search?q=yml+to+toml) si nécessaire.

---

### Ressources (js/css)

Les éléments suivants sont activés par défaut :

- [minification](https://gohugo.io/hugo-pipes/minification/) — réduit la taille des ressources au minimum
- [bundling](https://gohugo.io/hugo-pipes/bundling/) — regroupe toutes les feuilles de style en une seule ressource
- [fingerprint / integrity](https://gohugo.io/hugo-pipes/fingerprint/) — vérification d’intégrité

---

### Thème par défaut light / dark / auto

```yml {linenos=true}
params:
  # defaultTheme: light
  # defaultTheme: dark
  defaultTheme: auto # bascule automatique selon le thème du navigateur
```

---

### Bouton de changement de thème (activé par défaut)

Affiche une icône à côté du titre de la page pour changer de thème.

Pour le désactiver :

```yml {linenos=true}
disableThemeToggle: true
```

Tableau récapitulatif :

| `defaultTheme` | `disableThemeToggle` | stockage local | thème système | Information        |
| -------------- | -------------------- | -------------- | ------------- | ------------------ |
| `auto`         | true                 | Non            | Oui           | thème système seul |
|                | false                | Oui            | Oui           | _commutateur actif_ |
| `dark`         | true                 | Non            | Non           | forcer sombre      |
|                | false                | Oui            | Non           | _commutateur actif_ |
| `light`        | true                 | Non            | Non           | forcer clair       |
|                | false                | Oui            | Non           | _commutateur actif_ |

---

### Mise en page Archives

Créez un fichier `archives.md` dans le dossier `content` :

```shell
.
├── hugo.yaml
├── content/
│   ├── archives.md
│   └── posts/
├── static/
└── themes/
    └── PaperMod/
```

Ajoutez ensuite :

```yml
---
title: "Archive"
layout: "archives"
url: "/archives/"
summary: archives
---
```

**Remarque :** la mise en page Archives ne prend pas en charge la traduction multilingue des mois.

---

### Mode normal (par défaut)

![regular](images/regular.jpg)

---

### Mode Home-Info

![homeinfo](images/homeinfo.jpg)

Utilise la première entrée comme zone d’information.

```yml
params:
  homeInfoParams:
    Title: Bonjour
    Content: Informations, liens, présentation…
```

---

### Mode Profil

Affiche la page d’accueil comme une page pleine avec image et liens sociaux.

```yml {linenos=true}
params:
  profileMode:
    enabled: true
    title: "<Titre>"
    subtitle: "Sous-titre"
    imageUrl: "<lien image>"
    imageTitle: "<texte alternatif>"
    imageWidth: 120
    imageHeight: 120
    buttons:
      - name: Archive
        url: "/archive"
      - name: Github
        url: "https://github.com/"
```

---

### Page de recherche

PaperMod utilise [Fuse.js Basic](https://fusejs.io/getting-started/different-builds.html#explanation-of-different-builds).

Activation dans `hugo.yaml` :

```yml {linenos=true,hl_lines=[5]}
outputs:
  home:
    - HTML
    - RSS
    - JSON
```

Création du fichier `search.md` :

```yml
---
title: "Recherche"
layout: "search"
summary: "search"
placeholder: "texte indicatif"
---
```

Masquer une page de la recherche :

```yml
searchHidden: true
```

---

### Indication des brouillons

Ajoute la mention `[draft]` aux pages en brouillon.

---

### Image de couverture des articles

```yml
cover:
  image: "<chemin ou URL>"
  alt: "<texte alternatif>"
  caption: "<légende>"
  relative: false
```

---

### Boutons de partage

```yml
params:
  ShowShareButtons: true
```

---

### Temps de lecture

```yml
params:
  ShowReadingTime: true
```

---

### Table des matières

```yml
ShowToc: true
TocOpen: true
```

---

### Fil d’Ariane

```yml
params:
  ShowBreadCrumbs: true
```

---

### Lien d’édition des articles

```yml
params:
  editPost:
    URL: "https://github.com/<depot>/content"
    Text: "Suggérer des modifications"
    appendFilePath: true
```

---

### Navigation Article précédent / suivant

```yml
params:
  ShowPostNavLinks: true
```

---

### Bouton de copie du code

```yml
params:
  ShowCodeCopyButtons: true
```

---

### Auteurs multiples

```yml
author: ["Moi", "Toi"]
```

---

### Commentaires

```yml
params:
  comments: true
```

---

### Raccourcis clavier

```text
c — ouvrir/fermer la table des matières
g — retour en haut
h — accueil
t — changement de thème
/ — recherche
```

---

### SEO avancé

Activé uniquement lorsque `env: production`.

- Rich snippets
- Twitter Cards
- OpenGraph

---

### Multilingue

Pris en charge nativement.

---

### Divers

- Barre de défilement stylisée
- Défilement fluide
- Bouton retour en haut
- Google Analytics
- Surlignage syntaxique
- Flux RSS
