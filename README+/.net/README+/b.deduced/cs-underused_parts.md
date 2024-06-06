# C# - Good parts - Underused

Some of the C# syntax, features, and libraries are underestimated or unrevealed. The next observations may be biased but are based on live experience in various projects and teams.

## Fresh released

C# evolves swiftly with regular and rich releases, but not every developer is an early adaptor, and not every team is eager to update the breadwinning production environment.

However, staying fit with C# is reasonable and feasible. Releases of .NET are cumulative and stable; besides new syntax and structures, they bring more performance, security with longer support. 

Devoted bloggers<sup>👨‍👩‍👧‍👦</sup> are greatly at separating the wheat from the chaff, and IDEs hint at new features.

&nbsp;&nbsp;&nbsp;&nbsp;<sup>👨‍👩‍👧‍👦</sup> <sub>I won't recommend any since this must be a personal experience, selection of the active and a matter of taste.</sub>\
&nbsp;&nbsp;&nbsp;&nbsp;<sup>🙋‍♂️</sup> <sub>Revealing [CallerArgumentExpressions](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/proposals/csharp-10.0/caller-argument-expression)<sup>🔗</sup> urged me to rewrite [exception helpers](https://github.com/Kyriosity/use-dev/tree/main/src/TuttiFrutti/AbcExt/Errors).</sub>

## Predicates and delegates as arguments

// ToDo: ➡️ move to hints ! ➡️ \
They are good for the parametrization of method calls but are seldom seen there.

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

The image of "illegal" hacking and rumors of slow performance follow the reflection but are unfair. It does worth tricks and has become a programming paradigm (unless trying to substitute "direct" language construct). 

// ToDo: link to caller !

## Dynamic code generation

It doesn't involve deranged imagination to improvise the auto-implementation of interfaces - to spare coding of countless combinations. [Roslyn](https://github.com/dotnet/roslyn)<sup>🔗</sup> has  much facilitated dynamic code though there's a lack of good tutorials.

// ToDo: link to use-dev

## Extension methods

### Props of polymorphism

// ToDo: EXAMPLE !

## Miscellany

### Value Task

[ValueTask](learn.microsoft.com/dotnet/api/system.threading.tasks.valuetask-1)<sup>🔗</sup> was introduced in .NET Core 2.0 to wrap the result of `Task`. It won't create an overhead if the result is available.

Along with another abstraction `IValueTaskSource` it's a choice over `Task` for one-time calls without blocking and similar scenarios.

## Wrap up

There must be other useful but neglected parts, features, and syntax of C# and its subsystem, that you may know and contribute to this document.

Besides definitely underused parts there are\
|--- [Parts in shade](cs-shadow_parts.md)\
|--- Obsolete/bad parts, features, and [practices](../a.review/cs-malpractice.md) 
