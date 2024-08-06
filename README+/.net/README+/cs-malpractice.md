# C# - Misconception and malpractice

## Inappropriate usage

### Essence 

* Albeit C# has pointers, destructors, finalizers, calls to the garbage collector, memory allocation, "front door" to unmanaged code, and interop with other languages — 
programming them for business applications doesn't look natural, unless for a very specific workaround, fix of bizarre bugs, or non-conforming 3d-party API.

* Microsoft thoroughly documents which C# constructs are better or risky for performance/memory, and guessing them from CLR is counter-productive (Q&A sites cite contradictory opinions about string interpolation, await/async). As well C# doesn't guarantee the same CLR output for future releases or every platform.

Best improving intentions of individuals on a "low level" may occur in parallel with those similar to the .NET team on interpretation/compilation and the latter will probably win.

Ok, nothing wrong with knowing the details of CLR and IL (it makes one a better developer) except the time resources, and focus one must invest.

### "Bare" code for high-performance calculations

The backside of comfy C# programming is that .NET isn't suited for direct top-efficient code (like C++ on WinCom). The energy of .NET will exceed the needs of business solutions but will slow down calculations over arrays of millions of items or high-speed transformation of images or videos (even with all the parallelism in the play).

To stay with C# in such a case, hardware acceleration or external libraries are required.

### Phantom gains

[`ArrayPool`](https://learn.microsoft.com/en-us/dotnet/api/system.buffers.arraypool-1), spans, non-generic collections, record structs, and "jettison" of LINQ are suitable when 1) performance is a huge issue, 2) better syntax and match with entities (e.g. `struct` for _x-y-point_ objects).

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

Any use for casting, call of props, and methods on them breaches the C# type approach. However, it could be a valid workaround for return values of methods, which throw only, to be used in ternary expressions.

### Dubious `sealed`

There's no reason to seal a class but to show some mistrust in colleagues. It's an arguable practice when exposing/exporting a library/module.

## Syntax

### Abuse of extension methods

Maybe the worst example is their usage for multi-inheritance. Extending tuples or general types for shortcuts burdens and undermines the whole project.

Extended methods shall be used for big, common features across projects (like LINQ).

## Errors and messaging

### Indiscriminate catch

Negligent use of snippets can create the next good known crash-prone block:

```csharp
try { 
   /// sharp code
} catch (Exception) { success = false; } // out of memory, disk error ? sweep it under the carpet!
```

It's explicit and mostly corrected but not its minor siblings as here:

```csharp
var firstName = "X Æ A-12";
try {
     names.Human.Register(firstName);
} catch(ArgumentException) {
/// expected 
     log.error("Couldn't register invalid: {firstName});
     success = false;
}

```

Now consider that we submit a popular legal name (say, "John") and land  again in the catch clause. Why?
Filtering to the expected doesn't exclude the same type thrown from other code parts (e.g. internal bug of our register). 

Solutions for this and other traps with exception are proposed in ➡️[design decisions](https://github.com/Kyriosity/use-dev/tree/main/README+/decisions/README+/intercom/README+/errors) 

---

## 🚧 ... TO BE CONTINUED ... 🚧
