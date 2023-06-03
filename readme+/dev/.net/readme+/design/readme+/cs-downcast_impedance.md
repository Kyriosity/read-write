# C# - Downcasting impedance

> NOTE: Always draw a base (parent) class in UML **up** to derived from it. For explicit view of up- and downcasting.

Contrary to carefree **up**casting C# will prevent assigning pure base class with any derived (downcast), even when there's no piece of extension there.

Explicable, but some patterns may tempt you to overcome this limitation. E.g. for effective way of data exchange between layers in multitier arhitecture, converters, presenters, when defaults or auto-calculations will safely fit extensions (what .NET can't predict).

## Rush: unified interfaces

Using the same class/interface is extremelly simple but build up monoliths with big desin holes, which may/will pay off later (e.g. non-deployable assemblies).

It's wise to reserve this option for prototypes only.

## Universal: (de)serialization

Serialization to a format like JSON and further deserialization may be a fast and obvious solution with a pair of "native" calls. The obvious disadvantage lays in performance charges.

## Smart: up-down-casting

🚧DRAFT
```csharp
var book = ViewModel.Create(...);
Model.Fill(book);

```

## Best: yours

Circumstances and your experiens may suggest even a better workaround.
