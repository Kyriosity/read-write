# Software - Design - Documentation

<p dir="rtl">,Code in English<br/>,comment in Latin<br/>,document en français<br/>but think in 3D diagrams</p>

[Quality code](../../QA/README+/code-quality.md) with profound and thoroughly categorized [names](../../design/names) must explain design brainchilds in intuitive fashion. Sincerely written [design-defining-tests](../../design/drive/) must smoothly introduce them. And nothing is more suitable for reverse engineering (manual or automatic) than source codes. 

Albeit this approach solus becomes gradually tougher (until it hits the wall of the perfectionism exponent) and will not reveal remarkable design/architecture intentions. It's warped to unfold the big canvas of abstractions.

In reality, the code will be partly or greatly obscure and tests will lack clarity and both &mdash; seamless categorization. 
Code prose and time will bury grand (no sarcasm) design decisions unless highlighted with a pen. 

Explorers on the other side will overestimate weak decisions, and search for deep meaning in shallow parts.

**That's why software design needs documentation, which must be a creative stratum between code readability and dev team lore.**

\_________

**General to the theme:**\
|- [Tech docu](../../../pencraft/README+/tech_docu.md)\
|--- [Tips](../../../pencraft/README+/tips-tech_docu.md)

## Recording ⏺️ design ⏹️

Even if there's extensive user guidance, even the best quality application code needs a fluent explanation: 

* engaging intro,
* navigation to source code,
* clues to common and own patterns and templates used,
* known design compromises, drawbacks, and "props" [props as supports].

The higher the level and more concise (yet complete) the documentation &mdash; the better. Nobody will maintain volumes of papers up-to-date and the rare will read them thoroughly.

### Log/Blog

Commit comments can make a skeleton of the design log. Theoretically automated but practically there will be too many mixed entries with white noise.

Just a daily (semi-weekly) log (or blog) on notable decisions could be a great help in documenting the pace of design. 

### F.A.Q.

Continuous ratification of design decisions (incl. rejection) in the form of Question-Answer will compose a useful and concise user/developer document. 

### Diagrams and presentations

**Any text document (except F.A.Q.) over a few pages will be boring without drawings, diagrams, and presentations.**

There are elaborated methodologies and tools (to remember classical IBM Rational Rose and RUP) to evolve a project in UML and other diagrams. 
However, they cost time, restrain presentation, stick thinking to 2D (literally and metaphorically), and prompt to input redundant details. Mutual synchronization with code will make matters even worse.

The compromise is to maintain top diagrams with modest detailing. make presentations with and root documentation from them. 

## Whiteboard

Fast simple sketches resting on multiple fictitious axes (horizontal grouping, aggregation/inheritance hierarchies, timeline) could be enough and broader in all senses. 

They may start on a whiteboard<sup>🔲</sup> during a casual discussion and as taking shapes recorded in (vector) graphics tools of choice and skills. 

\_________

&nbsp;&nbsp;&nbsp;&nbsp;<sup>🔲</sup> <sub>Can anything be better than a whiteboard? The glass board! It allows one not only to look at the design from the unusual side but also attach various backgrounds (e.g. previous printout). _Trace paper_ is a compact individual variant.</sub>

### Beyond sketches

Easy come - easy go. 
Whiteboard sketches are potent for understanding but if stored as snapshots without shaping<sup>🗜️</sup>, trimming<sup>✂️</sup>, and attributing<sup>🍒</sup> they will be only trash for "future generations".\
This isn't a routine activity but an intellectual task of design and modeling.

\_________

&nbsp;&nbsp;&nbsp;<sup>🗜️</sup> <sub>Visualize artifacts on boars as recognized entities and connections.</sub>\
&nbsp;&nbsp;&nbsp;&nbsp;<sup>✂️</sup> <sub>Remove (join) redundant elements and visual noize.</sub>\
&nbsp;&nbsp;&nbsp;&nbsp;<sup>🍒</sup> <sub>Systematically classify and name artifacts.</sub>


## Summary

1. Docu shortage will obfuscate substantial concepts and require essential efforts to (re)gain focus on a software part later<sup>🔖</sup>.  
2. Instead of being a side-effect of development docu shall be an acknowledged task, requiring resources and enthusiasm.
3. Docu shall evolve along with software for accuracy and mutual contribution.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<sup>🔖</sup> <sub>You are self the consumer&nbsp;**#1** of this product - it's only a week to lose a grasp on the "unfocused" design part.</sub>

## Wrap up. Sync with code!

> ❗ The most important note was reserved to the end.

**No excuse for the docu missing references to the implementation** - that is code. Not every feature but entry points.

As an example in progress see ➡️[use-dev](https://github.com/Kyriosity/use-dev/).

## Appendix 1/2. Artistic images (sounds, videos)

Applying aesthetic traits to attribute images or enliven the text highly motivates readers when done with taste and bounds. Highly recommended as memory "anchors" on difficult subjects.

## Appendix 2/2. Alternatives?

### Video tutorial - Screen capture

"A picture is worth a thousand words", and the shortest video is made up of thousands of them. That's the absolute winner in the snap of design. 

When a release is ripe, it will take half an hour per module (app) to switch the screen snap on, explore the code, and commentate impromptu.<sup>📹</sup> Then an hour or some to review and record a much better version.

Yes, it's a kind of documentation (or source for) but it is rather peculiar.

\_______

&nbsp;&nbsp;&nbsp;&nbsp;<sup>📹</sup> <sub>Tools for screen capture begin from freeware (with 5` to learn) and go up to top pro.</sub>

### Coding under guidance

Arbitrarart, the most effective and fast way to introduce a project is to make new programmers code a feature under the guidance of an experienced developer (with a domain expert).

It's not a _pair programming_ and must be in no way the opposite of "watch&learn".

Disadvantage: it's a one-time exercise that takes hours from most competent team members.

Taking advantage of the disadvantage: everybody learns how to present the design and see its strong and weak sides.

🔚
