# Good parts of C# underused

Some of C# syntax, features and libraries are underestimated or unrevealed. Next observations may be biased but are based on live experience in various projects and teams.

## Fresh released

C# evolves swift with regular and rich releases, but not every developer is an early adaptor, and not every team is eager to update breadwinning production environment.

However staying fit with C# is reasonable and feasible. Releases of .NET  are stable and besides new syntax and structures bring more performance and security. 
Devoted bloggers<sup>:raising_hand:</sup> help to separate the wheat from the chaff, and IDEs hint at new features.

&nbsp;&nbsp;&nbsp;&nbsp;<sup>:raising_hand:</sup>&nbsp;<sub>Won't suggest any since this must be a personal selection.</sub>

## ReactiveX
Ironically it was Microsoft to originate [ReactiveX](https://reactivex.io/) but its fame was established through platforms of others, e.g. Angular.

[IObservable](https://docs.microsoft.com/en-us/dotnet/api/system.iobservable-1) is in base classes, [Reactive extensions](https://github.com/dotnet/reactive) are at least a decade in .NET and properly integrated with LINQ but ... seldom used.\
Sure, event/stream based development isn't for every use and its paradigm requires some learning curve, but this isn't excuse not not to look in `System.Reactive.Linq`.

## Predicates and delegates as arguments

Are good for parametrization of methods calls but seldom seen there.

## Multitasking out-of-the-box

Exaggerated fears for intricacy may divert developers from advantages of parallelism. C# presents high-level alternatives to custom bootstrap of multi-threading (semaphores, mutex, locks, pools). And it's not even about cozy [TPL](https://docs.microsoft.com/en-us/dotnet/standard/parallel-programming/task-parallel-library-tpl), PLINQ or unblocking with `async`/`await` but instant syntax alteration that unleashes the power of parallel computing.

```diff
   var nats = Enumerable.Range(1, 28_000_000).ToArray();
-  foreach (var item in nats) 
-    CalcHard(item);
+  Parallel.ForEach(nats, CalcHard); // must be faster on casual PC
```
```csharp
static void CalcHard(int nat) {
   using var sha = SHA512.Create();
   _ = sha.ComputeHash(Encoding.UTF8.GetBytes(((int)Math.Sqrt(nat) / Math.Atan2(nat, nat)).ToString()));
 }

```

## All of the LINQ

LINQ is that cool that is the first thing to miss when coding in other languages<sup>:thought_balloon:</sup>. However even its active user maybe unaware of much tenable features.\
Not to sound unwarranted, i was myself longly unaware of [Zip](https://learn.microsoft.com/dotnet/api/system.linq.enumerable.zip), [DefaultIfEmpty](https://learn.microsoft.com/dotnet/api/system.linq.enumerable.defaultifempty), [TryGetNonEnumeratedCount](https://learn.microsoft.com/dotnet/api/system.linq.enumerable.trygetnonenumeratedcount).

&nbsp;&nbsp;&nbsp;&nbsp;<sup>:thought_balloon:</sup><sub>If you're lucky enough not to face this, such [equivalent cheatsheets](https://www.garethrepton.com/TypeScript-equivalents-for-DotNet-Linq-functions/) may give you a feeling</sub>
