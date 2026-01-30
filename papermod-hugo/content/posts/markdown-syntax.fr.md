---
author: "Hugo Authors"
title: "Guide de la syntaxe Markdown"
date: "2019-03-11"
description: "Article d’exemple présentant la syntaxe Markdown de base et la mise en forme des éléments HTML."
tags: ["markdown", "css", "html", "themes","syntax"]
aliases: ["migrate-from-jekyl"]
cover:
  image: images/msg.png
  caption: "Généré à l’aide de [OG Image Playground par Vercel](https://og-playground.vercel.app/)"
ShowToc: true
TocOpen: true
---

Cet article propose un aperçu de la syntaxe Markdown de base pouvant être utilisée dans les fichiers de contenu Hugo. Il montre également si les éléments HTML de base sont stylisés par le CSS dans un thème Hugo.

<!--more-->

## Titres

Les éléments HTML `<h1>` à `<h6>` représentent six niveaux de titres de section. `<h1>` correspond au niveau de section le plus élevé, tandis que `<h6>` est le plus bas.

# H1

## H2

### H3

#### H4

##### H5

###### H6

## Paragraphe

Xerum, quo qui aut unt expliquam qui dolut labo. Aque venitatiusda cum, voluptionse latur sitiae dolessi aut parist aut dollo enim qui voluptate ma dolestendit peritin re plis aut quas inctum laceat est volestemque commosa as cus endigna tectur, offic to cor sequas etum rerum idem sintibus eiur? Quianimin porecus evelectur, cum que nis nust voloribus ratem aut omnimi, sitatur? Quiatem. Nam, omnis sum am facea corem alique molestrunt et eos evelece arcillit ut aut eos eos nus, sin conecerem erum fuga. Ri oditatquam, ad quibus unda veliamenimin cusam et facea ipsamus es exerum sitate dolores editium rerore eost, temped molorro ratiae volorro te reribus dolorer sperchicium faceata tiustia prat.

Itatur? Quiatae cullecum rem ent aut odis in re eossequodi nonsequ idebis ne sapicia is sinveli squiatum, core et que aut hariosam ex eat.

## Citations

L’élément blockquote représente un contenu cité depuis une autre source, éventuellement accompagné d’une référence qui doit se trouver dans un élément `footer` ou `cite`, et éventuellement de modifications en ligne telles que des annotations ou des abréviations.

#### Citation sans attribution

> Tiam, ad mint andaepu dandae nostion secatur sequo quae.
> **Note** que vous pouvez utiliser la _syntaxe Markdown_ à l’intérieur d’une citation.

#### Citation avec attribution

> Ne communiquez pas en partageant la mémoire, partagez la mémoire en communiquant.
>
> — <cite>Rob Pike[^1]</cite>

[^1]: La citation ci-dessus est extraite de la [conférence](https://www.youtube.com/watch?v=PAAkCSZUG1c) de Rob Pike lors de Gopherfest, le 18 novembre 2015.

## Tableaux

Les tableaux ne font pas partie de la spécification Markdown de base, mais Hugo les prend en charge nativement.

| Nom   | Âge |
| ----- | --- |
| Bob   | 27  |
| Alice | 23  |

#### Markdown en ligne dans les tableaux

| Italique   | Gras     | Code   |
| ---------- | -------- | ------ |
| _italique_ | **gras** | `code` |

## Types de listes

#### Liste ordonnée

1. Premier élément
2. Deuxième élément
3. Troisième élément

#### Liste non ordonnée

- Élément de liste
- Un autre élément
- Et encore un autre

#### Liste non ordonnée imbriquée

- Fruits
  - Pomme
  - Orange
  - Banane
- Produits laitiers
  - Lait
  - Fromage

#### Liste ordonnée imbriquée

1. Fruits
    - Pomme
    - Orange
    - Banane
2. Produits laitiers
    1. Lait
    2. Fromage
3. Troisième élément
    1. Sous-élément un
    2. Sous-élément deux

## Autres éléments — abbr, sub, sup, kbd, mark

<abbr title="Graphics Interchange Format">GIF</abbr> est un format d’image bitmap.

H<sub>2</sub>O

X<sup>n</sup> + Y<sup>n</sup> = Z<sup>n</sup>

Appuyez sur <kbd><kbd>CTRL</kbd>+<kbd>ALT</kbd>+<kbd>Suppr</kbd></kbd> pour terminer la session.

La plupart des <mark>salamandres</mark> sont nocturnes et chassent des insectes, des vers et d’autres petites créatures.
