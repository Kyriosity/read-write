# Driven design - TDD on DDD

This chapter isn't miscellanea but the conjunction of the duo topics, which come hand in hand in the driven development.

## TDD (Test Driven Design)

Simplicity and versatility make **TDD** superb for insight into fuzzy topics (almost any novel development). 

+ It's simple because it needs neither special skills nor prescribed processes.
+ It's versatile since it can be applied to any extent and direction, mock and stub anything, or rely on realistic data.
+ It's natural to start with - write a test method to test first code snippets.
+ Popular and mostly free unit-test frameworks libraries equip one enough to start. (Any modern IDE is shipped with a selection of testing templates.)

The purpose of TDD is in no way test automation but means to:

+ grope **concepts** and get a hands-on feeling on subjects (be it bookkeeping routines or starship models),
+ vitalize skeleton **functionality**, evaluate trends and risks,
+ couple design fantasies with the tech-stack materiality.

Optionally and cautionary:
+ start a **test framework** of the project (TDD will then outline test coverage with start stuff written in a good black-box manner).

### Downsides of TDD

it was so much test-driven flattery that some criticism must take place. The most negative influence could be _voodoo programming_ to achieve specific results.

Others are:

- ever-growing lines of non-production code, which require refactoring and maintenance lesser but comparable to main projects,
- lack (if not absence) of ripe active frameworks. // 🚧 ToDo: use-dev links to "3D tests"

## DDD (Design Driven Design)

<p dir=rtl><i>My ideal of program design is to represent the concepts<br/>
.of the application domain directly in code<br>
,That way, if you understand the application domain<br/>
.you understand the code and vice versa</i><br/>
<a href="https://www.stroustrup.com/quotes.html">Bjarne Stroustrup quotes</a></p>

TDD and **D**omain **D**riven **D**esign are perfect matches and will boost each other. With _design hat_ on one will draught domain objects, their functions, and relations, which one wearing the _"test" hat_ will mock and stub, develop the syntax of their reference, and give essential feedback.

There are many impressive stories of DDD to learn from, to which I can only supplement the next notice:

> DDD-tempered code is adverse to naming like _utilitiy_, _service_, _handler_, _data_ (unless conventions of platforms/frameworks).

## Make tests to drive

It's not enough to write legible and effective tests, which nobody will be eager to explore unless they get unfathomably scarlet.

Project **newbies** shall

+ promptly find tests and appreciate their naming and categorization,
+ learn the application by viewing and running tests.

Project "**masters**" shall

+ begin any addition, change, and **removal** change with tests,
+ care that even a non-programmer may comprehend ideas behind tests.

## Pitfalls, which reveal guidelines

### First and foremost

It occurs often that developers get lured into writing a piece of working code first and ... the whole further TDD is biased with broken enthusiasm for test drive.

### Underestimating

TDD/DDD may look first if not fun but a cozy exercise. Getting further will ask for tolerance to frustration. It will be much easier to jump off and leave the stuff "as is" (TDD work has tranquil acceptance on blurred criteria) than to admit misapprehensions, failed efforts, and rework again.

### Overfocus on structure and names

With only a handful of tests written accurate naming and categorization may distract one from new and convey little value. Detailed development and refactoring will urge you to revise these attributes. 

### Misjudgement of trivia

These mirages appear chiefly on the horizons of new software. Apparent "live" concepts look easygoing to implement without much TDD.<sup>:classical_building:</sup>

&nbsp;&nbsp;&nbsp;&nbsp;<sup>:classical_building:</sup> <sub>_Gia parádeigma_, ancient Greeks did a good piece of TDD for math, but applying it to programmatic abstractions will surprise one with total rethinking (no exaggeration).</sub>

### Contraindications

TDD/DDD isn't  _lapis philosophorum_ and is barely a good approach for:

+ test frameworks (tests of tests, then tests of these tests, and so on ...),
+ code porting,
+ non-testable entities: artistic brush, quality of the generated text, non-reproducible calculations.

## Wrapping up

We haven't resolved a mere trifle. How to make the TDD job effective and appealing. How to make tests a natural starting point for developers.

🚧:... TO BE CONTINUED .... ✏️
