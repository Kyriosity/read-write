# C# - Miscconception and malpractice

## Essence 

Albeit C# has destructors, finalizers, calls to garbage collector, memory allocation, "front door" to unmanaged code - 
programming them looks unnatural, unless for a very specific workaround, fix of bizarre bugs, or non-conforming 3d-party API.

Microsoft thoroughly documents which C# constructs are better for performance and memory, and guessing them from CLR is counter-productive (you may find some string interpolation disputes).

## Bloated interfaces

Interfaces (as in C#&nbsp;11), allow declarations that defy imagination: static members, internal classes, implementations.

Nevertheless, let them remain granulated and lightweight with:

+ static members to contract _operators_ (as ++),
+ default implementation for placeholders (which throw) or optional functions (which do nothing)

## Extension methods abuse

The worst case is their usage for multi-inheritance. Extending tuples or general types for shortcuts burdens and undermines the whole project.

Extended methods shall be used for big common features across projects or more, comparable to LINQ.

## Phantom gains

Non-generic collections, record structs, and rejection of LINQ are suitable when 1) performance is an issue, 2) better syntax and match with entities (e.g. struct for _x-y-point_ objects).

## Implicitly obsolete constructs

Any **un**named tuples in new stuff shall be out of law.

## Dynamic and ExpandoObject

Any use for casting, call of props, and methods on them breaches C# type approach. Though could be a valid workaround for ternary expressions with indirect (wrapped) `throw`.

## Dubious `sealed`

There's no reason to seal a class but to show some mistrust in colleagues. It's an arguable practice when exposing/exporting a library/module.


