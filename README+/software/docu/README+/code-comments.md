# Code&nbsp;&nbsp;&mdash;&nbsp;&nbsp;Comments

<p dir="rtl">,<i>When you feel the need to write a comment<br />first try to refactor the code so that<br />.any comment becomes superfluous</i><br />
 <a href="../../../pencraft/README+/quotes/README+/contributors/README.md#Kent-Beck">Kent Beck</a>, "Refactoring", <b><i>1999</i></b></p>

> **Comments can be eye-catching and essential but signal design inconsistency and poor naming.**<sup>🙋</sup>

Carefully written code is self-descriptive by nature and needs no epistolary clarification<sup>🙋</sup>, 
and even abracadabra in _regex_ processors can be broken down into figurative methods and variables. 

However, comments, rehearsing the names of classes, functions, arguments, and properties, bloat many (if not the majority) source code files of prominent (and not) providers on GitHub (or elsewhere)<sup>📄</sup>.

Accompanied by info and copyright<sup>©️</sup> header and footers. 

\___________\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<sup>🙋</sup>&nbsp;<sub>This statement is for high-level declarative languages.</sub>\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<sup>📄</sup>&nbsp;<sub>Sometimes on a single purpose to report the number of lines contributed.</sub>\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<sup>©️</sup>&nbsp;<sub>As if there were no license agreement or such a spell may prohibit impudent copy-paste.</sub>

## Exceptions

First and foremost, descriptive comments and blocks of them in **demo tests** to serve as guides for devs and presentations for users. 
To replace extra documentation in a way better.

Other valid points are:
 
+ stamps on auto-generated stuff,
+ ridiculous workarounds (especially for third-party bugs),
+ courtesy of Q&A sites,
+ worthy tricks that harm readability,
+ code snippets in documentation,
+ informal notes on test data,
+ domain-explaining quotes from sources like a wiki,
+ explanation of voids **when** significant (`this file is intentionally left blank`, `this class must be void`)
 
One other distinct and legitimate niche is [comment-driven development](https://en.wikipedia.org/wiki/Comment_programming)<sup><b>w</b></sup> (though it's more fun).

Comments may be anchored theses for documentation if you can effectively support two-way updates.

### Commenting the code out

Switching off code lines is a usual manipulation but committing one requires a comment at least that it was on purpose. It might be just three slashes `///` or a team may decide on acronyms like:

&nbsp;&nbsp;&nbsp;&nbsp;`///DEL` — delete after review\
&nbsp;&nbsp;&nbsp;&nbsp;`///ALT` — alternative implementation \
&nbsp;&nbsp;&nbsp;&nbsp;`///ERR` — doesn't work\
&nbsp;&nbsp;&nbsp;&nbsp;`///EXC` — causes an exception\
&nbsp;&nbsp;&nbsp;&nbsp;`///IDEA` — It was a fast sketch which one may simplify or elaborate\
&nbsp;&nbsp;&nbsp;&nbsp;`///LOL` — i did it for lulz

\___________\
 🔚 🌘 2023-2025

