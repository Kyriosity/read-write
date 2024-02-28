# Software - Naming 
<p dir="rtl"><i>"...In the beginning was the Word"</div></i></p><br/>
 

Naming is the most **meaningful**, **underrated**, and **neglected** activity in the realm of software. It's seen as granted when smoothly guides through the design and makes coding intuitive. CONTRARY, When names are confusing, bulky, redundant, or ambiguous - impeded comprehension and efforts are addressed to something else (complexity, legacy, learning curve, platform, and uniqueness).

Contrary, wading through the thorns of `Helpers`, `Service`, `Utils`, `Make()`, baobabs of bulky names, mirrors of ambiguity a developer will curse complexity, learning curve, platform, and else but not the naming.

## Practice

❎ False: naming is a derivative of development,

✔️ True: The naming of libraries, packages (assemblies), classes, methods, and even non-public _vars_ must be a **№1** challenge and involve the whole team<sup>:family:</sup> in discussions. This expense will pay off with *lingua franca* throughout the team and project, and ...
<details>
  <summary>... <b>Derived benefits</b></summary>
  
+ common comprehension of a domain, collaboration, and indeed bound team,
+ genuine design and self-descriptive code,
+ inspiration for behavior/domain-driven design,
+ escape from heaps of requirements, specs, DoU, and meetings protocols - hard to follow but easy to misunderstand or forget (but mostly neglected),
+ reduced efforts to get into a project for newcomers,
+ comfy navigation within the source code (with an IDE's explorer or <kbd>CTRL+F</kbd>).

 ---
 
</details>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<sup>:family:</sup><sub> The team here there aren't developers only but customers, testers, along with end users</sub>

## CATEGORIZATION !!!

## Rules of thumb

The higher the level of naming, the more attention.

## Verbal sins

- **Grandiloquence** 



General words will sound vague if not bombastic unless established in the domain. Compare florid `[Fact]` to modest `[TestCase]`. 

PUBLIC UTILITY

- **Jargonism**

### Guidelines for methods

`Get` must be taboo within method names - either this must be property or a better description of the returned: `Read`, `Calculate` u.a.

🚧 .. TO BE CONTINUED ... 🚧

# Wrapping up

Even top developers under time pressure and brakes on perfectionism will name logic classes as *services*, *helpers*, *utils*, *handlers* but would  be barely proud of that.

I mean that naming as [code quality](code-quality.md) can't be even perfect, but efforts to improve them must be genuine.

## Appendix 1 (of 1). Learning from others


### Hall of shame

And 1st place goes to ... `dirty` used as the property of a modified object may hold the 1st place.
