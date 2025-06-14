# `C#` &nbsp;&mdash;&nbsp; Misconception and malpractice

## Inappropriate usage

### Essence 

* Albeit C# has pointers, destructors, finalizers, calls to the garbage collector, memory allocation, "front door" to unmanaged code, and interop with other languages — 
programming them for business applications isn't intrinsic, unless for a particular workaround, fix of bizarre bugs, or non-conforming 3d-party API.

* The Microsoft learn corner thoroughly documents which .NET constructs are better or risky for performance/memory, and guessing them from CLR is counter-productive.<sup>📍</sup>
As well C# doesn't guarantee the same CLR output for future releases or every platform.\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<sup>📍</sup> <sub>As an example, Q&A sites may cite contradictory opinions about string interpolation, await/async, and other constructs.</sub>

The best intentions of individuals on a "low level" may occur in parallel with the .NET team on optimization of interpretation/compilation, and the latter will probably win.

There is nothing wrong with knowing the details of CLR and IL (it makes one a better developer) except the time resources, and focus one must lavish invest.

### "Bare" .NET for high-performance calculations

The downside of comfy C# programming is that .NET isn't suited for direct top-efficient code (like `C++` on `WinCom`). The energy of .NET will exceed the needs of business solutions, but will slow down calculations over arrays of millions of items or high-speed transformation of images or videos (even with all the parallelism in play).

To stay with C# in such a case, hardware acceleration patches or external libraries are a must.

### Phantom gains

[`ArrayPool`](https://learn.microsoft.com/en-us/dotnet/api/system.buffers.arraypool-1)<sup>🪟</sup>, spans, non-generic collections, record structs, and "jettison" of LINQ are suitable when 1) performance is a huge issue, 2) better syntax and match with entities (e.g. `struct` for _x-y-point_ objects).

### Obsolete constructs

- Any **un**named tuples in new stuff must be out of law.
- 🚧🚧🚧

## Declarations

### Bloated interfaces

Interfaces (as in C#&nbsp;11) allow declarations that defy imagination: static members, internal classes, and default implementations.

Nevertheless, let them remain granulated and lightweight with:

* static members to contract _operators_ (as `++` or `*=`),
* default implementation, limited to placeholders (which throw) or optional functions (which do nothing).

🚧🚧🚧 EXAMPLE REQUIRED 🖋️


### Dynamic and ExpandoObject

Any use of casting, call of props, and methods on them breaches the strongly typed C#. However, it could be a valid workaround or hack when nothing else helps.\
(Example: for return values of methods, which throw only, to be used in ternary expressions as in custom 
[`exception shortcuts`](https://github.com/Kyriosity/use-dev/blob/main/src/TuttiFrutti/AbcCommu/Errors/_basal/%F0%9F%94%BAException.cs).)

### Dubious `sealed`

There's no reason to seal a class but to show a degree of mistrust in colleagues. (Do you have other suggestions?)
It's also an arguable practice when exposing/exporting a library &thinsp;&mdash;&thinsp; to circumvent it with crooked aggregations.

## Syntax

### Abuse of extension methods

Extending tuples or general types for shortcuts burdens and undermines the whole project. Maybe a worse practice is their principal usage for multi-inheritance. 
These methods shall be used for big, universal features across projects (like LINQ). // ToDo: Link to StrExt

## Errors and messaging

### Indiscriminate catch

Negligent use of snippets can create the next good, known crash-prone block. It's obvious, and most of us won't code such a trap. 

```csharp
try { 
   /// sharp code
} catch (Exception) { success = false; } // out of memory, disk error ? sweep it under the carpet!
```

But what about its minor siblings, as here:

```csharp
var firstName = "Asd12s*d";
try {
     names.Human.Register(firstName);
} catch(ArgumentException) {
/// expected
     log.error("Couldn't register invalid: {firstName});
     success = false;
}

```

Now, consider that we submit a popular legal name, "John", and land again in the catch clause. Why?
Filtering to the expected type doesn't exclude its throw from other code parts (e.g., internal bug of our register). 

A test framework, throwing its own `ArgumentException`, can make matters even worse.

\___________

🔚 ... 🌔 2023-2025 ... but 🚧 ... TO BE CONTINUED ... 🚧
