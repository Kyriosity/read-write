# C# - Miscconception and malpractice

## Essence 

Albeit C# has destructors, finalizers, calls to garbage collector, memory allocation, "front door" to unmanaged code - 
programming them looks unnatural, unless for very specific workaround, fix of bizarre bugs, non-conforming 3d-party API.

Microsoft thoroughly documents which C# constructs are better for perfomance and memory, and guessing them from CLR is contra-productive (you may find some string interpolation disputes).

## Bloated interfaces

Interfaces (as in C#&nbsp;11), allow declarations that defy imagination: static members, internal classes, implementations.

Nevertheless, let them remain granulated and lightweight with:

+ static members to contract _operators_ (as ++),
+ default implemetation for placeholders (throw) or optional funcs (do nothing)

## Extension methods abuse

The worst case is their usage for multi-inheritance. Extending tuples or general types for shortcuts burdens and undermines the whole project.

Extended methods shall be used for big common features across project or more, comparable to LINQ.

## Peculiar choice for phantom gains

Non-generic collections, record structs, rejection of LINQ are suitable when 1) performance is an issue, 2) signally relieved this way.

## Implicitly obsolete constructs

Any **un**named tuples in new stuff shall be out of law.

## Dynamic and ExpandoObject

Any use for casting, call of props and methods on them breaches C# type approach. Though could be a valid workaround for ternary expressions with indirect (wrapped) `throw`.

## Dubious `sealed`

There's no reason to seal a class but to stress the mistrust in colleagues. And it's an arguable practice when exposing/exporting a library/module.


