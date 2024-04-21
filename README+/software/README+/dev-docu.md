# Development - Documentation

<p dir="rtl">,Code in English<br/>,comment in Latin<br/>,document en français<br/>. . .</p>

## `//` Commenting the `code`

Comments can be eye-catching and essential but signal design inconsistency and poor naming.  Whereas good pro code is self-descriptive by nature and needs no epistolary clarification<sup>:raising_hand:</sup>.

Exploring source codes of prominent providers on GitHub or elsewhere you'll find many (if not the majority) of the files there bloated with comments, rehearsing the names of classes, functions, arguments, and properties with preceding copyright header<sup>©️</sup>.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<sup>:raising_hand:</sup>&nbsp;<sub>This statement is for high-level declarative languages.</sub>\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<sup>©️</sup>&nbsp;<sub>As if there were no license agreement or such a spell may prohibit impudent copy-paste.</sub>

However, comments are fully justified for:

+ weird workarounds (especially for third-party bugs),
+ courtesy of Q&A sites,
+ worthy tricks that harm readability,
+ code snippets in documentation,
+ domain-explaining quotes from sources like a wiki,

One other legitimate niche is [comment-driven development](en.wikipedia.org/wiki/Comment_programming)<sup>🔗</sup>. 

Comments may contain temporary text fragments, which will be compiled later into design documentation (and thus directly refer to the implementation). 
The automation of this idea may stumble on implementation and maintenance expenses but it's worth deliberation.

<p dir="rtl">. . .<br/>but think in 3D diagrams</p>

## Recording ⏺️ design ⏹️

[Quality code](code-quality.md) reads well, peculiarly when a well-thought-of test plan guides the investigators. And nothing is better for reverse engineering than source code. 
This approach solus becomes exponentially harder and will not reveal remarkable design/architecture intentions. It's warped to unfold the big picture.

In practice, the code will be obscure and tests will lack clarity and seamless categorization. Code prose and time will bury great (no sarcasm) design decisions unless emphasized in docs.

### In word

Even if there's extensive user guidance, even the best quality application code needs a fluent explanation: 

+ attractive intro,
+ navigation to source code,
+ clues to common and own patterns and templates used,
+ known design compromises, drawbacks, and "props",

The higher level and more concise the documentation the better - nobody will maintain volumes of papers up-to-date and read them attentively.

#### Log

Commit comments can make a log of the design. Theoretically but practically it will be too much white noise.

Just the daily log on notable decisions could be a great help to document the pace of design. 

#### F.A.Q.

Continuous ratification of design decisions (incl. rejection ) in the form of Question-Answer will compose a useful and concise user/developer document. 

---

Any text document (except F.A.Q.) over a few pages will be boring without drawings, diagrams, and presentations.

### Diagrams and presentations

There are elaborated commercial tools to create strict and attributed UML diagrams, but limit them to formal rules (e.g. 2D). 
A fast simple sketch could be enough and broader in all senses.
It may start at a whiteboard within the discussion.

### Artistic images

Applying aesthetic traits to attribute images or enliven the text highly motivates readers when done with taste and bounds. Highly recommended as memory "anchors" on difficult subjects.

#### Pictograms / emojis

Small images are smart helpers to annotate, navigate, and focus unless heavily overused. They may apply to everything - text, solution items (folders and filenames), and even program output (UTF-8 glyphs to rescue).

A team should limit them to a subset<sup>🍋</sup>, define the exact meaning of most, and put some on a blacklist (for ambiguity or cultural issues).

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<sup>🍋</sup> <sub>By default markdown emojis, supported by GitHub  - see this [cheatsheet](https://github.com/ikatyang/emoji-cheat-sheet/blob/master/README.md).</sub>

### Video tutorial - Screen capture

"A picture is worth a thousand words", and a short video is worth a hundred pictures. That's the absolute winner in the snap of design. 

When a release is ripe, it will take max. 20-30' to switch the screen snap on, explore the code, and commentate impromptu. 
It may take an additional 10' to find a tool for video capture.
You will be the first to thank yourself after a pause on this or that piece of development.

## Summary

1. Docu shortage will obfuscate substantial concepts and require essential efforts to (re)gain focus on a software part later<sup>🔖</sup>.  
2. Instead of being a side-effect of development docu shall be an acknowledged task, requiring resources and enthusiasm.
3. Docu shall evolve along with software for accuracy and mutual contribution.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<sup>🔖</sup> <sub>You are self the consumer&nbsp;Nr1 of this product - it's only a week to lose a grasp on the "unfocused" design part.</sub>

🔚


