# Markdown on Git :octocat: &mdash;&thinsp; Hands-on experience <sup>😹</sup>

<p align="right"><b>&ndash;</b>&nbsp;What is the difference between<br /><i>markdown</i> newbie and expert?<br /><b>&ndash;</b>&nbsp;Half an hour.</p>

Markdown is lightweight to learn and use, with plenty of guides and cheat sheets for advanced techniques. This markup and its dialects were never designed to provide rich content.

GitHub alone doesn't render its own site in markdown or a flavor despite positioning it as built-in and primary documentation means.

<p align="center"><b>However if you still consider trying it beyond a slightly formatted text, here is my ounce of teaching illustrated by this repository.</b></p>

<p dir="rtl"><i>.Markdown forgives</i>»<br /><i>«.The GitHub doesn't</i></p>

## Editors and Viewers, Tools

A simple markdown is readable without WYSIWYG, and no editors are supporting it. 
No IDE (as Visual Studio) guarantees a "native" browser experience. Thus, the editor of choice is www.gihub.com where you switch between _Edit_ and _Preview_.

* There's no excuse to avoid grammar check browser plugins.
* View releases on browsers with different engines.
* Always prove the mobile presentation to be passable (but don't expect a nice layout on small screens).

## Limitations

### Markdown

- Markdown doesn't have codes akin to HTML or rich-text formats (e.g. for non-breaking space).
- Native markdown tables are intended for little portions of data.
- There are no variables in markup (Remember it's plain text.)

### Git

- The saddest experience is that no shared content and snippets can be included but <samp>copy-paste</samp>.\
(While elementary repositories share common headers and footers for READMEs.)
- GitHub removes styles and some other formatting.\
(Thus there are always borders in both markdown and HTML tables).
- There's no overlay for image loading but blank space &mdash; readers may be unaware of this and skip your beautiful illustrations.
- Many (if not most) Q&A tricks for markdown won't work on Git.
- It's easier to list what the GitHub site editor has (few shortcut keys) rather than what's expected (toolbars, context menus, safe saving, and so on).
- GitHub isn't the fastest and the smartest markdown engine.

## More than text

### Diagrams

+ GitHub renders `mermaid` diagrams in markdown.\
If you don't know them a [quick tour](https://mermaid.js.org/intro/)<sup>🧜🏼‍♀️</sup> is enough to chart your ideas without delay.
+ Entity names can be made into HTML links (but not in every type!).
+ "Mermaids" mushrooming gives hope to see WYSIWYG tooling soon.

"Mermaids" are beautiful but not for drawings. For a specific layout or artistic look, you have to snap/save a drawing in other programs.

### Pictures

+ That's nothing bad with including images in documents but their size. Markdown on Git won't support extra features like linkable picture areas or images in pop-ups.

### Pictograms / Symbols

GitHub markdown has <code>:<i>emoji</i>:</code> codes but it's the same collection as in _emoji keyboard_ (<kbd>Win+.</kbd> for Windows users). 
To my knowledge, the only exception is Git's <code>:octocat:</code>.
Emojis are better than their codes unless a document must be saved as <samp>ASCII</samp>.

Review [HTML symbols](https://www.w3schools.com/charsets/ref_html_symbols.asp)<sup>🔗</sup> as a great enhancement of selections.

<p align="center">⚠️ Browsers may show some pictograms differently. Find out diffs on this snapshot:</p>
<p align="center"><a href="essays/README+/AI-2020s.md#evidence"><img alt="&nbsp;string of emojis presented different" src="../../_rsc/_img/snap/screen/emojis_diff-browsers.jpg" title="&nbsp;Click to see how it looks in yours" /></a></p>

### Miscellany

Don't forget about naturally supported `code snippets`, [math expressions](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/writing-mathematical-expressions)<sup>:octocat:</sup>, and [badges](https://shields.io/)<sup>🔗</sup>.

## HTML

HTML elements are required even for the purest text: markdown has neither non-breaking space nor a hyphen.

The richer the content the more HTML you will use. The use of HTML is inevitable inside of `<table>`<i>s</i>.

## Tips, tricks and advice

Advice Nr&thinsp;1 is **don't try to hack git markdown**. Even if you manage to style some stuff one day Git may sweep it out.

Besides symbols, the best HTML pals of markdown writers are

+ `<details>` expandables to moderate the volume hit and for optional parts.
+ `<table>` - needs explanation?
+ `<sub>`, `<sup>`, and `..[v]align=..`.

Markdown automatically highlights alternative rows, but by inserting `</tr><tr>` you can master it.

### Fancy footnotes

Numbered footnotes are academic and convenient but a number itself won't tell much about its subject (when separated by enough content). Mnemonic superscript references are eye-catching<sup>🙋</sup>.

&nbsp;&nbsp;&nbsp;&nbsp;<sup>🙋</sup>You can invent your footnotes vocabulary, as I use _raising hand_ to express the own opinion.
    
### Links suffixes

Named links are overall practice but they distract. You may hint that a URL goes **outside**: [Docs as code](https://www.writethedocs.org/guide/docs-as-code/)<sup>🔗</sup>. 
Next, narrow mnemonics to hint on frequently referred resources, like:\
[Reactive programs](https://en.wikipedia.org/wiki/Reactive_programming)<sup><b>w</b></sup>,&nbsp;&nbsp;
[Trending C#](https://github.com/trending/c%23)<sup>:octocat:</sup>,&nbsp;&nbsp;
[charts samples](https://mermaid.js.org/syntax/examples.html)<sup>🧜‍♀️</sup>,&nbsp;&nbsp;
[co- vs. contravariance](https://learn.microsoft.com/en-us/dotnet/standard/generics/covariance-and-contravariance)<sup>🪟</sup>,&nbsp;&nbsp;
[`C# Lookup`](https://learn.microsoft.com/en-us/dotnet/api/system.linq.lookup-2)<sup>🪟</sup>,&nbsp;&nbsp;
[.NET conf 2024](https://www.youtube.com/watch?v=ikSNL-lxolc)<sup><picture><img src="../../_rsc/_img/logo/logo-youtube_h12px.jpg" title="&nbsp;link to YouTube video" /></picture></sup>.

### <a id="link-achors" />Link anchors

Prefer `<a id="anchor_name" />` for sustained (internal) links to avoid changeable and motley `#-heading`.

```diff
-   ## Unlinkable fancy header,,🐈‍⬛!!..
+   ## <a id="feline_anchor">unlinkable fancy header,,🐈‍⬛!!..

// somewhere ...
... <a href="../animal_stories.md#feline_anchor">fancy cats</a> ...
```

### Images

Avoid clickable images unless they are links or a detailed (bigger) version: HTML `<picture>` to rescue.

## Wrap up

You may consider Git-supported dialects as [flavored markdown](https://github.github.com/gfm/)<sup>:octocat:</sup> and converters as [PanDoc](https://pandoc.org)<sup>🔗</sup>.

\___________\
🔚 🌙 2025
