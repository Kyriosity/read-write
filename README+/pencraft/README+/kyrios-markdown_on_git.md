# Markdown on Git :octocat: &mdash;&thinsp; Personal experience <sup>😹</sup>

<p align="right"><b>&ndash;</b>&nbsp;What is the difference between<br /><i>markdown</i> newbie and expert?<br /><b>&ndash;</b>&nbsp;Half an hour.</p>

Markdown is lightweight to learn and use with plenty of guides and cheat sheets for advanced techniques. However, you shouldn't use it for rich content. (Even GitHub content isn't built-in markdown despite its role as the primary markup of documentation.)

<p align="center"><b>But if you still want to try it beyond a slightly formatted text, here is my ounce of teaching backed by this repository.</b></p>

<p align="right">«<i>Markdown forgives. The GitHub doesn't.</i>»</p>

## Editors and Viewers, Tools

Simple markdown is readable without WYSIWYG and there are no tools for it to guarantee a "native" browser experience. So, the editor of choice is www.gihub.com where you switch between _Edit_ and _Preview_.

* There's no excuse to avoid grammar check browser plugins.
* Always prove the mobile presentation to be legible.

## Limitations

### Markdown

- Natural markdown tables are intended for little portions of text.

### Git

- The saddest experience with raw markdown is that you can't include shared content and snippets but <samp>copy-paste</samp>.

- GitHub removes styles and some other formatting. Thus there are always borders in both markdown and HTML tables.
  
- There's no overlay for image loading but blank space &mdash; readers may be unaware of this and skip your beautiful illustrations.

## Non-text

### Diagrams and Pictures

+ Enough to say that you can and shall insert [mermaid](https://mermaid.js.org)<sup>🔗</sup> diagrams. Text (names) there can be made into HTML links (but not in every type!).

+ That's nothing bad with including images in documents but their size.

### Pictograms

GitHub markdown has <code>:<i>emoji</i>:</code> codes but it's the same collection as in _emoji keyboard_ (<kbd>Win+.</kbd> for Windows users). The only exception, to my knowledge, is Git's <code>:octocat:</code>.
Emojis are better than their codes unless a document must be saved as <samp>ASCII</samp>.

WARNING: Different browsers may show some pictograms differently, a snapshot for example:

<a href="essays/README+/AI-2020s.md#evidence"><img alt="&nbsp;string of emojis presented different" src="../../_rsc/_img/snap/screen/emojis_diff-browsers.jpg" title="&nbsp;Click to see how it looks in yours" /></a>

### Misc

Don't forget about naturally supported `code snippets`.

## HTML

HTML elements are required even for simple text: markdown has neither space nor hyphen for non-breaking.

The richer the content the more HTML you will use.
  
## Tips, tricks and advice

Advice Nr&thinsp;1 is **don't try to hack git markdown**. Even if you manage to style some stuff one day Git may sweep it out.

Tip Nr&nbsp;1 is to use `<details />` expandables to moderate the volume hit and for optional parts.

### Fancy footnotes

Numbered footnotes are academic and convenient but a number itself won't tell much about its subject (when separated by enough content). Mnemonic superscript references<sup>🙋</sup> are eye-catching.

&nbsp;&nbsp;&nbsp;&nbsp;<sup>🙋</sup>You can invent your footnotes vocabulary, as I use _raising hand_ to express the own opinion.
    
### Links suffixes

Named links are overall practice but they distract. You may hint that a URL goes outside: [fast mermaid examples](https://mermaid.js.org/syntax/examples.html) <sup>🔗</sup>. 
Next, narrow mnemonics for frequently referred resources, like 
[wiki](https://wikipedia.org)<sup><b>w</b></sup>, [git](https://github.com)<sup>:octocat:</sup>, [YouTube](https://youtube.com)<sup><picture><img src="../../_rsc/_img/logo/logo-youtube_h12px.jpg" title="link to YouTube video" /></picture></sup>,
[Microsof Learn](https://learn.microsoft.com/)<sup>🪟</sup>.

### <a id="link-achors" />Link anchors

Prefer `<a id="anchor_name" />` for sustained (internal) links to avoid changeable and motley `#-heading`.

### Images

Avoid clickable images unless they are links or a detailed (bigger) version: HTML `<picture>` to rescue.

## Wrap up

You may consider Git-supported dialects as [flavored markdown](https://github.github.com/gfm/)<sup>:octocat:</sup> and converters as [PanDoc](https://pandoc.org)<sup>🔗</sup>.

\___________\
🔚 🌙 2025
