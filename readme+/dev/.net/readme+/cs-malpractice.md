# C# - Malpractice

## Essence 

Albeit C# has destructors, finalizers, calls to garbage collector, memory allocation, "front door" to unmanaged code - 
programming them looks unnatural, unless it's a very specific task, workaround of bizarre bugs or non-conforming 3d party.

## Secret tricks

Use of undocumented or unreadable constructions, side-effects. When acquitted, then shall be wrapped into good named method.

## Extension methods abuse

The worst case is their usage for multi-inheritance.

Extending tuples or general types burdens and undermines the whole project.

## Peculiar choice for phantom gains

Non-generic collections, record structs, rejection of LINQ are suitable when 1) performance is an issue, 2) signally relieved this way.

## Implicitly obsolete constructs

Any **un**named tuples in new stuff shall be out of law.

## Dynamic and ExpandoObject

Any use for casting, call of props and methods on them breaches C# type approach. Though could be a valid workaround for ternary expressions with indirect (wrapped) `throw`.


