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

High quality also implies smart syntax which prevents typos and  indistinct strength of high quality must lay in preventing typos (with right syntax) and logical mistakes (sound flow).

## Test coverage

> Test coverage may (and shall) share the same functionality with [TDD](../tdd-ddd.md) but is intended only to mechanically examine software and no matter when written or run.

Efficient ample tests will patch buggy and badly joined application, but does good code need this whole scale of automated scrutiny: unit, integration testing?
_Errare humanum est_ while tests can't harm a product. Quality of code allow to focus tests on
+ subjects of change
+ dependent from and external part
+ performance benchmarks

### Pitfalls

#### Falsely green tests

Bad tests are worse than none, and the worst test is a passing one that indeed shields a fail. And the worst of latter is when this fail or passing is sporadic and not easy reproducible.

An illustrative affinity is falsely green of traffic lights.

#### Overlap and excess

Rules of a project may dictate 100% unit test coverage (at least one for an accessible member), and as a rule this will formalist to the utmost.

⏲️... GOOD EXAMPLES PENDING ... 🚧

The overlap means that it if text _x_ test fails there's at least one test y that will also fail.  OVERLAP MEANS THAT if a test X fails then at least one other test OF THE SCOPE WILL ALSO FAIL. EXAMPLE WITH Napoleon

#### Formalism 
 

## Mediocre and bad code

Apart from environments where good code won't bloom (budget/time pressure, unsuited teams, bad management) or shall not be planted (proof of concepts, temp hacks) even motivated smart teams on big projects may not guarantee high quality. To name few reasons:

+ Overhead of formal processes on the expense of development and communication  
+ Poor feedback (little or no code review, pair programming, coaching) and reluctance to learn (also from critique)
+ Over-creativity, pedantry/perfectionism, procrastination
+ Acceptance of prototype or first iteration without refactoring
and maybe the first reason
+ Deficiency of shared code (beginning from team/enterprise foundations up to open source collaborations)

## Moralité

With all that said, why does mediocre code prevail and _clean code_ migrates to buzzwords? Primarily, poor-quality code is written much faster and cheaper. And as it does the job other arguments fade.

Benefits of quality code are delayed as exponentially growing hits of bad software parts. The point when controllable chaos turns into uncontrollable may be fatal but lay far in next releases.

And not every developer will self-reflect on "submit and forget" occupation.
