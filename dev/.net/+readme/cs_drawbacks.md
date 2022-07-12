# Nothing is perfect and C# too
C# team has an ear for [proposals](https://github.com/dotnet/csharplang/tree/main/proposals), but some personal are:
## Concepts
Non-abstract `object` asserts flaws in object-oriented design. On the other hand `object` brings "original" footprint, big enough to pollute coding space.

To declare an entity `class`, `record`, `record class`, `struct`, `record struct`, *tuples* 

## Syntax
Rudimentary `;` ending a line brings nothing but visual noise.

Gradual releases of syntax shortcuts, as `?` or `!`, sometimes erode C# readability.<sup>:raising_hand:</sup>

&nbsp;&nbsp;&nbsp;&nbsp;<sup>:raising_hand:</sup><sub>Quite arguably, and i hope that C# team doesn't plan to make a Perl out of their language</sub>

Nullable variants of declaration (the `?` prefix) are unambiguous for value types but not for references and objects, which can be nulled anyway.

The `const` modifier shall be not limited to pre-compiled values (it's mere optimization) but prevent further assignment, as `init` and `readonly` do.

[Named tuples](https://docs.microsoft.com/en-us/archive/msdn-magazine/2017/august/essential-net-csharp-7-0-tuples-explained) are very handy to return sporadic composed results, but can't cast to an interface. As well - anonymous objects.

Much of topic classes as [Math](https://docs.microsoft.com/en-us/dotnet/api/system.math) shall be namespaces rather than uniting classes.

## Numbers
Will one weigh ten(!) predefined integral types to write a line like `for (var i = 0; i < ; i++)`?\
Why 0.1 and 0.2 must be explicitly declared with awkward `decimal` to accurately sum them up?

Actually a developer can declare just a *number* and distinguish only the way it's processed: fixed or [floating-point arithmetic](https://docs.oracle.com/cd/E19957-01/806-3568/ncg_goldberg.html).

## String
Laconic `==` implies ordinal case-sensitive comparison while `String.Compare()` is bulky and turbid.
`IndexOf` and other methods with numerous overloads invoke comparison, for which Microsoft advises explicit `Comparison` options.\
Syntax shortcuts here could do the code both shorter and readable.

## Nice to have
### APIs to other languages
IronPython is neglected, and there's no descent lib to make a bridge to execute Linux-targeted python code snippets.

### Math
C# [Math](https://docs.microsoft.com/en-us/dotnet/api/system.math) is pretty scarce, and 3d-party libraries aren't in the state of the art.

C# would only profit with a lightweight assembly which could: 
+ list more [constants](https://en.wikipedia.org/wiki/Mathematical_constant)
+ provide more useful functions (there're tons uncovered)
+ varying length for irrational values like Pi
+ generate and check numbers in [sequences](http://oeis.org/wiki/Welcome) (`bool Prime.Has(ulong num)`), detect sequences
+ introduce complex numbers
+ parallelize, async heavy algorithms with progress report and cancellation option

### Basic exception, messages and guards


### Lingua

### Auto-removable temp files
