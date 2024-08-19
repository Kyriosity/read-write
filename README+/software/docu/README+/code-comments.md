# Code - Comments

Comments can be eye-catching and essential but signal design inconsistency and poor naming.  

[Quality code](../QA/) is self-descriptive by nature and needs no epistolary clarification<sup>🙋</sup>, 
and even abracadabra in _regex_ processors can be broken down into figurative functions and vars. 

Exploring source codes of prominent providers on GitHub or elsewhere you'll find many (if not the majority) of the files there bloated with comments, rehearsing the names of classes, functions, arguments, and properties with preceding copyright header<sup>©️</sup>.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<sup>🙋</sup>&nbsp;<sub>This statement is for high-level declarative languages.</sub>\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<sup>©️</sup>&nbsp;<sub>As if there were no license agreement or such a spell may prohibit impudent copy-paste.</sub>

<details>
  <summary><ins><b>&nbsp;Naturally, enough cases are licit to comment - to expand a few:&nbsp;</b></ins></summary>

+ stamps on auto-generated stuff,
+ ridiculous workarounds (especially for third-party bugs),
+ courtesy of Q&A sites,
+ worthy tricks that harm readability,
+ code snippets in documentation,
+ informal notes on test data,
+ domain-explaining quotes from sources like a wiki.\
\____________________________________
</details>

One other distinct and legitimate niche is [comment-driven development](https://en.wikipedia.org/wiki/Comment_programming)<sup>🔗</sup>. Further options can be worth deliberation as:

* Comments may contain temporary text fragments, which will be compiled later into design documentation (and thus directly refer to the implementation).\
<sub>The automation of this idea may stumble on implementation and maintenance expenses.</sub>

### Commenting the code out

 Switching off code lines is a usual manipulation but committing one requires a comment at least that it was on purpose. It might be just three slashes `///` or a team may decide on acronyms like:\
 `///DEL` - delete after review\
 `///ALT` - alternative implementation \
 `///ERR` - doesn't work\
 `///EXC` - causes an exception\
 `///LOL` - i did it for lulz // It was a fast sketch which one may simplify or elaborate

