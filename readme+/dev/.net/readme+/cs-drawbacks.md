# C# drawbacks (minority report)

Nothing is perfect and C# too. The following language artifacts are awkward leastwise for me. 

## Syntax

- Rudimentary `;` ending a line brings nothing but visual noise.
- The `const` modifier shall be not limited to pre-compiled values (it's mere optimization) but prevent re-assignment, as `init` and `readonly` do.
- Missing (default) access modifier shall be better reserved for ultimate `private` or better `public` than for specific and less used `internal`\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<sup>:raising_hand:</sup>&nbsp;<sub>Well, this couldn't be changed<sub>
- Nullable declaration (with `?` prefix) is evident for value types but ambiguous for references and objects, which can be nulled anyway:\
`string a = null; string? b = null;`
- Gradual releases of syntax shortcuts, such as `?` or `!`, softly erode C# readability.\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<sup>:raising_hand:</sup>&nbsp;<sub>Quite arguably but with hope that C# team doesn't plan to make a Perl out of their language</sub>
  
### Generics

The next definition is laconic and clear `class CollWrapper<C, T> where C : ICollection<T> { ... }`, \
but not its redundant declaration `new CollWrapper<List<int>, int>()`.

&nbsp;&nbsp;&nbsp;&nbsp;<sup>:raising_hand:</sup>&nbsp;<sub>.NET team [admits](https://learn.microsoft.com/en-us/dotnet/csharp/programming-guide/generics/differences-between-cpp-templates-and-csharp-generics) that their generics are "_does nots_" of C++ templates.</sub>

## Types
  
Root `object`, both non-abstract and interface-less, asserts flaws in object-oriented design. On the other hand, it brings an "original" footprint, big enough to pollute coding space with names.

Either `class`, `record`, `record class`, `struct`, `record struct`, or *tuples* can declare an entity. Each has pros and cons for a particular case, but deciding between them could distract from design.

`Exception` can't be the return of a method, while `void` which will unconditionally throw is a declaration fail.

## Namespaces and class organization

* Historic namespaces as [System](https://learn.microsoft.com/en-us/dotnet/api/system) are bloated and mixed.
For example, exceptions should be organized in their own namespace with shorter calls: `Exceptions.Argument.Throw(predicate, message="")`.
* Classes like [Math](https://docs.microsoft.com/en-us/dotnet/api/system.math), [MathF](https://docs.microsoft.com/en-us/dotnet/api/system.mathf) shall be namespaces for granulated domain classes.

## Single-class inheritance

A class may refer to only a single base class but multiple interfaces with default method implementation. This dismantles arguing for conceptual single-class inheritance (which must have been technically restrained).

Alternatives with [extension methods](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/classes-and-structs/extension-methods) are pretty functional, while dynamic composition is beyond usual programming (though Roslyn has much facilitated it).

## Casting limitations

- [Named tuples](https://docs.microsoft.com/en-us/archive/msdn-magazine/2017/august/essential-net-csharp-7-0-tuples-explained) and anonymous objects are very handy to submit sporadic composed results, but can't cast to an interface or class.
- Neither implicit nor explicit downcasting works while JSON (de)serialization legally does this operation. Allowing this cast doesn't contradict type safety.

## Numbers
  
- Does either developer ponder ten(!) primitive whole types when writing ordinary `for (var i = 0; i < count; i++)`?
- Why 0.1 and 0.2 must be explicitly declared as `decimal` to accurately sum them up?

Developers should better declare just a *number* and distinguish only the way it's processed: fixed (default) or [floating-point arithmetic](https://docs.oracle.com/cd/E19957-01/806-3568/ncg_goldberg.html).

C#11 introduced [INumber](https://learn.microsoft.com/en-us/dotnet/api/system.numerics.inumber-1) which genericizes numbers but in a bulky and restricted fashion.

## String

Laconic `==` implies _ordinal_ _case-sensitive_ comparison while `String.Compare()` is bulky and turbid.
`IndexOf` and other methods with numerous overloads invoke comparison, for which Microsoft advises explicit `Comparison` options.\
Syntax shortcuts here could make the code both shorter and readable.

## Inborn naming

-  *Interface* is a too common term for contract (and not only in C#).
- *Reverse*, as in [LINQ method](https://learn.microsoft.com/de-de/dotnet/api/system.linq.enumerable.reverse), is actually *flip*.
- _out_ for [covariance](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/keywords/out-generic-modifier) collides with _out_ parameter modifier

...TO BE CONTINUED...
