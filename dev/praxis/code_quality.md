<p dir="rtl">,Junior developer writes poor code<br/>
,advanced one - good code<br/>
,expert writes no code<br/>
guru deletes code<br/></p>
<p dir="rtl"><i>Anonymous</i></p>

# Code quality

Code quality is the cement of software. It's imperceptible for users, but ought to be of superior grade for high, heavy-duty and complex constructions.

## Quality code

That's _a)_ bug-unfriendly _b)_ reviewed _c)_ _clean code_ that follows acknowledged guidelines and principles (e.g. SOLID) and also...

- [x] **reads** in both directions: new developer will learn the domain from it while domain expert (with some assistance) will grasp implemented business logic
- [x] **teaches** techniques and gimmicks
- [x] **inspires** to develop this application and contribute to this code (opposed to "i'd better re-write all this")

High quality also implies smart syntax, which excludes typos, and sound flow preventing logical mistakes.

⏲️... GOOD EXAMPLES PENDING ... 🚧

## Test coverage

> Test coverage may (and shall) share the same functionality with [TDD](../tdd-ddd.md) but is intended only to mechanically examine software (no matter when written or run).

Efficient ample tests will patch buggy and badly joined application, but does good code need this whole scale of automated scrutiny: unit, integration, performance testing?

_Errare humanum est_ while no test can harm a product. Quality of code allows then to focus tests on ...
+ subjects of apparent changes
+ dependencies of imports and external parts
+ performance bottlenecks

... and avoid\
|--- [Tests pitfalls](code_tests_pitfalls.md)


## Mediocre and bad code

Apart from environments where good code won't bloom<sup>:wilted_flower:</sup> or shall not be planted<sup>:desert:</sup> even motivated intelligent teams on big projects may not guarantee high quality. To name few reasons:

+ overhead of formal processes at the expense of development and communication  
+ poor feedback (little or no code review, pair programming, coaching) and reluctance to learn (also from critique)
+ over-creativity, unrestrained abstraction, pedantry/perfectionism, procrastination
+ cancelled iterations/refactoring\
... and somehow root ...
+ deficiency of shared code use and collaboration (from team/enterprise foundations up to open source)

&nbsp;&nbsp;&nbsp;&nbsp;<sup>:wilted_flower:</sup>&nbsp;<sub>budget/time jaws, code conveyors, unsuited teams, bad management</sub>\
&nbsp;&nbsp;&nbsp;&nbsp;<sup>:desert:</sup>&nbsp;<sub>prototypes, stand-alone auxiliaries, temporary solutions</sub>

## Moralité

With all that said, why does mediocre code prevail and _clean code_ migrates to buzzwords? 

Primarily, poor-quality code is written much faster and cheaper. And as it does the job other arguments fade.

Benefits of quality code are delayed<sup>:family_man_woman_boy_boy:</sup> as well as exponentially growing issues from bad software parts. The point when controllable chaos turns into uncontrollable may be fatal but lay far in next releases.\
&nbsp;&nbsp;&nbsp;&nbsp;<sup>:family_man_woman_boy_boy:</sup>&nbsp;<sub>for all beneficieries: users, customers, developers, project organizers</sub>

Wrapping up. Not every developer will self-reflect on "submit and forget" work, and not every project management will draw a golden section between profanity and academism. 
