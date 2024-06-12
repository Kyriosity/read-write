# Software - Naming 

<p dir="rtl"><i>"...In the beginning was the Word"</div></i></p><br/>

 
Naming is the most **meaningful**, **underrated**, and **neglected** activity in the realm of software. It's seen as granted when it smoothly guides through the design and makes coding intuitive. 

On the contrary, wading through the thorns of poorly named and labyrinths of poorly categorized code, abatis of docu a developer will curse application complexity, learning curve, technologies used, and fate but not the naming.

## How to...

:x: Usual: Naming as a derivative of development, which spawns `Helper.Get(..)`, `Utils.Do(...)`, `Service.Find(...)`, and other no-brainers littering the space.

✔️ The naming of libraries, packages (assemblies), classes, methods, and even non-public _vars_ must be a **№1** challenge and involve the whole team<sup>:family:</sup> in discussions. 

The inevitable and noticeable expenses will pay off with ***lingua franca*** throughout the team and project, and ...
  
+ common comprehension of a domain, collaboration, and indeed bound team,
+ genuine design and self-descriptive code,
+ inspiration for behavior/domain-driven design,
+ escape from heaps of docs<sup>📒</sup>,
+ reduced efforts to get into a project for newcomers,
+ comfy navigation in the source code (even with <kbd>CTRL+F</kbd>).

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<sup>:family:</sup><sub> The team here there aren't developers only but customers, testers, along with end users</sub>\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<sup>📒</sup><sub> reqs/specs, DoU, meetings protocols, and primers - hard to follow but easy to misunderstand or forget but mostly neglected</sub>

## Categorization

Naming couldn't be flat - it's an axiom, but categorization in software abstraction has two major challenges

* floating
*OOD.

TRAP: Duplicate names in the chain!

## Rules of thumb

The higher the level of naming, the more attention.

Name, apply, get feedback, refactor.

There must be at least two with different backgrounds to confirm top names.

# Wrapping up

Even top developers under time pressure and brakes on perfectionism would be barely proud of their implementation of naming.

I mean that the naming as [code quality](code-quality.md) can't be perfect, but efforts to improve them must be genuine.

## Appendix 1 (of 2). Guidelines and Verbal Sins 

## Verbal sins

- **Grandiloquence** 

General words will sound vague if not bombastic unless established in the domain. Compare florid `[Fact]` to modest `[TestCase]`. 

- **Unexpected match** 

`public utility`

- **Jargonism**

### Guidelines for methods

`Get` must be taboo within method names - either this must be property or a better description of the returned: `Read`, `Calculate` u.a.

🚧 .. TO BE CONTINUED ... 🚧

## Appendix 2 (of 2). Learning from others

### Hall of fame

+ Core S[E]QL commands.

### Hall of shame

And 1st place goes to ... `dirty` used as the trait of a modified object.
