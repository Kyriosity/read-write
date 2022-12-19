<p dir="rtl">,Junior developer writes poor code<br/>
,advanced one - good code<br/>
,expert writes no code<br/>
guru deletes code<br/></p>
<p dir="rtl"><i>Anonymous</i></p>

# Code quality

Code quality is the cement of software. It's imperceptible for users, but ought to be of superior grade for high, heavy-duty and complex constructions.

## Quality code

That's bug-unfriendly reviewed _clean code_ that follows acknowledged guidelines and principles (e.g. SOLID) and...

+ **reads** in both directions: new developer will learn the domain from it while domain expert (with some assistance) will grasp implemented business logic
+ **teaches** techniques and gimmicks
+ **inspires** to develop this application and contribute to this code (opposed to "i'd better re-write all this")

High quality also implies smart syntax which excludes typos and sound flow preventing logical mistakes.

⏲️... GOOD EXAMPLES PENDING ... 🚧

## Test coverage

> Test coverage may (and shall) share the same functionality with [TDD](../tdd-ddd.md) but is intended only to mechanically examine software (no matter when written or run).

Efficient ample tests will patch buggy and badly joined application, but does good code need this whole scale of automated scrutiny: unit, integration, performance testing?
_Errare humanum est_ while no test can harm a product. Quality of code allows then to focus tests on

+ subjects of apparent changes
+ dependencies of imports and external parts
+ performance bottlenecks

### Pitfalls

#### Falsely green tests

Bad tests are worse than none, and the worst test is a passing one that indeed shields a fail. And the worst of latter is when such fail/pass is sporadic and not easy reproducible.

An illustrative affinity is stuck green of traffic lights.

#### Excess and overlap and , formalism

Rules of a project may dictate 100% unit test coverage (at least one for an accessible member), and as a rule this will formalise proofs. Figuratevely, formal test is a kind of `ASSERT 2+2 IS 2*2`<sup>:large_orange_diamond:</sup>.\
&nbsp;&nbsp;&nbsp;&nbsp;<sup>:large_orange_diamond:</sup>&nbsp;<sub>Please do not take verbatim. Such tests may be a base for floating point errors checks.</sub>

The overlap means that a text _x_ will never pass if there's a test _y_ that fails. 

⏲️... GOOD EXAMPLES PENDING ... 🚧

## Mediocre and bad code

Apart from environments where good code won't bloom (budget/time jaws, code conveyors, unsuited teams, bad management) or shall not be planted (prototypes, stand-alone auxiliaries) even motivated intelligent teams on big projects may not guarantee high quality. To name few reasons:

+ Overhead of formal processes at the expense of development and communication  
+ Poor feedback (little or no code review, pair programming, coaching) and reluctance to learn (also from critique)
+ Over-creativity, pedantry/perfectionism, procrastination
+ Cancelled iterations/refactoring\
...and somehow root...
+ Deficiency of shared code (beginning from team/enterprise foundations up to open source collaborations)

## Moralité

With all that said, why does mediocre code prevail and _clean code_ migrates to buzzwords? Primarily, poor-quality code is written much faster and cheaper. And as it does the job other arguments fade.

Benefits of quality code are delayed<sup>:family_man_woman_boy_boy:</sup> as well as exponentially growing issues from bad software parts. The point when controllable chaos turns into uncontrollable may be fatal but lay far in next releases.\
&nbsp;&nbsp;&nbsp;&nbsp;<sup>:family_man_woman_boy_boy:</sup>&nbsp;<sub>for all beneficieries: users, customers, developers, project organizers</sub>

Not every developer will self-reflect on "submit and forget" work, and not every project management will draw a golden section between profanity and academism. 
