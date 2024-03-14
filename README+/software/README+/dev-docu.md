# Development - Documenting

## Commenting the code - you need NOT

Comments can be eye-catching and essential but signal design inconsistency and poor naming.  Whereas [quality code](code-quality.md) is self-descriptive by nature and needs no remarks 
 above<sup>:raising_hand:</sup>.

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

Comments may contain temporary text fragments, which will be compiled later into design documentation (and thus directly refer to the implementation). The automation of this idea requires much phantasy and stumbles on extra efforts and maintenance.


## Design papers - you DO need

### Diagrams and presentations

Applications in high-level languages are demonstrative in reverse engineering, but the backward way isn't the best to learn (even with auto-generated diagrams and textual compilation). It will be a real headache without a good file structure and quality code. The ideas, intentions, and spirit of design might differ.

Here the overall diagrams and presentations are rather handy.

Throughout all my writing I stress the code-first: clean, clear, self-descriptive. And you and me may get an expression that a good application needs no documentation...

The lesser the better but cut isn't good.

**Further topics**:\
|- [Technical writing](../../pencraft)

