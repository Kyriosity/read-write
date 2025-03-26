# Naming &nbsp;&nbsp;&mdash;&nbsp;&nbsp; Practice

## Rules of thumb

* The higher the level of naming, the more attention.
* Name, apply, get feedback, refactor.
* At least two people with different backgrounds must confirm the top names.
* Avoid top names known in neighboring domains but with another meaning.\
(when possible avoid names that may become language keywords, e.g. _field_ - hallo, C#13 preview.

## Guidelines

### Methods for values

* `Get` - means available values and must be property,
* `Find` - implies efforts and queries which must bring the result (or fail with exception),
* `Lookup` - implies querying which may bring nothing. In other words, it's `TryFind`.

`Calculate`/`Process` is different from all the above.

## Traps

TRAP: Duplicate names in the chain!     PRINTER.PRINT

TRAP: The realm of `Helpers`, `Managers`, `Providers`. `Services`, ...

### Symbolic traps

ll -> EXAMPLES REQUIRED

INTERNATIONAL CHECK

## Verbal sins

- **Grandiloquence** 

General words sound vague (if not bombastic) unless established in the domain. Compare florid `[Fact]` to modest `[TestCase]`. 

- **Unexpected match** 

`public utility`

- **Jargonism**

### Guidelines for methods

`Get` must be taboo within method names - either this must be property or a better description of the returned: `Read`, `Calculate` u.a.

## Appendix. Posers

Some naming occasions can be harder than difficult.

### Impedance with inherited domain names

// ToDescribe:

### Active or passive voice

`document.print(device)` vs. `device.print(document)`

// ToDescribe:



\___________\
🔚 2023-2025
