# C# - Nice to have - Syntax, constructs and features

C#.NET isn't a universal formula; its team with community assistance doesn't possess unbounded resources. However, this platform could offer extra features and foundations, which can only boost its charm.

## More base interfaces

The general interface defines members like `Count`, `Clone()`, `Equals()`, `CompareTo()`, which developers are eager to apply to their codes too.\
However much more remains uncovered, e.g. Max/Min for limiting collections and object size.

Other promising members (like `IsReadOnly`) are defined within specific interfaces.

## Basic exceptions, messages, and guards

To begin with, it could be proof of `>0` for collection sizing, though subclassing of general numeric type will be better.

## Constraints

Constraints could allow much more freedom. Firstmost, `new()` shall not limit type to a parameterless constructor of objects without `required` fields.

<details>
    <summary><ins>&nbsp;Some syntax proposals&nbsp;</ins></summary>
&nbsp;
    
```diff csharp
Flush<T>(T stream) where T :  IDisposable AND System.IO.Stream

... where T : NOT Exception

// help with not "coupling" enums
- Bonus.Calc(IEnumerable<T> months) where T : Enum
+ Bonus.Calc(IEnumerable<T> months) where T : Month OR Months // Months is Month but [Flags]
```

I long for better [numbers](cs-drawbacks.md#Numbers) in C# but meanwhile constraints could improve the state.

```csharp
// rationally limited natural number
Retail.Price<N>(N val) : where N : byte, ushort;

- Bonus.Calc(IEnumerable<T> months) where T : Enum
+ Bonus.Calc(IEnumerable<T> months) where T : Month OR Months // Months is Month but [Flags]


```

To a turn (for me) numbers and constraints shall be like:

```csharp

method<N>(N arg) where N : number, N !=0

method<N1, N2>(N1, N2) where N1, N2 : integer
   where N1<100  
   where N2

// and similar conditions
```

---
</details>

Plus-rated queries on Q&A sites formulate demands for _constraints_ "grammar" further, better, and wider.

## Syntax

### Method arguments as in object initializer

If a method has arguments of compatible type, the chances are good to shuffle them by mistake.\
Some patterns and practices (named args, side-typing) reduce the risk but bring overhead, and you still must deal with established calls and obey the args order.

Using an object initializer technique would be a relief.

```csharp

// longly known method
Calc(int a, short b, long c = 1);

// its call
- Bonus.Calc(IEnumerable<T> months) 
+ Bonus.Calc(IEnumerable<T> months) 

```

This also would make much prettier initialization of objects from factory/builder methods.

### Sugar

There's no excuse why shortcuts like `ArgumentNullException.ThrowIfNull(...)` aren't added to most exceptions. 
There could also be static classes without evident _Exception_ suffix (e.g. `NotImplemented.Throw()`). 

GUARDS and LINKE to USE-DEV **! ! ! **

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

Let's put aside that long signatures are bug buddies and shall be encapsulated into classes/structs or tuples. 

As a matter of fact, repetitive sequences of arguments occur (sometimes dictated by external tools), and ensuring the same names in order would be pleasing.

```csharp

// one of the possible syntax through attribute
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
<summary><ins>&nbsp;Interface conjunction - <b>Design sketch&nbsp;</ins></b></summary>
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

<ins>&nbsp;**Further nice-to-have:**&nbsp;</ins>\
|- [Parts and frameworks](cs-lacks-parts.md)

