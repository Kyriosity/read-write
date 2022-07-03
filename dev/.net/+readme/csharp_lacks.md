# C# drawbacks
Nothing is perfect whereas C# hasn't been monumentally accomplished. Team of .NET has an ear for numerous [proposals](https://github.com/dotnet/csharplang/tree/main/proposals), but if i dare to express some worries offhand...

## Syntax
Semicolon `;` ending a line is a rudiment, adding up to visual noise.

Gradual releases of syntax shortcuts, as `??` or `!!`, erode C# readability.<sup>:raising_hand:</sup>

&nbsp;&nbsp;&nbsp;&nbsp;<sup>:raising_hand:</sup><sub>Quite arguably, and i hope that C# team doesn't plan to make new Perl out of their language</sub>

## Declarations
The 'object' as a non-abstract class asserts flaws in OOD.

Nullable variants of declaration (the `?` prefix) works fine for value types, but is ambiguous for references and objects, which can be nulled anyway.

The `const` modifier shall be not limited to pre-compiled values (it's mere optimization) but prevent further assignment, as `init` and `readonly` do.

[Named tuples](https://docs.microsoft.com/en-us/archive/msdn-magazine/2017/august/essential-net-csharp-7-0-tuples-explained) are very handy to return sporadic composed results, but can't cast to an interface. As well - anonymous objects.

[Math](https://docs.microsoft.com/en-us/dotnet/api/system.math) shall be a namespace rather than uniting class.

## Numbers
Will one weigh ten(!) predefined integral types to write a line like `for (var i = 0; i < ; i++)`?\
Why to accurately sum up 0.1 and 0.2 those must be explicitly declared with awkward `decimal` ?

Actually a developer can declare just a *number* and distinguish only the way it's processed: fixed or [floating-point arithmetic](https://docs.oracle.com/cd/E19957-01/806-3568/ncg_goldberg.html).

## String
Laconic `==` implies ordinal case-sensitive comparison while `String.Compare()` is bulky and turbid.
`IndexOf` and other methods with numerous overloads invoke comparison, for which Microsoft advises explicit `Comparison` options.\
Syntax shortcuts would be warmly welcomed here.

## Nice to have
### Math
[Math](https://docs.microsoft.com/en-us/dotnet/api/system.math) class offers little of functions and only three constants. External libraries aren't in state of the art.
C# could only profit with a lightweight assembly which will provide more functions, more constants, varying length values like Pi.

### Auto-removable temp files

### Native reactive

