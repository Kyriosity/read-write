# C# - Drawbacks - "Minority report"

Artworks can be perfect &mdash; not technologies. With all its goodies __C#__ has downsides as bulky declarations of hierarchies, rigid interfaces, and notably restrained generics.

The following language artifacts are awkward leastwise for me. 

## Syntax

- Rudimentary `;` ending a line brings nothing but visual noise.
- Constructor names imply extra refactoring on class/struct renaming (could be independent `ctor()`, `this()`). Take the "untitled" `base()` call in the same constructors.
- Rudimentary `0` as the start index in collections<sup>:o:</sup>, which doesn't correlate with the count and shall better start from `1`.
- Default (when missing)  access modifier<sup>:o:</sup> shall be better reserved for "ultimate" `private` or  `public` than for less EXPLICIT and  less used `internal`
- The `const` modifier shall not be limited to pre-compiled values (as in intermediate languages) but prevent re-assignment, as `init` and `readonly` do.
- No constant option for default values in signatures.\
`Do(int val, string rem=string.empty)`
- Nullable declaration (with `?` prefix) is evident for value types but ambiguous for references and objects, which can be nulled anyway:\
`string a = null; string? b = null;`
- a perplexing extension of nullable as `((int?)1).Value` and `((bool?)true).HasValue`<sup>❔</sup>.

Gradual releases of syntax shortcuts, such as `?` or `!`, silently erode C# readability.<sup>🙋</sup> While shortcuts as `[]` for empty colls are rational and eye-pleasing.

\_______________

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<sup>:o:</sup> <sub>These native features can't be changed.</sub>\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<sup>:raising_hand:</sup>&nbsp;<sub>Though this paces and hopefully .NET team doesn't plan to make a Perl out of their language</sub>\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<sup>❔</sup> <sub>Isn't `null` a value too?</sub>

### Generics - limitations

The next definition is terse and clear `class CollWrapper<C, T> where C : ICollection<T> { ... }` but not the redundancy in its declaration `new CollWrapper<List<int>, int>()`.

Advanced C# design reveals more generic restraints and results in *Vodoo programming* to workaround them.<sup>🙋</sup>

