---
author: "Hugo Authors"
title: "Prise en charge des emojis"
date: "2019-03-05"
description: "Guide d’utilisation des emojis dans Hugo"
tags: ["emoji"]
ShowToc: true
ShowBreadCrumbs: true
---

Les emojis peuvent être activés dans un projet Hugo de plusieurs manières.

<!--more-->

La fonction [`emojify`](https://gohugo.io/functions/emojify/) peut être appelée directement dans les templates ou dans des [shortcodes en ligne](https://gohugo.io/templates/shortcode-templates/#inline-shortcodes).

Pour activer les emojis globalement, définissez `enableEmoji` sur `true` dans la [configuration](https://gohugo.io/getting-started/configuration/) de votre site. Vous pourrez ensuite saisir directement les codes abrégés d’emojis dans les fichiers de contenu, par exemple :

<p><span class="nowrap"><span class="emojify">🙈</span> <code>:see_no_evil:</code></span>  <span class="nowrap"><span class="emojify">🙉</span> <code>:hear_no_evil:</code></span>  <span class="nowrap"><span class="emojify">🙊</span> <code>:speak_no_evil:</code></span></p>
<br>

La [table de référence des emojis](http://www.emoji-cheat-sheet.com/) constitue une ressource utile pour les codes abrégés d’emojis.

---

**N.B.** Les étapes ci-dessus activent les caractères et séquences d’emojis du standard Unicode dans Hugo. Toutefois, le rendu de ces glyphes dépend du navigateur et de la plateforme utilisés. Pour styliser les emojis, vous pouvez soit utiliser une police d’emojis tierce, soit une pile de polices, par exemple :

{{< highlight html >}}
.emoji {
font-family: Apple Color Emoji, Segoe UI Emoji, NotoColorEmoji, Segoe UI Symbol, Android Emoji, EmojiSymbols;
}
{{< /highlight >}}

{{< css.inline >}}

<style>
.emojify {
	font-family: Apple Color Emoji, Segoe UI Emoji, NotoColorEmoji, Segoe UI Symbol, Android Emoji, EmojiSymbols;
	font-size: 2rem;
	vertical-align: middle;
}
@media screen and (max-width:650px) {
  .nowrap {
    display: block;
    margin: 25px 0;
  }
}
</style>

{{< /css.inline >}}
