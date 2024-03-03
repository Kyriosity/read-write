# Software - Naming 
<p dir="rtl"><i>"...In the beginning was the Word"</div></i></p><br/>

 
Naming is the most **meaningful**, **underrated**, and **neglected** activity in the realm of software. It's seen as granted when it smoothly guides through the design and makes coding intuitive. 

On the contrary, wading through the thorns of poorly named and labyrinths of poorly categorized code a developer will curse application complexity, learning curve, technologies used, and fate but not the naming.

## Practice

:x: Usual: Naming as a derivative of development, which spawns `Helper.Get(..)`, `Utils.Do(...)`, `Service.Find(...)`, and other no-brainers littering the space.

✔️ The naming of libraries, packages (assemblies), classes, methods, and even non-public _vars_ must be a **№1** challenge and involve the whole team<sup>:family:</sup> in discussions. This expense will pay off with ***lingua franca*** throughout the team and project, and ...
  
+ common comprehension of a domain, collaboration, and indeed bound team,
+ genuine design and self-descriptive code,
+ inspiration for behavior/domain-driven design,
+ escape from heaps of requirements, specs, DoU, and meetings protocols - hard to follow but easy to misunderstand or forget (but mostly neglected),
+ reduced efforts to get into a project for newcomers,
+ comfy navigation within the source code (with an IDE's explorer or <kbd>CTRL+F</kbd>).

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<sup>:family:</sup><sub> The team here there aren't developers only but customers, testers, along with end users</sub>

## Categorization

Naming couldn't be flat - it's an axiom, but categorization in software abstraction has two major challenges

* floating
*OOD.

## Rules of thumb

The higher the level of naming, the more attention.

Name, apply, get feedback, refactor.

There're must be at least two with different background to confirm top names.

# Wrapping up

Even top developers under time pressure and brakes on perfectionism would be barely proud of their implementation of naming.

I mean that naming as [code quality](code-quality.md) can't be even perfect, but efforts to improve them must be genuine.

## Appendix 1 (of 2). Guideliens and Verbal sins 

## Verbal sins

- **Grandiloquence** 

General words will sound vague if not bombastic unless established in the domain. Compare florid `[Fact]` to modest `[TestCase]`. 

- **Match** 

`public utility`

- **Jargonism**

### Guidelines for methods

`Get` must be taboo within method names - either this must be property or a better description of the returned: `Read`, `Calculate` u.a.

🚧 .. TO BE CONTINUED ... 🚧

## Appendix 2 (of 2). Learning from others

### Hall of fame

### Hall of shame

And 1st place goes to ... `dirty` used as the property of a modified object may hold the 1st place.
