# Driven design - TDD on DDD

## TDD (Test Driven Design)

Simplicity and versatility make **TDD** superb for insight into fuzzy topics (that is almost any new development). 

It's simple because it needs neither special skills nor prescribed processes, while popular and mostly free unit-test libraries equip one enough to start.\
It's versatile since it can be applied to any extent and direction, mock and stub anything, or rely on realistic data.

The purpose of TDD is in no way test automation but means to:

+ grope **concepts** and get a hands-on feeling on subjects (be it bookkeeping routines or starship models),
+ vitalize skeleton **functionality** and evaluate trends with risks,
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
+ promptly find tests and appreciate their naming and categorization
+ learn the application by viewing and running them

Project "masters"
+ begin any change with tests
+ care that even a non-programmer may comprehend tests

## Contraindications

With all this said TDD-DDD isn't  _lapis philosophorum_ and is barely a good solution for:

+ test frameworks (tests of tests, then tests of these tests, and so on ...),
+ code porting,
+ non-testable entities: artistic brush, quality of the generated text, non-reproducible calculations.
+ obvious things, like defining arithmetic operations (where ancient Greeks already did good TDD)

## Wrapping up

It's time to recall the deepest pitfall in TDD (DDD). It occurs quite often that a developer gets lured into writing a piece of working code first and then the whole further TDD is biased with lesser enthusiasm for test drive.

Now, how to make the TDD job effective and appealing? How to make a developer look into tests first?\
🚧:... TO BE CONTINUED ....:pencil2:
