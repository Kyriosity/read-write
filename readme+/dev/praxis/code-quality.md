<p dir="rtl">,Junior developer writes poor code<br/>
,advanced one - good code<br/>
,expert writes no code<br/>
guru deletes code<br/></p>
<p dir="rtl"><i>Anonymous</i></p>

# Code quality

Code quality is the **cement** of software. It's imperceptible for spectators and doesn't matter much for booths, but ought to be of superior grade for sky-scraping, heavy-duty, or complex constructions.

## High-quality code

That's _a)_ bug-unfriendly _b)_ reviewed/tested _c)_ _clean code_ that follows acknowledged guidelines and principles (e.g. SOLID) and also...

- [x] **reads** in both directions: the new developer will learn the domain from it while the domain expert (with some assistance) will grasp the implemented application logic
- [x] **teaches** techniques and gimmicks
- [x] **inspires** to contribute to this code (rather than "it's better to rewrite that")

The concept of high-quality code correlates with [Test Driven Design](../design/readme+/tdd-ddd.md) 

### Bug-unfriendly code

Even bug-**free** code can be bug-**prone**, while bug-unfriendly style minimizes the risk of introducing an error by change (no matter whether unit tests will pick one).

High-quality code has

+ syntax that prevents typos (in C# simple `string.Empty` instead of `""` and other [tricks](../.net/readme+/cs-hints.md))
+ sound logical flow (early return, shallow enclosures)

### Test coverage

> Test coverage may (and shall) share the same functionality with TDD but is intended merely to mechanically examine software (no matter when written and run).

Efficient, ample tests allow only patching buggy and badly joined applications, while good code doesn't need a whole scale of automated scrutiny: unit, integration, and performance testing.

However, _errare humanum est_, no test can harm the product. Quality of code allows us to focus tests on ...

+ subjects of apparent changes
+ dependencies of imports and external parts
+ performance bottlenecks

... and avoid\
|--- [Tests pitfalls](../testing/code-tests_pitfalls.md)

## Elegant code

🚧 TO BE WRITTEN...

## P.S. Moralité

With all that said, why does mediocre code prevail and _clean code_ migrate to buzzwords? 

Primarily, poor-quality code is written much faster and cheaper. And as it does the job counter-arguments fade.

Benefits of quality code lag<sup>:family_man_woman_boy_boy:</sup> as well as exponentially growing issues from bad software parts. The point when controllable chaos goes out of control may be crucial but lay far in the next releases (when its creators are safely on other projects).\
&nbsp;&nbsp;&nbsp;&nbsp;<sup>:family_man_woman_boy_boy:</sup>&nbsp;<sub>for all beneficiaries: users, customers, developers, project organizers</sub>

Not every developer will self-reflect on "submit and forget" work, and not every project management will draw a golden section between profanity and academism. 

## P.P.S. Mediocre code - why

Apart from environments where good code won't bloom<sup>:wilted_flower:</sup> or shall not be planted<sup>:desert:</sup> even motivated intelligent teams may not achieve high quality over a big project. To name a few reasons:

+ overhead of formal processes at the expense of development and communication  
+ "egocentrism": low feedback (code review, pair programming, coaching) and reluctance to learn (also from critique)
+ over-creativity, unrestrained abstraction, pedantry/perfectionism, procrastination
+ canceled iterations/refactoring
+ hesitation to use and contribute to shared code (from team/enterprise foundations up to open source)

&nbsp;&nbsp;&nbsp;&nbsp;<sup>:wilted_flower:</sup>&nbsp;<sub>budget/time jaws, code conveyors, unsuited teams, bad management</sub>\
&nbsp;&nbsp;&nbsp;&nbsp;<sup>:desert:</sup>&nbsp;<sub>prototypes, stand-alone auxiliaries, temporary solutions</sub>

Some smart guys individually develop great apps and are so good at comprehending the whole picture that don't need and like to lose time with code organisation. However, it's a rare story and not about enterprise development.
