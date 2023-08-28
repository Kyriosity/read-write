# Driven design - TDD on DDD

## TDD (Test Driven Design)

Simplicity and versatility make **TDD** superb for insight into fuzzy topics (almost any novel development). 

It's simple because it needs neither special skills nor prescribed processes, while popular and mostly free unit-test libraries equip one enough to start.\
It's versatile since it can be applied to any extent and direction, mock and stub anything, or rely on realistic data.

The purpose of TDD is in no way test automation but means to:

+ grope **concepts** and get a hands-on feeling on subjects (be it bookkeeping routines or starship models),
+ vitalize skeleton **functionality**, evaluate trends and risks,
+ couple design dreams with the materiality of programming possibilities.

Optionally:
+ define **test framework** of the project (TDD will then outline test coverage with start stuff written in a good black-box manner).

## DDD (Design Driven Design)

TDD and **D**omain **D**riven **D**esign are perfect matches and will boost each other. With _design hat_ on one will draught domain objects, their functions, and relations, which one wearing the _"test" hat_ will mock and stub, develop the syntax of their reference, and give essential feedback.

There're many impressive stories of DDD, to which I could only supplement the next notice:

> DDD-tempered code is adverse to naming like _utilitiy_, _service_, _handler_, _data_ (unless conventions of platforms/frameworks).

## Make tests to drive

It's not enough to write legible and effective tests, which nobody will be eager to explore unless they get unfathomably scarlet.

A novice shall

+ promptly find tests and appreciate their naming and categorization,
+ learn the application by viewing and running tests.

Project "masters"

+ begin any change with tests,
+ care that even a non-programmer may comprehend tests.


## Pitfalls

### First and foremost

It occurs often that developers get lured into writing a piece of working code first and ... the whole further TDD is biased with broken enthusiasm for test drive.

### Underestimating

TDD/DDD may look first if not fun but a cozy exercise. Getting further will ask for tolerance to frustration. It will be much easier to jump off and leave the stuff "as is" (TDD outcomes have tranquil acceptance on blurred criteria) than to admit misapprehensions, failed efforts, and rework again.

### Misjudgement of trivia

Maybe it's the biggest illusion that apparent "live" concepts are easygoing to implement. \
Ancient Greeks already did a good piece of TDD for math, but applying it to programmatic abstractions may require a total rethinking (no exaggeration). 

### Contraindications

TDD/DDD isn't  _lapis philosophorum_ and is barely a good approach for:

+ test frameworks (tests of tests, then tests of these tests, and so on ...),
+ code porting,
+ non-testable entities: artistic brush, quality of the generated text, non-reproducible calculations.

## Wrapping up

We haven't resolved a mere trifle. How to make the TDD job effective and appealing. How to make tests a natural starting point for developers.\
🚧:... TO BE CONTINUED ....:pencil2:
