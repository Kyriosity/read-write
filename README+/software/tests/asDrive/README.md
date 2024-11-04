# Software &mdash; Tests as/for Drive

The idea to write tests not only _a posteriori_ to validate written code but prior - to guide their creation - can be rooted back to the 1950s,  when high-level languages emerged.<sup>👴</sup>

&nbsp;&nbsp;&nbsp;&nbsp;<sup>👴</sup> <sub>One of the best summaries is in [You won't believe how old TDD is](https://arialdomartini.wordpress.com/2012/07/20/you-wont-believe-how-old-tdd-is/)<sup>🔗</sup>.</sub>

Simplicity and versatility make **TDD** superb for insight into fuzzy topics (almost any novel development). 

+ It's simple because it needs neither special skills nor prescribed processes.
+ It's versatile since it can be applied to any extent and direction, mock and stub anything, or rely on realistic data.
+ It's natural to start with writing a test method to test the first code snippets.
+ Popular and mostly free unit-test frameworks libraries equip one enough to start. (Any modern IDE is shipped with a selection of testing templates.)

The purpose of TDD is in no way test automation but means to:

Optionally and cautionary:
+ start a **test framework** of the project (TDD will then outline test coverage with start stuff written in a good black-box manner).

### Downsides of TDD

it was so much test-driven flattery that some criticism must take place. The most negative influence could be _voodoo programming_ to achieve specific results.

Others are:

- ever-growing lines of non-production code, which require refactoring and maintenance lesser but comparable to main projects,
- lack (if not absence) of ripe active frameworks. // 🚧 ToDo: use-dev links to "3D tests"

## DDD (Design Driven Design)

EVERY DEV IS DD explicit or not, obfuscated or not.

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


### Contraindications

TDD/DDD isn't _lapis philosophorum_ and is barely a good approach for:

+ code porting,
+ badly formalizable entities: artistic brush, or generated text (image, video, or sounds)
+ non-reproducible calculations.

We haven't resolved a mere trifle. How to make the TDD job effective and appealing. How to make tests a natural starting point for developers.


🚧🐝🖋️ ...PLACEHOLDER...🚧🚧🚧

🔚
