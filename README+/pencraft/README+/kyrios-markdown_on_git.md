# Markdown on Git :octocat: &mdash;&thinsp; Personal experience <sup>😹</sup>

<p align="right"><b>&ndash;</b>&nbsp;What is the difference between<br /><i>markdown</i> newbie and expert?<br /><b>&ndash;</b>&nbsp;Half an hour.</p>

Markdown is lightweight to learn and use, with plenty of guides and cheat sheets for advanced techniques. However, it and its dialects were never intended to provide rich content.

GitHub itself doesn't render its site in markdown or flavor despite providing it as built-in and primary documentation markup.

<p align="center"><b>But if you still want to try it beyond a slightly formatted text, here is my ounce of teaching illustrated by this repository.</b></p>

<p dir="rtl">«<i>.Markdown forgives. The GitHub doesn't</i>»</p>

## Editors and Viewers, Tools

A simple markdown is readable without WYSIWYG, and no editors are supporting it. No IDE (as Visual Studio) guarantees a "native" browser experience. Thus, the editor of choice is www.gihub.com where you switch between _Edit_ and _Preview_.

* There's no excuse to avoid grammar check browser plugins.
* View releases on browsers with different engines.
* Always prove the mobile presentation to be passable (it won't be perfect for rich layout).

## Limitations

### Markdown

- Markdown doesn't have codes akin to HTML or rich-text formats (e.g. for non-breaking space).
- Native markdown tables are intended for little portions of data.
- There are no variables in markup (Remember it's plain text.)

### Git

- The saddest experience with raw markdown is that you can't include shared content and snippets but <samp>copy-paste</samp>.
- GitHub removes styles and some other formatting.\
(Thus there are always borders in both markdown and HTML tables).
- There's no overlay for image loading but blank space &mdash; readers may be unaware of this and skip your beautiful illustrations.
- Many (if not most) Q&A tricks for markdown won't work on Git.
- GitHub site editir could provide much more actions than Preview and Commit.
- GitHub isn't the fastest and the smartest markdown engine.

## Non-text

### Diagrams

+ Enough to say that you can and shall insert [mermaid](https://mermaid.js.org)<sup>🔗</sup> diagrams. And that they are evolving pretty fast.
+ Entity names can be made into HTML links (but not in every type!).
+ "Mermaids" aren't for illustration. For a specific layout or artistic look, you have to snap/save a drawing in other apps.

### Pictures

+ That's nothing bad with including images in documents but their size. Markdown on Git won't support extra features like linkable picture areas or images in pop-ups.

### Pictograms / Symbols

GitHub markdown has <code>:<i>emoji</i>:</code> codes but it's the same collection as in _emoji keyboard_ (<kbd>Win+.</kbd> for Windows users). 
The only exception, to my knowledge, is Git's <code>:octocat:</code>.
Emojis are better than their codes unless a document must be saved as <samp>ASCII</samp>.

HTML symbols enhance the choice.

WARNING: Different browsers may show some pictograms differently, a snapshot for example:

<a href="essays/README+/AI-2020s.md#evidence"><img alt="&nbsp;string of emojis presented different" src="../../_rsc/_img/snap/screen/emojis_diff-browsers.jpg" title="&nbsp;Click to see how it looks in yours" /></a>

### Misc

Don't forget about naturally supported `code snippets`, and [badges](https://shields.io/)<sup>🔗</sup>

## HTML

HTML elements are required even for simple text: markdown has neither non-breaking space nor hyphen.

The richer the content the more HTML you will use. The use of HTML is inevitable inside of `<table>`<i>s</i>.

## Tips, tricks and advice

Advice Nr&thinsp;1 is **don't try to hack git markdown**. Even if you manage to style some stuff one day Git may sweep it out.

Best HTML pals are

+ `<details />` expandables to moderate the volume hit and for optional parts.
+ `<table>` - need to explain?
+ `..[v]align=..`

### Fancy footnotes

Numbered footnotes are academic and convenient but a number itself won't tell much about its subject (when separated by enough content). Mnemonic superscript references are eye-catching<sup>🙋</sup>.

&nbsp;&nbsp;&nbsp;&nbsp;<sup>🙋</sup>You can invent your footnotes vocabulary, as I use _raising hand_ to express the own opinion.
    
### Links suffixes

Named links are overall practice but they distract. You may hint that a URL goes outside: [fast mermaid examples](https://mermaid.js.org/syntax/examples.html) <sup>🔗</sup>. 
Next, narrow mnemonics for frequently referred resources, like 
[wiki](https://wikipedia.org)<sup><b>w</b></sup>, [git](https://github.com)<sup>:octocat:</sup>, [YouTube](https://youtube.com)<sup><picture><img src="../../_rsc/_img/logo/logo-youtube_h12px.jpg" title="&nbsp;link to YouTube video" /></picture></sup>,
[Microsof Learn](https://learn.microsoft.com/)<sup>🪟</sup>.

### <a id="link-achors" />Link anchors

Prefer `<a id="anchor_name" />` for sustained (internal) links to avoid changeable and motley `#-heading`.

```diff
-   ## Unlinkable fancy header,,🐈‍⬛!!..
+   ## <a id="feline_anchor">unlinkable fancy header,,🐈‍⬛!!..

// somewhere outside ...
... <a href="../animal_stories.md#feline_anchor">fancy cats</a> ...
```

### Images

Avoid clickable images unless they are links or a detailed (bigger) version: HTML `<picture>` to rescue.

## Wrap up

You may consider Git-supported dialects as [flavored markdown](https://github.github.com/gfm/)<sup>:octocat:</sup> and converters as [PanDoc](https://pandoc.org)<sup>🔗</sup>.

\___________\
🔚 🌙 2025
