
# Naming in software design

The naming of libraries, packages (assemblies), classes, methods and even non-public _vars_ **must** be a №1 challenge and involve the whole team<sup>:family:</sup> into discussions. This expense will pay off with *lingua franca* througout the team and project, and ...
<details>
  <summary>... derived benefits</summary>
  
+ common comprehension of a domain, collaboration and indeed bound team
+ genuine design and self-descriptive code
+ inspiration for behavior/domain driven design
+ escape from heaps of reqs and specs - hard to follow but easy to misunderstood, forget (but mostly neglected)
+ reduced efforts to get into a project for newcomers
+ comfy navigation within the source code (both with IDE's explorer and CTRL+F)
 
</details>


&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<sup>:family:</sup><sub>&nbsp;&nbsp;The team here there is'nt only developers but customers, testers, along with end users</sub>

## Verbal sins

Even top developers under time pressure and brakes on perfectionism will name logic classes as *services*, *helpers*, *utils*, *handlers* but would 
be barely proud of that.

General words, if not from domain, will sound vague if not bombastic. Compare `[Fact]` against modest `[TestCase]`. 

### Guidelines for methods

`Get` must be taboo within method names - either this must be property or better desription of the returned: `Read`, `Calculate` u.a.

🚧 .. TO BE CONTINUED ... 🚧
