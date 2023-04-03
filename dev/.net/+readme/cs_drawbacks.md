# C# drawbacks (minority report)

Nothing is perfect and C# too. Following language artifacts are awkward leastwise for me. 

## Syntax

- Rudimentary `;` ending a line brings nothing but visual noise.
- The `const` modifier shall be not limited to pre-compiled values (it's mere optimization) but prevent re-assignment, as `init` and `readonly` do.
- Missing (default) access modifier shall be better reserved for ulitimate `private` or better `public` than for specific and less used `internal`\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<sup>:raising_hand:</sup>&nbsp;<sub>Well, this couldn't be changed<sub>
- Nullable declaration (with `?` prefix) is evident for value types but ambiguous for references and objects, which can be nulled anyway:\
`string a = null; string? b = null;`
- Gradual releases of syntax shortcuts, as `?` or `!`, sometimes erode C# readability.\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<sup>:raising_hand:</sup>&nbsp;<sub>Quite arguably, and i hope that C# team doesn't plan to make a Perl out of their language</sub>

## Types
Root `object`, both non-abstract and interface-less, asserts flaws in object-oriented design. On the other hand it brings "original" footprint, big enough to pollute coding space.

Either `class`, `record`, `record class`, `struct`, `record struct` or *tuples* can declare an entity. Each has pros and cons for particular case, but deciding between them could distract from design.

## Namespaces and class organization
- Historic namespaces as [System](https://learn.microsoft.com/en-us/dotnet/api/system) are bloated and mixed.
For example, exceptions should be organized in own namespace with shorter names: `throw new Exceptions.NotImplemented()`.
- Classes like [Math](https://docs.microsoft.com/en-us/dotnet/api/system.math), [MathF](https://docs.microsoft.com/en-us/dotnet/api/system.mathf) shall be namespaces for granulated domain classes.

## Lack of multi-class inheritance
Ability to implement multiple interfaces dismantles reasoning of conceptual single-class inheritance (which must have been technically restrained).\
Alternatives with [extension methods](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/classes-and-structs/extension-methods) are pretty functional, while dynamic composition is malformed performance hammer.

## Casting limitations
- [Named tuples](https://docs.microsoft.com/en-us/archive/msdn-magazine/2017/august/essential-net-csharp-7-0-tuples-explained) and anonymous objects are very handy to submit sporadic composed results, but can't cast to an interface or class.
- Neither implicit nor explicit downcasting works while JSON (de)serialization legally does this operation. Allowing this cast doesn't contradict type safety.

## Numbers
- Will either developer ponder ten(!) primitive whole types to write ordinary `for (var i = 0; i < count; i++)`?
- Why 0.1 and 0.2 must be explicitly declared as `decimal` to accurately sum them up?

Actually a developer can declare just a *number* and distinguish only the way it's processed: fixed (default) or [floating-point arithmetic](https://docs.oracle.com/cd/E19957-01/806-3568/ncg_goldberg.html).

C#11 introduced [INumber](https://learn.microsoft.com/en-us/dotnet/api/system.numerics.inumber-1) which genericizes numbers but in bulky and restricting fashion.

## String
Laconic `==` implies _ordinal_ _case-sensitive_ comparison while `String.Compare()` is bulky and turbid.
`IndexOf` and other methods with numerous overloads invoke comparison, for which Microsoft advises explicit `Comparison` options.\
Syntax shortcuts here could do the code both shorter and readable.

## Inborn naming
-  *Interface* is too much common term.
- *Reverse*, as in [LINQ method](https://learn.microsoft.com/de-de/dotnet/api/system.linq.enumerable.reverse), is actually *flip*.

...TO BE CONTINUED...
