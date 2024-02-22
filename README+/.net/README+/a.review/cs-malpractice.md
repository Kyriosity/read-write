# C# - Misconception and malpractice

## Essence 

Albeit C# has destructors, finalizers, calls to the garbage collector, memory allocation, and "front door" to unmanaged code - 
programming them doesn't look natural, unless for a very specific workaround, fix of bizarre bugs, or non-conforming 3d-party API.

Microsoft thoroughly documents which C# constructs are better or risky for performance/memory, and guessing them from CLR is counter-productive (Q&A sites cite contradictory opinions about string interpolation, await/async). As well C# doesn't guarantee the same CLR output for the next releases or another platform.

## "Bare" code for high-performance calculations

The backside of comfy C# programming is that .NET isn't suited for direct top-efficient code (like C++ on WinCom). The energy of .NET will exceed the needs of business solutions but will slow down calculations over arrays of millions of items or high-speed transformation of images or videos (even with all the parallelism in the play).

To stay with C# in such a case, the use of hardware acceleration libraries is required.

## Bloated interfaces

Interfaces (as in C#&nbsp;11) allow declarations that defy imagination: static members, internal classes, and default implementations.

Nevertheless, let them remain granulated and lightweight with:

* static members to contract _operators_ (as `++` or `*=`),
* default implementation, limited to placeholders (which throw) or optional functions (which do nothing).

🚧🚧🚧 EXAMPLE REQUIRED 🖋️

## Extension methods abuse

Maybe the worst example is their usage for multi-inheritance. Extending tuples or general types for shortcuts burdens and undermines the whole project.

Extended methods shall be used for big, common features across projects (like LINQ).

## Phantom gains

Non-generic collections, record structs, and rejection of LINQ are suitable when 1) performance is an issue, 2) better syntax and match with entities (e.g. struct for _x-y-point_ objects).

## Obsolete constructs

Any **un**named tuples in new stuff shall be out of law.

## Dynamic and ExpandoObject

Any use for casting, call of props, and methods on them breaches the C# type approach. Though it could be a valid workaround for return values of methods, which throw only, to be used in ternary expressions.

## Dubious `sealed`

There's no reason to seal a class but to show some mistrust in colleagues. It's an arguable practice when exposing/exporting a library/module.
