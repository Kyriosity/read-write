# C# &mdash; Features and parts in shade

Different from [underused sides](../cs-feat_underused.md), these shaded parts (good or not) are specific and a developer may never need to use one. However one must be aware of them to use on demand or compare with a custom realization.

## ReactiveX

Ironically, it was Microsoft who originated [ReactiveX](https://reactivex.io/)<sup>🔗</sup> but its fame was established through platforms of others, e.g. Angular.

[IObservable](https://docs.microsoft.com/en-us/dotnet/api/system.iobservable-1)<sup>🪟</sup> is in base classes, [Reactive extensions](https://github.com/dotnet/reactive)<sup>:octocat:</sup> are at least a decade in .NET and properly integrated with LINQ but ... seldom used.\
Sure, event/stream-based development isn't for every use and its paradigm requires some learning curve, but this isn't an excuse not to look in `System.Reactive.Linq`.

### Use cases

* Messaging. In evolved scenarios, you may like to group messages or give a grace period to revoke one.
* Hardware. Dealing with APIs, you may deal with physical effects and remedies (e.g., bouncing switches).

## Explicit extensions - STILL in DEVELOPMENT❗

[Proposal](https://github.com/dotnet/csharplang/blob/main/proposals/extensions.md)<sup>:octocat:</sup> of Mads Torgersen himself divides extensions for implicit and explicit.

The former is just a better syntax for extension methods. The latter intercepts much with inheritance and shall be used with care for pure functional logic.

```csharp
public explicit extension Customer for DataObject {
  ///... extra props and methods
}
```

## Miscellaneous
|- **General**&thinsp;<sup>🪟</sup>\
|--- [`DataObject`](https://learn.microsoft.com/en-us/dotnet/api/system.windows.forms.dataobject)\
|- Accelerated calculations\
|--- [Single instruction, multiple data (SIMD)](https://learn.microsoft.com/en-us/dotnet/standard/simd)\
|--- [Hardware acceleration](https://learn.microsoft.com/en-us/dotnet/desktop/wpf/advanced/optimizing-performance-taking-advantage-of-hardware)

🔚 2022-2025
