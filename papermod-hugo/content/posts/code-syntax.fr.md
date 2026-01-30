---
author: ["Aditya Telange"]
title: "Guide de la syntaxe du code"
date: "2019-03-10"
description: "Article d’exemple présentant la syntaxe du code et sa mise en forme de base pour les éléments HTML."
summary: "Article d’exemple présentant la syntaxe du code et sa mise en forme de base pour les éléments HTML."
tags: ["markdown", "syntax", "code", "gist","themes"]
ShowToc: true
TocOpen: true
social:
  fediverse_creator: "@adityatelange@mastodon.social"
---

### Code en ligne

`Ceci est du code en ligne`

### Balise `pre` seule

<pre>
Ceci est du texte préformaté
</pre>

### Bloc de code avec backticks

```{hl_lines=[2,8]}
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8" />
    <title>Exemple de document HTML5</title>
    <meta
      name="description"
      content="Article d’exemple présentant la syntaxe Markdown de base et la mise en forme des éléments HTML."
    />
  </head>
  <body>
    <p>Test</p>
  </body>
</html>
```

### Bloc de code avec backticks et langage spécifié

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8" />
    <title>Exemple de document HTML5</title>
    <meta
      name="description"
      content="Article d’exemple présentant la syntaxe Markdown de base et la mise en forme des éléments HTML."
    />
  </head>
  <body>
    <p>Test</p>
  </body>
</html>
```

### Bloc de code avec backticks, langage spécifié et numéros de ligne

```html {linenos=true}
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8" />
    <title>Exemple de document HTML5</title>
    <meta
      name="description"
      content="Article d’exemple présentant la syntaxe Markdown de base et la mise en forme des éléments HTML."
    />
  </head>
  <body>
    <p>Test</p>
  </body>
</html>
```

### Bloc de code avec numéros de ligne et lignes <mark>mises en évidence</mark>

- PaperMod prend en charge `linenos=true` ou `linenos=table`

```html {linenos=true,hl_lines=[2,8]}
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8" />
    <title>Exemple de document HTML5</title>
    <meta
      name="description"
      content="Article d’exemple présentant la syntaxe Markdown de base et la mise en forme des éléments HTML."
    />
  </head>
  <body>
    <p>Test</p>
  </body>
</html>
```

- <del>Avec `linenos=inline`, la mise en évidence des lignes <mark>**peut ne pas** fonctionner correctement</mark>.<del>
- Ce problème est corrigé avec le commit [045c084](https://github.com/adityatelange/hugo-PaperMod/commit/045c08496d61b1b3f9c79e69e7d3d243a526d8f3)

```html {linenos=inline,hl_lines=[2,8]}
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8" />
    <title>Exemple de document HTML5</title>
    <meta
      name="description"
      content="Article d’exemple présentant la syntaxe Markdown de base et la mise en forme des éléments HTML."
    />
  </head>
  <body>
    <p>Test</p>
  </body>
</html>
```

### Bloc de code indenté avec quatre espaces

    <!doctype html>
    <html lang="en">
    <head>
      <meta charset="utf-8">
      <title>Exemple de document HTML5</title>
    </head>
    <body>
      <p>Test</p>
    </body>
    </html>

### Bloc de code avec le shortcode interne de mise en évidence de Hugo

{{< highlight html >}}

<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8">
  <title>Exemple de document HTML5</title>
</head>
<body>
  <p>Test</p>
</body>
</html>
{{< /highlight >}}

### Gist GitHub

{{< gist adityatelange 376cd56ee2c94aaa2e8b93200f2ba8b5 >}}
