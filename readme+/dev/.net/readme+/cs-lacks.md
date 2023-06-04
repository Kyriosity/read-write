# Nice to have in C#

C#.NET isn't a universal formula, and its team **+** community don't posses unbounded resources. However this platform could offer extra features and foundations, which can only boost its charm.

## More base interfaces

General interface define members like `Count`, `Clone()`, `Equals()`, `CompareTo()`, which developers are eager to apply to their codes too.\
However much more remain uncovered, e.g. Max/Min for limiting collections and objects size.

Other promissing members (like `IsReadOnly`) are defined within specific interfaces.

## Basic exception, messages and guards

To begin with it could be proof of `>0` for collection sizing.

## Syntax

### Sugar

There's no excuse why shortcuts like `ArgumentNullException.ThrowIfNull(...)` aren't added to most exceptions. As well there're could be static classes without evident _Exception_ (e.g. NotImplemented.Throw()). 

### Enums inheritance

Seems logical and plain to adopt inheretance like this: 

<details>
<summary><b>Design sketch</b></summary>
    
```csharp
enum FundamentalState 
{
    Solid,
    Liquid,
    Gas,
    Plasma
}

enum AppliedTheoryState : FundamentalStates
{
    CrystallLiquid,
    BoseEinsteinCondensate,
    NeutronDegenerate,
    QuarkGluonPlasma,
}

[Flags]
enum MyLabReagentStates : FundamentalStates
{
    Unknown = 0,
    NotApplicable
}
```

with downcast only, e.g.:

```diff csharp
-  FundamentalState state = AppliedTheoryState.Gas;
+  AppliedTheoryState state = FundamentalState.Gas;
```
</details>

### Interfaces conjunction
Fine-granulated interfaces and their multi-inheritance into more substantial belong to sound design practices.

Another story is combination of primitive (or feature) interfaces as options for casting or *builders*.\
Suppose, there're `ILimited`, `ITimestamped` and `INotifyPropertyChanged` which combinations imply 2<sup>3</sup> nominal declarations. And what if this could be done with `<IInterfaceA, IInterfaceB[, IInterfaceC[, ...]]>`

<details>
<summary><b>Design sketch</b></summary>

```csharp
static class AircraftBuilder
{
        static <IAirSpecs, IPowerplant> BusinessJet(...) { ... }
        static <IAirSpecs, IPowerplant, ILoadSpecs> Cargo(...) { ... }
        static <IAirSpecs, IPowerplant, ILoadSpecs, IPassengerConfig> Liner(...) { ... }
}

IList<IataAirportCode> Planning.Destinations.FindOptimal(IataAirportCode from, <IAirSpecs, IPowerplant> vehicle) { ... }
void Planning.Capacity.Register(<ILoadSpecs, IPassengerConfig> transport) { ... }

```
</details>

Such feature will be also useful for run-time object composition.

## Math
Native [Math](https://docs.microsoft.com/en-us/dotnet/api/system.math) is pretty scarce, and 3d-party libraries aren't in the state of the art.

C# would only profit with a lightweight assembly which could: 
+ itemize more [constants](https://en.wikipedia.org/wiki/Mathematical_constant)
+ provide more useful functions (there're myriads uncovered)
+ approximate popular irrational values like π (Pi) to requested length
+ generate and check numbers in [sequences](http://oeis.org/wiki/Welcome) (`bool Prime.Has(ulong num)`), detect sequences
+ introduce complex numbers
+ parallelize, async heavy algorithms with progress report and cancellation option

## Measurement systems
Definition of natural values (geometry, masses, temperature, elictricity, movement u.a.) and their conversions between systems of measurements (metric, US customary, UK imperial u.a.) are more than essential tools (e.g., Celsius-Fahrenheit-Kelvin).

I've outlined custom [Typescript framework](../../../../../../convert-smth) but hope that Microsoft one day will promote a sound multi-platform pluggable<sup>:electric_plug:</sup> framework.\
&nbsp;&nbsp;&nbsp;&nbsp;<sup>:electric_plug:</sup><sub>since no framework will cover all diversities of physical values and systems (especially custom), and there must be "templates" to add own definitions</sub>

## Lingua
Let's take some output from fictitious tree search `$"Branches: {found}, ≥ leaves: {cutoff}"`. That can be quickly refactored for narrative or voice generator:\
`$"{found} {(1 == found ? "branch has" : "branches have")} no less than {cutoff} {(1 == cutoff ? "leaf" : "leaves")}"`

If an application will generate much multi-language text it won't be a big deal to implement
<details>
<summary><u>Blueprint of pluralization utility</u></summary>

```csharp
namespace Lingua.Grammar;

interface INumbered
{
    string Count(long num);
    string Count(double num);
}

interface IPluralForms {
    INumbered Plural((string singular, string plural) forms, string culture = "");
    INumbered Dual((string singular, string dual, string plural) forms, string culture = "");
    INumbered Trial((string singular, string dual, string trial, string plural) forms, string culture = "");
    INumbered Paucal((string singular, string paucal, string plural) forms, string culture = "");
    INumbered Custom(string[] forms, Func<long, int> indexWhole, Func<double, int>? indexFractional = null);
}
```

</details>

However
- this reinvents the wheel,
- there're other forms of grammatical number besides plurals,
- numbering is only a share of grammatical agreements in every single tongue,
- linguistics goes far beyond competence in few tongue families.

And what if .NET foundation classes could:
- neatly formulate declensions, conjugation and other formations,
- define constants for unfamiliar forms of loanwords (greek, latin u.a.),
- revise habitual [CultureInfo](https://docs.microsoft.com/en-us/dotnet/api/system.globalization.cultureinfo) (classify tongue families and default agreements)

And, not least, add syntax sugar like
<details>
<summary><b>Proposal for grammar interpolation</b></summary>
&nbsp;&nbsp;`${number [: [format] : [forms] : []] }`, where

&nbsp;&nbsp;&nbsp;&nbsp;*number* is whole or fractional subject\
&nbsp;&nbsp;&nbsp;&nbsp;*format* specifies usual format or to put in words\
&nbsp;&nbsp;&nbsp;&nbsp;*forms* - grammar forms as in imaginary `INumbered` in the snippet above
</details>
