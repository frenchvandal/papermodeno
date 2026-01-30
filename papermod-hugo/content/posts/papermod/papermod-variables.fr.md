---
title: "Variables | Front Matter"
summary: Liste des variables de Front Matter utilisées par PaperMod
date: 2021-01-20
tags: ["PaperMod", "Docs"]
author: ["Aditya Telange"]
draft: true
weight: 5
social:
  fediverse_creator: "@adityatelange@mastodon.social"
---

**Ci-dessous figurent les variables utilisées par ce thème…**

---

### Variables du site sous `Params`

| nom                                    | type          | exemple                   | Description                                                                                 |
| -------------------------------------- | ------------- | ------------------------- | ------------------------------------------------------------------------------------------- |
| `env`                                  | string        | 'production'              | Définir l’environnement en production                                                      |
| `title`                                | string        | 'Mon blog'                | Définir le titre du site                                                                    |
| `description`                          | string        | 'Ceci est mon blog'       | Définir la description du site                                                             |
| `author`                               | string \| list| 'Moi' \| ['Moi','Toi']    | Afficher un ou plusieurs auteurs                                                           |
| `images`                               | string        | 'monimage.png'            | Lien ou chemin de l’image pour OpenGraph et Twitter Cards                                   |
| `keywords`                             | list          | [blog, page]              | Ajouter des mots-clés pour la page d’accueil                                                |
| `DateFormat`                           | string        | "January 2, 2006"         | Format des dates sur le site ([détails](https://gohugo.io/functions/format/))               |
| `languageAltTitle`                     | string        | "English"                 | Titre alternatif en mode multilingue                                                        |
| `ShowReadingTime`                      | boolean       | true \| false             | Afficher le temps de lecture dans les métadonnées                                           |
| `ShowShareButtons`                     | boolean       | true \| false             | Afficher / masquer les boutons de partage                                                   |
| `ShowCodeCopyButtons`                  | boolean       | true \| false             | Afficher / masquer le bouton de copie du code                                               |
| `ShowFullTextinRSS`                    | boolean       | true \| false             | Afficher le contenu complet dans le flux RSS                                                |
| `defaultTheme`                         | string        | light \| dark \| auto     | Définir le thème par défaut                                                                 |
| `disableThemeToggle`                   | boolean       | true \| false             | Désactiver l’icône de changement de thème                                                   |
| `disableSpecial1stPost`                | boolean       | true \| false             | Désactiver l’apparence spéciale du premier article                                          |
| `disableScrollToTop`                   | boolean       | true \| false             | Désactiver le bouton de retour en haut                                                      |
| `disableAnchoredHeadings`              | boolean       | true \| false             | Désactiver les titres ancrés                                                                |
| `hideMeta`                             | boolean       | true \| false             | Masquer les métadonnées (date, temps de lecture, auteur, traductions)                       |
| `hideSummary`                          | boolean       | true \| false             | Masquer le résumé dans les pages de liste                                                   |
| `showtoc`                              | boolean       | true \| false             | Afficher / masquer la table des matières                                                    |
| `tocopen`                              | boolean       | true \| false             | Garder la table des matières ouverte par défaut                                             |
| `ShowPostNavLinks`                     | boolean       | true \| false             | Afficher les liens Article précédent / suivant                                              |
| `ShowBreadCrumbs`                      | boolean       | true \| false             | Afficher le fil d’Ariane au-dessus des pages                                                |
| `ShareButtons`                         | list          | ["linkedin", "x"]         | Personnaliser les boutons de partage                                                        |
| `ShowWordCount`                        | boolean       | true \| false             | Afficher le nombre de mots                                                                 |
| `ShowRssButtonInSectionTermList`       | boolean       | true \| false             | Afficher l’icône RSS dans les pages de section et de liste                                  |
| `UseHugoToc`                           | boolean       | true \| false             | Utiliser la table des matières native de Hugo                                               |
| `comments`                             | boolean       | true \| false             | Afficher / masquer les commentaires                                                         |
| `hideFooter`                           | boolean       | true \| false             | Masquer le pied de page                                                                     |
| `CanonicalLinkText`                    | string        | 'Publié initialement sur' | Texte affiché avant l’URL canonique                                                         |
| `displayFullLangName`                  | boolean       | true \| false             | Afficher le nom complet de la langue dans le sélecteur                                      |
| `analytics.google.SiteVerificationTag` | string        | "XYZabc"                  | Balise de vérification Google Analytics                                                     |
| `analytics.bing.SiteVerificationTag`   | string        | "XYZabc"                  | Balise de vérification Bing                                                                |
| `analytics.yandex.SiteVerificationTag` | string        | "XYZabc"                  | Balise de vérification Yandex                                                             |
| `schema`                               | -             | -                         | [Détails](#schema)                                                                         |
| `fuseOpts`                             | -             | -                         | [Détails](#fuseopts)                                                                       |
| `socialIcons`                          | -             | -                         | [Détails](#socialicons)                                                                    |
| `label`                                | -             | -                         | [Détails](#label)                                                                          |
| `assets`                               | -             | -                         | [Détails](#assets)                                                                         |
| `cover`                                | -             | -                         | [Détails](#cover)                                                                          |
| `profileMode`                          | -             | -                         | [Détails](#profilemode)                                                                    |
| `editPost`                             | -             | -                         | [Détails](#editpost)                                                                       |

### Variables du site

| nom         | type   | exemple                                    | Description                                                                                                                   |
| ----------- | ------ | ------------------------------------------ | ----------------------------------------------------------------------------------------------------------------------------- |
| `copyright` | string | `**[example.site](https://example.site)**` | Variable de site Hugo pouvant également contenir du Markdown                                         |

---

> Remarque : le même format est utilisé pour les variables de page.
