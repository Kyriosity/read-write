# C# - Parts in shade

These parts (good or not) are specific and a developer may never need to use one. However one must be aware of them to use on demand.

## ReactiveX

Ironically it was Microsoft who originated [ReactiveX](https://reactivex.io/)<sup>🔗</sup> but its fame was established through platforms of others, e.g. Angular.

[IObservable](https://docs.microsoft.com/en-us/dotnet/api/system.iobservable-1)<sup>🔗</sup> is in base classes, [Reactive extensions](https://github.com/dotnet/reactive)<sup>🔗</sup> are at least a decade in .NET and properly integrated with LINQ but ... seldom used.\
Sure, event/stream-based development isn't for every use and its paradigm requires some learning curve, but this isn't an excuse not to look in `System.Reactive.Linq`.

### Use cases

* Messaging. In evolved scenarios, you may like to group messages or give a grace period to revoke one.
* Hardware. Dealing with APIs you may deal with physical effects and remedies (like debouncing of switches).

## Miscellaneous

|- Accelerated calculations\
|--- [Single instruction, multiple data (SIMD)](https://learn.microsoft.com/en-us/dotnet/standard/simd)<sup>🔗</sup>\
|--- [Hardware acceleration](https://learn.microsoft.com/en-us/dotnet/desktop/wpf/advanced/optimizing-performance-taking-advantage-of-hardware)<sup>🔗</sup>

🔚
