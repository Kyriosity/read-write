# Driven design - TDD on DDD

## TDD (Test Driven Design)

Simplicity and versatility makes **TDD** superb for insight of vague topics (that is almost any new development). 

It's simple because needs neither special skills nor prescribed processes, while popular and mostly free unit-test libraries are enough to start.\
It's versatile since can be applied in any extent and direction, mock and stub anything or rely on real data.

The purpose of TDD is no way test automation but means to
+ grope **concepts** and get hands-on feeling on subjects (be it bookkeeping routines or starship model)
+ vitalize skeleton **functionality** and evaluate trends with risks
+ couple design dreams with reality of programming possibilities

Optionally:
+ define **test framework** of the project (TDD will then outline test coverage with start stuff written in a good black-box manner).

## DDD (Design Driven Design)

TDD and **D**omain **D**riven **D**esign are a perfect match and will boost each other. With _design hat_ on one will draught domain objects, their functions and relations, which one wearing _"test" hat_ will mock and stub, develop syntax of their use, and give essential feedback.

There're much eloquent stories of DDD, to which i could only supplement this notice:

> DDD-tempered code does not prop nameing with wording like _utilitiy_, _service_, _handler_, _data_ (unless conventions of platforms/frameworks).

## Make tests to drive

It's not enough to write both legible and effective tests, which nobody will be eager to explore unless they get unfathomably scarlet.

A novice shall
+ promptly find tests and appreciate their naming and categorization
+ learn the application by viewing and running them

Project "masters"
+ begin any change with tests
+ care that even a non-programmer may comprehend tests

## Contraindications

With all this said TDD-DDD may look like _lapis philosophorum_ but is barely a good solution for:

+ test frameworks (tests of tests of tests of ...)
+ code porting
+ non-testable things: artistic brush, quality of generated text, check of non-reproducable calculations

🚧:... TO BE CONTINUED ....:pencil2:

## Wrapping up

It's significant to recall the deepest pitfall in TDD (DDD). It occurs quite often that a developer gets lured to write some working code first and then the whole further TDD is biased with lesser enthusiasm for test drive.
