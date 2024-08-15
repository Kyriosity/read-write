# Software - Naming and categorization

<p dir="rtl"><i>"...In the beginning was the Word"</div></i></p><br/>

The denomination is a pivotal but underrated and neglected activity in every sphere. 

In software, it looks like granted when names with categories smoothly guide through the design and make coding intuitive. On the contrary, wading through the thorns of poorly named and labyrinths of badly categorized code, abatis of docu developers will curse application complexity, learning curve, technologies used, and fate but at least the naming.

## How to...

:x: Usual: Naming as a derivative of development, which spawns `Helper.Get(..)`, `Utils.Do(...)`, `Service.Find(...)`, and other no-brainers littering the space.

✔️ The naming of libraries, packages (assemblies), classes, methods, and even non-public _vars_ must be a **№1** challenge and involve the whole team<sup>:family:</sup> in discussions. 

The inevitable and noticeable expenses will pay off with the formation of ***lingua franca*** throughout the team and project, and ...
  
+ common comprehension of a domain, collaboration, and indeed bound team,
+ genuine design and self-descriptive code,
+ inspiration for behavior/domain-driven design,
+ escape from heaps of docs<sup>📒</sup>,
+ reduced efforts to get into a project for newcomers,
+ comfy navigation in the source code (incl. <kbd>CTRL+F</kbd>).

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<sup>:family:</sup><sub> The team means not only developers and managers but customers, testers with end users.</sub>\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<sup>📒</sup><sub> reqs/specs, DoU, meetings protocols, and primers - hard to follow but easy to misunderstand or forget but mostly neglected</sub>

### Categorization

Categoria
Naming couldn't be flat - it's an axiom, but categorization in software abstraction has two major challenges

* floating
*OOD.

TRAP: Duplicate names in the chain!


### Guidelines/Rules of thumb

* The higher the level of naming, the more attention.\
It's a routine to comb out    sdfsdf
* Name, apply, get feedback, refactor.
* At least two people with different backgrounds must confirm the top names.
* divide et empera

### Impedance with inherited domain names

// ToDescribe

# Wrapping up

Even top teams under time pressure and brakes on perfectionism would be barely proud of their implementation of naming. Then the naming (as [code quality](../../QA/README+/code-quality.md)) will never be perfect, but efforts to improve them must be continuous and genuine.

## Appendix 1 (of 3). Guidelines and Verbal Sins 

## Verbal sins

- **Grandiloquence** 

General words sound vague (if not bombastic) unless established in the domain. Compare florid `[Fact]` to modest `[TestCase]`. 

- **Unexpected match** 

`public utility`

- **Jargonism**

### Guidelines for methods

`Get` must be taboo within method names - either this must be property or a better description of the returned: `Read`, `Calculate` u.a.

🚧 .. TO BE CONTINUED ... 🚧

## Appendix 2 (of 2). Pabulum

### Active or passive voice

Document.print(), plotter.Print

## Appendix 3 (of 3). Learning from others

### Hall of fame

+ Core S[E]QL commands.

### Hall of shame

And 1st place goes to ... `dirty` used as the trait of a modified object.
