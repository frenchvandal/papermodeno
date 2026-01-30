---
title: "FAQ / Guide pratique"
summary: Nous tentons de répondre aux questions fréquemment posées par les utilisateurs.
date: 2021-01-20
aliases: ['/papermod-how-to-guide', '/posts/papermod/papermod-how-to']
tags: ["PaperMod", "Docs"]
author: ["PaperMod Contributors"]
draft: true
weight: 3
---

> - **Tous les exemples ci-dessous utilisent le format `yml/yaml`. Il est recommandé d’utiliser `yml` plutôt que `toml`, car il est plus lisible.**
>
> - Vous pouvez trouver des convertisseurs [YML vers TOML](https://www.google.com/search?q=yml+to+toml) si nécessaire.

---

## Surcharger un template du thème

Grâce à l’ordre de recherche de Hugo, vous pouvez surcharger n’importe quelle partie d’un thème. Voici un exemple simple.

Supposons que vous souhaitiez modifier le template `list`. Il vous suffit de copier le template `list` :

```shell
your-site/themes/papermod/layouts/_defaults/list.html
```

et de le coller dans votre propre dossier `layouts` :

```shell
your-site/layouts/_defaults/list.html
```

Vous êtes alors libre d’apporter toutes les modifications souhaitées au fichier `list`.
Lors de la génération du site, Hugo utilisera votre version de `list.html` à la place de celle du thème.

---

## Activer les métadonnées sociales et le SEO

Cela inclut OpenGraph, Twitter Cards et Schema.

```yml {linenos=true}
params:
  env: production
```

ou définissez `HUGO_ENV` sur « production » dans les variables d’environnement du système.

---

## Impossible de trouver une empreinte valide dans l’attribut « integrity » pour la ressource… ?

Découvrez le rôle de Subresource Integrity : [Subresource_Integrity](https://developer.mozilla.org/en-US/docs/Web/Security/Subresource_Integrity)

Pourquoi la ressource `asset` ne se charge-t-elle pas ? : [Fonctionnement de Subresource Integrity dans les navigateurs](https://developer.mozilla.org/en-US/docs/Web/Security/Subresource_Integrity#How_browsers_handle_Subresource_Integrity)

**Solution :**

Ajoutez la configuration suivante dans `hugo.yaml` :

```yml {linenos=true}
params:
  assets:
    disableFingerprinting: true
```

Problèmes liés :

- https://stackoverflow.com/questions/65056585/hugo-theme-not-loading
- https://stackoverflow.com/questions/65040931/hugo-failed-to-find-a-valid-digest-in-the-integrity-attribute-for-resource
- https://blog.gerardbeckerleg.com/posts/hugo-failed-to-find-a-valid-digest-in-the-integrity-attribute-for-resource/

---

## Regrouper du CSS personnalisé avec les ressources du thème

- Pour ajouter du CSS personnalisé et le regrouper dans un seul fichier CSS minifié

Créez la structure suivante dans votre projet :

```
.(racine du site)
├── hugo.yaml
├── content/
├── theme/hugo-PaperMod/
└── assets/
    └── css/
        └── extended/
            ├── custom_css1.css
            └── autre_nom.css
```

Tous les fichiers `css` placés dans `assets/css/extended` seront regroupés.

**Note :** `blank.css` sert uniquement de fichier de substitution afin d’éviter les erreurs lorsque le dossier `assets/css/extended` est vide.

Problèmes liés :

- [Papermod Theme: How to add custom CSS?](https://discourse.gohugo.io/t/papermod-theme-how-to-add-custom-css/30165)

---

## En-tête / pied de page personnalisés

Du CSS ou du JavaScript personnalisés peuvent être ajoutés de la manière suivante :

```
.(racine du site)
├── hugo.yaml
├── content/
├── theme/hugo-PaperMod/
└── layouts
    ├── partials
    │   ├── comments.html
    │   ├── extend_footer.html
    │   └── extend_head.html
    └── robots.txt
```

Créez les fichiers HTML selon la structure ci-dessus.

Le contenu de `extend_head.html` sera ajouté dans la balise `head` de la page.

Le contenu de `extend_footer.html` sera ajouté en bas de la page.

---

## Ajouter un menu au site

Vous pouvez ajouter des entrées de menu qui apparaîtront dans l’en-tête de chaque page.

Ajoutez pour cela une section `menu` dans le fichier `hugo.yaml` :

```yml {linenos=true}
menu:
  main:
    - identifier: categories
      name: categories
      url: /categories/
      weight: 10
    - identifier: tags
      name: tags
      url: /tags/
      weight: 20
    - identifier: example
      name: example.org
      url: https://example.org
      weight: 30
```

`name` définit le texte affiché dans le menu.  
`url` définit l’URL de destination.  
`weight` permet de contrôler l’ordre d’affichage.

Pour plus d’informations, consultez la [documentation Hugo sur les menus](https://gohugo.io/content-management/menus/).

---

## Épingler un article

Un article peut être épinglé (affiché en haut de la liste) en ajoutant une variable `weight=<num>` dans les paramètres de la page.

Exemple :

```yml {linenos=true}
---
title: "Mon article important"
date: 2020-09-15T11:30:03+00:00
weight: 1
---
```

```yml {linenos=true}
---
title: "Mon deuxième article important"
date: 2020-09-15T11:30:03+00:00
weight: 2
---
```

---

## Ajouter des favicons personnalisés

Les chemins suivants sont pris en charge dans le dossier `/static` :

- `favicon.ico`
- `favicon-16x16.png`
- `favicon-32x32.png`
- `apple-touch-icon.png`
- `safari-pinned-tab.svg`

1. Les favicons peuvent être générés via [Favicon.io](https://favicon.io) puis placés directement dans le dossier `/static`.

2. Il est également possible d’utiliser des favicons situés hors du dossier `/static`.

   Ajoutez alors la configuration suivante :

   ```yml {linenos=true}
   params:
     assets:
       favicon: "<lien / url absolue>"
       favicon16x16: "<lien / url absolue>"
       favicon32x32: "<lien / url absolue>"
       apple_touch_icon: "<lien / url absolue>"
       safari_pinned_tab: "<lien / url absolue>"
   ```

   Remarque : une URL absolue correspond à un lien direct vers une ressource externe, par exemple `https://site.web/image.png`.

```yml {linenos=true}
params:
  assets:
    favicon: "/favicon.ico"
    favicon16x16: "/favicon-16x16.png"
    favicon32x32: "/favicon-32x32.png"
    apple_touch_icon: "/apple-touch-icon.png"
    safari_pinned_tab: "/safari-pinned-tab.svg"
```

---

## Centrer une image en Markdown

Ajoutez `#center` après l’image pour la centrer.

```md {linenos=true}
![nom](chemin/vers/image.png#center)
```

**Avec le shortcode [`figure`](https://gohugo.io/content-management/shortcodes/)**

Utilisez `align=center` pour centrer l’image avec une légende :

```md {linenos=true}
{{</* figure align=center src="image.jpg" */>}}
```

---

## Utiliser le surligneur syntaxique « chroma » de Hugo

1. Désactivez Highlight.js dans `hugo.yaml` :

   ```yml {linenos=true}
   params:
     assets:
       disableHLJS: true
   ```

2. Configurez la mise en forme Markdown dans `hugo.yaml` :

   ```yml {linenos=true}
   markup:
     highlight:
       codeFences: true
       guessSyntax: true
       lineNos: true
       style: monokai
   ```

3. Si `lineNos: true` est activé, l’arrière-plan peut ne pas être correct.
   Cela fonctionne uniquement avec `noClasses: false` ou `pygmentsUseClasses: true`.
   Consultez [Générer le CSS du surligneur syntaxique](https://gohugo.io/content-management/syntax-highlighting/#generate-syntax-highlighter-css).

   Ajoutez ensuite dans `assets/css/extended/custom.css` :

   ```css {linenos=true}
   .chroma {
     background-color: unset;
   }
   ```

   Plus d’informations : [Configurer Markup – Highlight](https://gohugo.io/getting-started/configuration-markup#highlight)

---

## La recherche ne fonctionne pas ?

Si vous utilisez un CDN pour servir les ressources depuis un autre domaine, la recherche peut cesser de fonctionner.

Pourquoi ? Voir [fastsearch.js#L35](https://github.com/adityatelange/hugo-PaperMod/blob/fb4988cfb6d0d6e4e489f17d89f0fa618def3396/assets/js/fastsearch.js#L35).

Le fichier `index.json` est récupéré un niveau au-dessus de l’emplacement où `search.min.js` est hébergé.
Cette approche permet de gérer les sites multilingues (ex. `example.com/fr/`) ou les sites placés dans un sous-répertoire (ex. `example.com/blog/`).

Pour corriger cela sur un site monolingue utilisant un CDN, vous pouvez [surcharger le template](#surcharger-un-template-du-thème) et modifier `fastsearch.js` comme suit :

```js {linenos=true}
xhr.open("GET", "https://example.com/index.json");
```

---

## Références

- [Surcharger un thème Hugo](https://zwbetz.com/override-a-hugo-theme/)
