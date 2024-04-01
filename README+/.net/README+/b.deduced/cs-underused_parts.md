# C# - Good parts - Underused

Some of the C# syntax, features, and libraries are underestimated or unrevealed. The next observations may be biased but are based on live experience in various projects and teams.

## Fresh released - prime

C# evolves swiftly with regular and rich releases, but not every developer is an early adaptor, and not every team is eager to update the breadwinning production environment.

However, staying fit with C# is reasonable and feasible. Releases of .NET  are stable and, besides new syntax and structures, they bring more performance and security. 
Devoted bloggers<sup>👨‍👩‍👧‍👦</sup> greatly help to separate the wheat from the chaff, and IDEs hint at new features. CHANGE ICO !

&nbsp;&nbsp;&nbsp;&nbsp;<sup>👨‍👩‍👧‍👦</sup> <sub>I won't recommend any since this must be a personal experience, selection and a matter of taste.</sub>\
&nbsp;&nbsp;&nbsp;&nbsp;<sup>🙋‍♂️</sup> <sub>Revaling [CallerArgumentExpressions](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/proposals/csharp-10.0/caller-argument-expression)<sup>🔗</sup> urged me to rewrite [exception helpers](https://github.com/Kyriosity/use-dev/tree/main/src/TuttiFrutti/AbcExt/Errors).</sub>

## ReactiveX - know about

Ironically it was Microsoft who originated [ReactiveX](https://reactivex.io/)<sup>🔗</sup> but its fame was established through platforms of others, e.g. Angular.

[IObservable](https://docs.microsoft.com/en-us/dotnet/api/system.iobservable-1)<sup>🔗</sup> is in base classes, [Reactive extensions](https://github.com/dotnet/reactive)<sup>🔗</sup> are at least a decade in .NET and properly integrated with LINQ but ... seldom used.\
Sure, event/stream-based development isn't for every use and its paradigm requires some learning curve, but this isn't an excuse not to look in `System.Reactive.Linq`.

## Extension methods - more than JUST ADD

Extension methods are ...

However they may help to DIFF MODULES !

## Predicates and delegates - as arguments

// ToDo: ➡️ move to hints ! ➡️ \
Are good for parametrization of methods calls but are seldom seen there.

## Multitasking out-of-the-box

Exaggerated fears of intricacy may divert developers from the advantages of parallelism. C# presents high-level alternatives to custom bootstrap of multi-threading (semaphores, mutex, locks, pools). 

And it's not even about cozy [TPL](https://docs.microsoft.com/en-us/dotnet/standard/parallel-programming/task-parallel-library-tpl)<sup>🔗</sup>, PLINQ or unblocking with `async`/`await` but instant syntax alteration that unleashes the power of parallel computing.

<details>
   <summary><ins>&nbsp;Cycles get parallelized in a snap:&nbsp;</ins></summary>
   
```diff
   var nats = Enumerable.Range(1, 28_000_000).ToArray();
-  foreach (var item in nats) 
-    CalcHard(item);
+  Parallel.ForEach(nats, CalcHard); // must be faster on casual PC

static void CalcHard(int nat) {
   using var sha = SHA512.Create();
   _ = sha.ComputeHash(Encoding.UTF8.GetBytes(((int)Math.Sqrt(nat) / Math.Atan2(nat, nat)).ToString()));
 }

```

</details>

## All of the LINQ

LINQ is so great that it's the first thing C# developers miss when coding in other languages&nbsp;<sup>:thought_balloon:</sup>. 

However, even its addicts may be unfamiliar with many tenable features. I myself knew about [OfType](https://learn.microsoft.com/en-us/dotnet/api/system.linq.enumerable.oftype) vs. [Cast](https://learn.microsoft.com/en-us/dotnet/api/system.linq.enumerable.cast), [Zip](https://learn.microsoft.com/dotnet/api/system.linq.enumerable.zip) obscenely later than I must have used them.

It's also better to be aware of disputable methods like [DefaultIfEmpty](https://learn.microsoft.com/dotnet/api/system.linq.enumerable.defaultifempty), [TryGetNonEnumeratedCount](https://learn.microsoft.com/dotnet/api/system.linq.enumerable.trygetnonenumeratedcount) before considering to implement that one specific.

&nbsp;&nbsp;&nbsp;&nbsp;<sup>:thought_balloon:</sup><sub>If you're lucky enough not to meet this, such [cheatsheet of equivalents](https://www.garethrepton.com/TypeScript-equivalents-for-DotNet-Linq-functions/)<sup>🔗</sup> may give you a feeling.</sub>

## Reflection

Rumors of "illegal" hacking and slow performance follow the reflection but are unfair. It does worth tricks and has become a programming paradigm (unless trying to substitute "direct" language construct). 

// ToDo: link to caller !

## Dynamic code generation

It doesn't involve deranged imagination to improvise the auto-implementation of interfaces - to spare coding of countless combinations. [Roslyn](https://github.com/dotnet/roslyn) has  much facilitated dynamic code though there's a lack of good tutorials.

// ToDo: link to use-dev
