# `C#`&nbsp;&nbsp;&mdash;&nbsp;&nbsp;Good sides&nbsp;&nbsp;&mdash;&nbsp;&nbsp;Underused

Parts of C# syntax, certain features, libraries, and frameworks are preferable but often remain unrevealed.

## Freshly released

C# evolves swiftly with regular and rich releases, but not every developer is an early adaptor, and not every team is eager to update the breadwinning production environment.

However, staying fit with C# is reasonable and feasible. Releases of .NET are cumulative and stable; besides new syntax and structures, they bring more performance, and security with longer support. 

Devoted bloggers and speakers<sup>👨‍👩‍👧‍👦</sup> are greatly at separating the wheat from the chaff, and IDEs hint at new features.

&nbsp;&nbsp;&nbsp;&nbsp;<sup>👨‍👩‍👧‍👦</sup> <sub>I don't recommend any since this must be a personal experience, selection of the active and a matter of taste. Except for the original [dev blog](https://devblogs.microsoft.com/dotnet/)<sup>🪟</sup>.</sub>\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<sub>**Advice:** Limit review ardor to [officially released features](https://learn.microsoft.com/en-us/dotnet/csharp/whats-new/)<sup>🪟</sup>. Many nice others are delayed from release to release (let alone those experimental).</sub>

### C#13.NET9 (2024) ... but wait! ...

Among other features, two could be rather practical. Announced, and promoted by bloggers but "still in active development" (2025).

+ `using` aliases improved: 1) full qualification not required for imported namespaces, 2) generics supported.
+ `extension` keyword (`explicit` and `implicit`): 1) good to replace clumsy extension methods with `this`, 2) properties supported.

### Earlier

The following "old" practical syntax and features remain unused in enough programs I've seen.

- [ ]  single file namespaces with `;` without `{}`
- [ ] [Tuple assignments](https://essentialcsharp.com/tuples#tuples)<sup>🔗</sup> - shortcuts assignment (swap!) and comparison.
- [ ] [`CallerArgumentExpressions`](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/proposals/csharp-10.0/caller-argument-expression)<sup>🙋‍♂️</sup>
- [ ] `readonly` for `struct` methods - questionable but don't harm and may prevent bugs

&nbsp;&nbsp;&nbsp;&nbsp;<sup>🙋‍♂️</sup> <sub>This urged me to rewrite ➡️[exception helpers](https://github.com/Kyriosity/use-dev/tree/main/src/TuttiFrutti/AbcCommu/Errors).</sub>

##### `switch` beyond `else if`

With pattern matching, tuples, and `=>` replacing `break` the good old statement got the second life.

## Pattern matching `switch` instead of `else if`s

"Conditional rows" with patterns and `_`-matching, "on-the-fly" tuples, and `=>` returns allow amazing tables of shortcuts.\
It's better to see once a recent video tutorial, for example [Advanced Pattern Matching in C#](https://www.youtube.com/watch?v=W-f9MHB-5TQ)<sup><picture><img src="../../_rsc/_img/logo/logo-youtube_h12px.jpg" title="&nbsp;Link to YouTube video" /></picture></sup>, Nov/2024.

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

LINQ is so great and practical that it's the first thing C# developers miss when coding in other languages.<sup>:large_blue_diamond:</sup>

However, even its addicts may be unfamiliar with many tenable features. I knew about 
[`Cast`](https://learn.microsoft.com/en-us/dotnet/api/system.linq.enumerable.cast), 
[`Zip`](https://learn.microsoft.com/dotnet/api/system.linq.enumerable.zip),
`SkipWhile`, `Append`, and `Prepend`, 
obscenely later than I must have used them.

Attach here [`Lookup`](https://learn.microsoft.com/en-us/dotnet/api/system.linq.lookup-2) &mdash; the counterpart of the well-known `Dictionary`.

It's also better to be aware of disputable methods like 
[`OfType`](https://learn.microsoft.com/en-us/dotnet/api/system.linq.enumerable.oftype), 
[`DefaultIfEmpty`](https://learn.microsoft.com/dotnet/api/system.linq.enumerable.defaultifempty), 
[`TryGetNonEnumeratedCount`](https://learn.microsoft.com/dotnet/api/system.linq.enumerable.trygetnonenumeratedcount).

&nbsp;&nbsp;&nbsp;&nbsp;<sup>:large_blue_diamond:</sup><sub>If you're lucky enough not to meet this, such [cheatsheet of equivalents](https://www.garethrepton.com/TypeScript-equivalents-for-DotNet-Linq-functions/)<sup>🔗</sup> may give you a feeling.</sub>

## Reflection

The image of "illegal" hacking and rumors of slow performance follow the reflection but are unfair. It does worth tricks and has become a programming paradigm (unless trying to substitute a "direct" language construct). 

// ToDo: link to caller !

## Dynamic code generation

It doesn't involve deranged imagination to improvise the auto-implementation of interfaces - to spare coding of countless combinations. [Roslyn](https://github.com/dotnet/roslyn)<sup>🔗</sup> has  much facilitated dynamic code though there's a lack of good tutorials.

// ToDo: link to use-dev

## Extension methods

### Props of polymorphism

// ToDo: EXAMPLE !

## Miscellany

### Value Task

[`ValueTask`](https://learn.microsoft.com/dotnet/api/system.threading.tasks.valuetask-1) was introduced in .NET Core 2.0 to wrap the result of `Task`. It won't create an overhead if the result is available.

Along with another abstraction `IValueTaskSource` it's a choice over `Task` for one-time calls without blocking and similar scenarios.

## Wrap up

There must be other useful but neglected parts, features, and syntax of C# and its subsystem, that you may know and contribute to this document.

Besides definitely underused parts there are\
|--- [Parts in shade](parts/cs-feat_shadow.md)\
|--- Obsolete/bad parts, features, and [malpractices](cs-malpractice.md) 

\___________\
🔚 🌙 2021-2025
