---
author: Hugo Authors
title: Mise en forme mathématique
date: 2019-03-08
description: Guide succinct pour configurer KaTeX
math: true
ShowBreadCrumbs: true
---

La notation mathématique dans un projet Hugo peut être activée à l’aide de bibliothèques JavaScript tierces.

<!--more-->

Dans cet exemple, nous utilisons [KaTeX](https://katex.org/).

- Créez un partial dans `/layouts/partials/math.html`
- Dans ce partial, référencez l’[extension d’auto-rendu](https://katex.org/docs/autorender.html) ou hébergez ces scripts localement
- Incluez le partial dans vos templates (par exemple dans [`extend_head.html`](../papermod/papermod-faq/#custom-head--footer)) de la manière suivante :
- Voir également l’[ISSUE #236](https://github.com/adityatelange/hugo-PaperMod/issues/236)

```bash
{{ if or .Params.math .Site.Params.math }}
{{ partial "math.html" . }}
{{ end }}
```

- Pour activer KaTeX globalement, définissez le paramètre `math` sur `true` dans la configuration du projet
- Pour activer KaTeX page par page, ajoutez le paramètre `math: true` dans les fichiers de contenu concernés

**Note :** utilisez la documentation en ligne des [fonctions TeX prises en charge](https://katex.org/docs/supported.html)

{{< math.inline >}}
{{ if or .Page.Params.math .Site.Params.math }}

<!-- KaTeX -->
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/katex@0.11.1/dist/katex.min.css" integrity="sha384-zB1R0rpPzHqg7Kpt0Aljp8JPLqbXI3bhnPWROx27a9N0Ll6ZP/+DiW/UqRcLbRjq" crossorigin="anonymous">
<script defer src="https://cdn.jsdelivr.net/npm/katex@0.11.1/dist/katex.min.js" integrity="sha384-y23I5Q6l+B6vatafAwxRu/0oK/79VlbSz7Q9aiSZUvyWYIYsd+qj+o24G5ZU2zJz" crossorigin="anonymous"></script>
<script defer src="https://cdn.jsdelivr.net/npm/katex@0.11.1/dist/contrib/auto-render.min.js" integrity="sha384-kWPLUVMOks5AQFrykwIup5lo0m3iMkkHrD0uJ4H5cjeGihAutqP0yW0J6dpFiVkI" crossorigin="anonymous" onload="renderMathInElement(document.body);"></script>
{{ end }}
{{</ math.inline >}}

### Exemples

{{< math.inline >}}

<p>
Mathématiques en ligne : \(\varphi = \dfrac{1+\sqrt5}{2}= 1.6180339887…\)
</p>
{{</ math.inline >}}

Mathématiques en bloc :

$$
 \varphi = 1+\frac{1} {1+\frac{1} {1+\frac{1} {1+\cdots} } }
$$