&nbsp;&nbsp;&nbsp;&nbsp;<sup>:raising_hand:</sup>&nbsp;<sub>.NET team [admits](https://learn.microsoft.com/en-us/dotnet/csharp/programming-guide/generics/differences-between-cpp-templates-and-csharp-generics)<sup>:link:</sup> that their generics are "_does nots_" of C++ templates.</sub>

### Fishy shortcuts

Some shortcuts obfuscate original goodies with insignificant gains in size.

For example, [`EnsureSuccessStatusCode`](https://learn.microsoft.com/en-us/dotnet/api/system.net.http.httpresponsemessage.ensuresuccessstatuscode) is better in its natural form:

```csharp
if (response.IsSuccessStatusCode) /// or differentiate for more specific conditions
     throw new HttpRequestException(); /// or specify explicitly any custom exception
```

## Type system
  
- Root `object`, both non-abstract and interface-less, asserts flaws in object-oriented design<sup>🐡</sup>. On the other hand, it brings an "original" footprint, big enough to pollute coding space with names.<sup>👣</sup>

- Either `class`, `record`, `record class`, `struct`, `record struct`, or *tuples* can declare an entity. Each has pros and cons for a particular case, but deciding between them could distract from design.

- There's no method signature to specify that it must unconditionally throw an exception, and `void` as a return is incorrect.\
(The workaround may be to [declare the return as an exception to be thrown](cs-hints.md#Gimmicks)).

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<sup>🐡</sup> <sub>Besides, the override of dummy `Equals()` and `ToString()` may bring nontrivial logic and violate _single responsibility_.</sub>\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<sup>👣</sup> <sub>Especially annoying in inter-methods within builders, when you expect to select among next steps.</sub>

## Single-class inheritance

A class may refer to only one base class but multiple interfaces with default method implementations. This dismantles arguing for conceptual single-class inheritance (which must have been technically restrained).

However, arranging the code from some interfaces is rather cumbersome and restrictive, and shall be reserved for limited technical purposes (not multiinheritance design).

Other peculiar and arbitrary alternatives are [extension methods](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/classes-and-structs/extension-methods)<sup>:link:</sup> and dynamic composition (notably facilitated with [Roslyn](https://weblog.west-wind.com/posts/2022/Jun/07/Runtime-CSharp-Code-Compilation-Revisited-for-Roslyn)<sup>:link:</sup>).

&nbsp;&nbsp;&nbsp;&nbsp;<sup>🙋</sup> <sub>I do object multi-inheritance for logic as destructive for single-responsibility but would like it for operational adornment: `ToString()`, `NotifyPropertyChanged`, `Compare` and similar.</sub>

## Namespaces and class organization

* Historic namespaces as [`System`](https://learn.microsoft.com/en-us/dotnet/api/system) are bloated and mixed.
First of all, numerous errors should be moved from `System` to their own `namespace Exception`.__*__
* Classes like [`Math`](https://docs.microsoft.com/en-us/dotnet/api/system.math), [`MathF`](https://docs.microsoft.com/en-us/dotnet/api/system.mathf) shall be namespaces for granulated domain classes.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;__*__<sub> System.SystemException => Exception.System</sub>

## Casting limitations

- [Named tuples](https://docs.microsoft.com/en-us/archive/msdn-magazine/2017/august/essential-net-csharp-7-0-tuples-explained)<sup>:link:</sup> and anonymous objects are very handy to submit sporadic composed results, but can't cast to an interface or class.
- Some obvious inheritance is missing (e.g. can't cast `DateTime` to `DateOnly`).
- Neither implicit nor explicit downcasting works while JSON (de)serialization legally does this operation.\
Allowing this cast doesn't contradict type safety.\
ToDo: an example with [contravariance](https://learn.microsoft.com/en-us/dotnet/standard/generics/covariance-and-contravariance)<sup>:link:</sup>

## Built-in and shipped types 

### Numbers
  
- Does either developer ponder ten(!) primitive whole types when writing ordinary `for (var i = 0; i < count; i++)`?
- Summing up 0.1 and 0.2 will reveal a [floating arithmetic flaw](https://docs.oracle.com/cd/E19957-01/806-3568/ncg_goldberg.html)<sup>:link:</sup> unless explicitly declared decimal.<sup>🪲</sup>\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<sup>🪲</sup> Debug `var roundErr = 0.1 + 0.2;` to prove.

Developers should better declare just a *numeric* and distinguish only the way it's processed: fixed (default) or floating. It would be a great option to derive subclasses from this _numeric_ could (with range and precision constraints).

C#11 introduced [INumber](https://learn.microsoft.com/en-us/dotnet/api/system.numerics.inumber-1)<sup>:link:</sup> which genericizes numbers but in a bulky and restricted fashion.<sup>🙋</sup>

### String

Laconic `==` implies _ordinal_ _case-sensitive_ comparison while `String.Compare()` is bulky and turbid.
`IndexOf` and other methods with numerous overloads invoke comparison, for which Microsoft advises explicit `Comparison` options.

Syntax shortcuts here could make the code both shorter and readable.

### DateTime

`DateTime` and refined `DateOnly` (non-casting from the first) are error-prone, awkward and limited. 
Ironically you may specify a date close to the year 9999 (when only regular astronomical events can be predicted that precise) but not a recorded one before [Common Era](https://en.wikipedia.org/wiki/Common_Era)<sup>🔗</sup>.

Ambiguous order and `int` input of year/month/day allows nonsense values, which only the running code may or may not detect (_viz_. a bad bug).<sup>🐛</sup>.

&nbsp;&nbsp;&nbsp;&nbsp;<sup>🐛</sup> <sub>Test initalization and `.Tostring()` with `new DateOnly(2023, 02, 29)`, `new DateOnly(31, 12, 1975)`, `var May = 5; new DateOnly(2007, 1, May)`, `new DateTime(0, 0, 0)`</sub>

Continued in [C# lacks - Dates](parts/cs-lacks-parts.md#Dates).

## Inborn naming

-  *Interface* is a term that is too common for contracts (not only in C#).
- LINQ [`Revers()`](https://learn.microsoft.com/de-de/dotnet/api/system.linq.enumerable.reverse), is actually *flip*.
- Type modifiers _in_/_out_ for contra-/covariance collide with the same name parameter modifiers (_more_/_less_ can be better)

## 🚧 To be continued ...

The list is far from being complete and I wait for one day (better to say a decade) when .NET hits a higher note - D-flat or even D#.

🔚
