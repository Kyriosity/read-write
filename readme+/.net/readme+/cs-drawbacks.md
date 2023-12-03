# C# - Drawbacks (minority report)

Nothing anthropogenic could be perfect and C# too. The following language artifacts are awkward leastwise for me. 

## Syntax

- Rudimentary `;` ending a line brings nothing but visual noise.
- Constructor names imply extra refactoring on class/struct renaming (could be independent `ctor()`, `this()`). Take the "untitled" `base()` call in the same constructors.
- Rudimentary `0` as the start index in collections<sup>:o:</sup>, which doesn't correlate with the count and shall better start from `1`.
- Missing (default) access modifier<sup>:o:</sup> shall be better reserved for ultimate `private` or better `public` than for specific and less used `internal`
- The `const` modifier shall be not limited to pre-compiled values (it's mere optimization) but prevent re-assignment, as `init` and `readonly` do.
- Nullable declaration (with `?` prefix) is evident for value types but ambiguous for references and objects, which can be nulled anyway:\
`string a = null; string? b = null;`
- Gradual releases of syntax shortcuts, such as `?` or `!`, softly erode C# readability.<sup>🙋</sup>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<sup>:o:</sup> <sub>Such native features can't be changed.</sub>\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<sup>:raising_hand:</sup>&nbsp;<sub>I assume arguability but hope that C# team doesn't plan to make a Perl out of their language</sub>
  
### Generics

The next definition is laconic and clear `class CollWrapper<C, T> where C : ICollection<T> { ... }`, but not its redundant declaration `new CollWrapper<List<int>, int>()`.

Advanced C# design reveals more generic restraints and consequent *Vodoo programming* to workaround them.<sup>🙋</sup>

&nbsp;&nbsp;&nbsp;&nbsp;<sup>:raising_hand:</sup>&nbsp;<sub>.NET team [admits](https://learn.microsoft.com/en-us/dotnet/csharp/programming-guide/generics/differences-between-cpp-templates-and-csharp-generics) that their generics are "_does nots_" of C++ templates.</sub>

## Types
  
- Root `object`, both non-abstract and interface-less, asserts flaws in object-oriented design. On the other hand, it brings an "original" footprint, big enough to pollute coding space with names.

- Either `class`, `record`, `record class`, `struct`, `record struct`, or *tuples* can declare an entity. Each has pros and cons for a particular case, but deciding between them could distract from design.

- There's no method signature to specify that it must unconditionally throw an exception, and `void` as a return is incorrect.\
(The workaround may be to [declare the return as an exception to be thrown](cs-hints.md#Gimmicks)).

## Namespaces and class organization

* Historic namespaces as [System](https://learn.microsoft.com/en-us/dotnet/api/system) are bloated and mixed.
For example, exceptions should be organized in their own namespace with shorter calls: `Exceptions.Argument.Throw(predicate, message="")`.
* Classes like [Math](https://docs.microsoft.com/en-us/dotnet/api/system.math), [MathF](https://docs.microsoft.com/en-us/dotnet/api/system.mathf) shall be namespaces for granulated domain classes.

## Single-class inheritance

A class may refer to only a single base class but multiple interfaces with default method implementation. This dismantles arguing for conceptual single-class inheritance (which must have been technically restrained).

Alternatives with [extension methods](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/classes-and-structs/extension-methods) are pretty functional, while dynamic composition is beyond usual programming (though Roslyn has much facilitated it).

## Casting limitations

- [Named tuples](https://docs.microsoft.com/en-us/archive/msdn-magazine/2017/august/essential-net-csharp-7-0-tuples-explained) and anonymous objects are very handy to submit sporadic composed results, but can't cast to an interface or class.
- Neither implicit nor explicit downcasting works while JSON (de)serialization legally does this operation. Allowing this cast doesn't contradict type safety.\
ToDo: an example with [contravariance](https://learn.microsoft.com/en-us/dotnet/standard/generics/covariance-and-contravariance)

## Numbers
  
- Does either developer ponder ten(!) primitive whole types when writing ordinary `for (var i = 0; i < count; i++)`?
- Summing up 0.1 and 0.2 will reveals a [floating arithmetic flaw](https://docs.oracle.com/cd/E19957-01/806-3568/ncg_goldberg.html) unless explicitly declared decimal (just debug `var roundErr = 0.1 + 0.2;` to prove).

Developers should better declare just a *number* and distinguish only the way it's processed: fixed (default) or [floating-point arithmetic](https://docs.oracle.com/cd/E19957-01/806-3568/ncg_goldberg.html).

C#11 introduced [INumber](https://learn.microsoft.com/en-us/dotnet/api/system.numerics.inumber-1) which genericizes numbers but in a bulky and restricted fashion.

## String

Laconic `==` implies _ordinal_ _case-sensitive_ comparison while `String.Compare()` is bulky and turbid.
`IndexOf` and other methods with numerous overloads invoke comparison, for which Microsoft advises explicit `Comparison` options.\
Syntax shortcuts here could make the code both shorter and readable.

## Inborn naming

-  *Interface* is a too common term for contracts (and not only in C#).
- *Reverse*, as in [LINQ method](https://learn.microsoft.com/de-de/dotnet/api/system.linq.enumerable.reverse), is actually *flip*.
- Type modifiers _in_/_out_ for contra-/covariance collide with the same name parameter modifiers (_more_/_less_ can be better)

... TO BE CONTINUED ...
