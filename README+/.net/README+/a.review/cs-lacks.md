# C# - Nice to have - Syntax, constructs and features

C#.NET isn't a universal formula; its team **+** community doesn't possess unbounded resources. However, this platform could offer extra features and foundations, which can only boost its charm.

## More base interfaces

The general interface defines members like `Count`, `Clone()`, `Equals()`, `CompareTo()`, which developers are eager to apply to their codes too.\
However much more remains uncovered, e.g. Max/Min for limiting collections and object size.

Other promising members (like `IsReadOnly`) are defined within specific interfaces.

## Basic exceptions, messages, and guards

To begin with, it could be proof of `>0` for collection sizing, though subclassing of general numeric type will be better.

## Syntax

### Sugar

There's no excuse why shortcuts like `ArgumentNullException.ThrowIfNull(...)` aren't added to most exceptions. 
As well there could be static classes without evident _Exception_ suffix (e.g. `NotImplemented.Throw()`). 

GUARDS and LINKE to USE-DEV !!!!!!!!!!!!!!!

### Extra inheritance

<details>
<summary><ins>&nbsp;<b>Enum</b> - Design sketch&nbsp;</ins></summary>
&nbsp;

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

---

</details>

<details>
<summary><ins>&nbsp;<b>Arguments signature</b> - Design sketch&nbsp;</ins></summary>
&nbsp;

Let's put aside that long signatures are bugs buddies and shall be encapsulated into classes/structs or tuples. 

Let's take the fact that repetitive sequences of arguments occur (sometimes dicatated by external tools) and ensuring the same names in order would be pleasing.

```csharp

// one of possible syntax through attribute
[Args("Name")]
bool Login(string name, string familyName) { ... }

[Args("Name.Western")]
void Personalize([Name], string middleName, Degree title) { ... }

Guid Register(int attempt, [Name.Western], byte age) { ... }

```

</details>

### Interfaces conjunction

Fine-granulated interfaces and their multi-inheritance into more substantial belong to sound design practices.

Another story is a combination of primitive (or feature) interfaces as options for casting or *builders*.\
Suppose, there're `ILimited`, `ITimestamped`, and `INotifyPropertyChanged` which combinations imply 2<sup>3</sup> nominal declarations. And what if this could be done with `<IInterfaceA, IInterfaceB[, IInterfaceC[, ...]]>`

<details>
<summary><b><ins>&nbsp;Design sketch&nbsp;</ins></b></summary>
&nbsp;
    
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
---

</details>

Such a feature will be useful also for run-time object composition.

## Math

Native [Math](https://docs.microsoft.com/en-us/dotnet/api/system.math)<sup>🔗</sup> is pretty scarce, and 3d-party libraries aren't in the state of the art.

C# would only profit from a lightweight assembly that could: 

+ inventory more [constants](https://en.wikipedia.org/wiki/Mathematical_constant)<sup>🔗</sup>,
+ provide more useful functions (there are myriads uncovered),
+ approximate popular irrational values like π (Pi) to the requested length,
+ generate and check numbers in [sequences](http://oeis.org/wiki/Welcome)<sup>🔗</sup> (`bool Prime.Has(ulong num)`), detect sequences,
+ introduce complex numbers,
+ parallelize, async heavy algorithms with progress report and cancellation option

<ins>&nbsp;**Further nice-to-have:**&nbsp;</ins>\
|- [Parts and frameworks](cs-lacks-parts.md)

