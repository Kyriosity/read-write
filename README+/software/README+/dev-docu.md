# Development - Documentation

<p dir="rtl">,Code in English<br/>,comment in Latin<br/>document en français</p>

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
+ notes, to be transformed into board tasks (better automatically on submission).

Comments may contain temporary text fragments, which will be compiled later into design documentation (and thus directly refer to the implementation). The automation of this idea may stumble on extra effort and maintenance but it's worth a try.

## Recording the ⏺️ design ⏹️

Good code reads well, especially when guided by a well-thought-of test plan. And nothing is better for reverse engineering than source code. This approach alone gets exponentially harder and will not reveal design/architecture intentions. It's warped to view the big picture.

In practice, the code will be obscure and tests will lack clarity and seamless categorization.

### Docu

Even if there's extensive user guidance, even the best quality application code needs a fluent explanation: 

+ attractive intro,
+ navigation notes,
+ clues to common and own patterns and templates used,
+ known design compromises, drawbacks, and "props",

The higher level and more concise the documentation the better - nobody will maintain volumes of papers up-to-date and read them attentively.

Any document will be a bore without drawings, diagrams, and presentations.

### Diagrams and presentations

Any good picture is worth of hundreds words.

#### Log

Commits and comments.

### Screen motion capture



**Further topics**:\
|- [Quality code](code-quality.md)\
|- [Technical writing](../../pencraft)

