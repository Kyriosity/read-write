# Development - Documentation

<p dir="rtl">,Code in English<br/>,comment in Latin<br/>,document en français<br/>. . .</p>

## Commenting the `code`

Comments can be eye-catching and essential but signal design inconsistency and poor naming.  Whereas good pro code is self-descriptive by nature and needs no remarks<sup>:raising_hand:</sup>.

Exploring source codes of prominent providers on GitHub or elsewhere you'll find many (if not the majority) of the files there bloated with comments, rehearsing the names of classes, functions, arguments, and properties with preceding copyright header<sup>©️</sup>.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<sup>:raising_hand:</sup>&nbsp;<sub>This statement is for high-level declarative languages.</sub>\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<sup>©️</sup>&nbsp;<sub>As if there were no license agreement or such a spell may prohibit impudent copy-paste.</sub>

However, comments are fully justified for:

+ weird workarounds (especially for third-party bugs),
+ courtesy of Q&A sites,
+ worthy tricks that harm readability,
+ code snippets in documentation,
+ domain-explaining quotes from sources like a wiki,

There's one more niche [comment-driven development](en.wikipedia.org/wiki/Comment_programming)<sup>🔗</sup>. 

Comments may contain temporary text fragments, which will be compiled later into design documentation (and thus directly refer to the implementation). The automation of this idea may stumble on extra effort and maintenance but it's worth a try.

## Recording the ⏺️ design ⏹️

<p dir="rtl">. . .<br/>.and think in 3D diagrams</p>


Good code reads well, especially when guided by a well-thought-of test plan. And nothing is better for reverse engineering than source code. This approach alone gets exponentially harder and will not reveal design/architecture intentions. It's warped to view the big picture.

In practice, the code will be obscure and tests will lack clarity and seamless categorization.

### Docu

Even if there's extensive user guidance, even the best quality application code needs a fluent explanation: 

+ attractive intro,
+ navigation to source code,
+ clues to common and own patterns and templates used,
+ known design compromises, drawbacks, and "props" (that not properties),

The higher level and more concise the documentation the better - nobody will maintain volumes of papers up-to-date and read them attentively.

Any document will be a bore without drawings, diagrams, and presentations.

### Diagrams and presentations

There are elaborated commercial tools to create strict and attributed UML diagrams, but limit them to formal rules (e.g. 2D). 
A fast simple sketch could be enough and brpader in all senses.
It may start at a whiteboard within the discussion.

### Log

Commit comments can make a log of the design. Theoretically but practically it will be too much white noise.

Just the daily log on notable decisions could be a great help to reveal the pace of design. 

### Screen capture

That's the absolute winner in the snap of design. When a release is ripe, it will take max. 20-30' to switch the screen snap on, explore the code, and commentate. Maybe 10' more to find a tool of video capture.
You will be the first to thank yourself after a pause on this piece of development.

**Further topics**:\
|- [Quality code](code-quality.md)\
|- [Technical writing](../../pencraft)

