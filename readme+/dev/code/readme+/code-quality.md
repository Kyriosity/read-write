<p dir="rtl">,Junior developer writes poor code<br/>
,advanced one - good code<br/>
,expert writes no code<br/>
guru deletes code<br/></p>
<p dir="rtl"><i>Anonymous</i></p>

# Code - Quality

Code quality is the **cement** of software. It's imperceptible for spectators and doesn't matter much for booths, but ought to be of superior grade for sky-scraping, heavy-duty, or complex constructions. Poor quality, as in building, results in security cracks.

## High-quality code

That's _**a)**_ bug-unfriendly _**b)**_ reviewed/tested _**c)**_ _clean code_ that follows acknowledged guidelines and principles (e.g. SOLID as most known) and also...

- [x] **reads** in both directions: the new developer will learn the domain from it while the domain expert (with some assistance) will grasp the implemented application logic
- [x] **teaches** techniques and gimmicks
- [x] **inspires** to contribute to this code (rather than "it's better to rewrite that")


### Re: Bugs

Even bug-**free** code can be bug-**prone**. Code style must be bug-unfriendly to minimize risks of introducing an error by change (no matter whether unit tests will pick one).

High-quality code has

+ syntax that prevents typos<sup>🎼</sup> and mistakes (like deceptive names or accidental casts),
+ visible logical flow (not limited to early return, shallow enclosures).

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<sup>🎼</sup>&nbsp;<sub>e.g. `String.Empty` instead of `""` and some [C# tricks](../../../.net/readme+/deduced/cs-hints.md)</sub>

### Re: Tests

Test coverage may (and shall) share the same functionality with [Test Driven Design](../../design/readme+/tdd-ddd.md) but is intended to mechanically examine software (no matter when a subject of the test was implemented).

Efficient, ample test coverage allows only patching buggy and badly joined applications, while good code doesn't need a whole scale of automated scrutiny: unit, integration, and performance testing.

_Errare humanum est_, and quality code allows one to focus tests on ...

* bottlenecks: intricate logic, performance, accuracy,
* subjects of frequent changes,
* dependencies on imports and external parts.

... and get more breath to avoid [tests pitfalls](../../testing/tests-pitfalls.md).

## Moralité

With all that said, why does deficient code prevail and _clean code_ migrate to buzzwords? 

1. Poor-quality code is written much faster, cheaper, and without heated debates<sup>🥴</sup>. And as it does the job counter-arguments fade.
2. Benefits of quality code lag for all beneficiaries<sup>:family_man_woman_boy_boy:</sup> as well as exponentially growing issues from bad software parts. The point when controllable chaos goes out of control, or a security breach opens may be crucial but lay far in the next releases.<sup>:parachute:</sup>
3. Intention for quality is a half success but with incomplete efforts, it will be the same, though better, deficient code. 

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<sup>🥴</sup>&nbsp;<sub>Provided one doesn't bother with [development] principles.</sub>\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<sup>:family_man_woman_boy_boy:</sup>&nbsp;<sub>Customers, developers, tester, users and project organizers.</sub>\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<sup>:parachute:</sup>&nbsp;<sub>When its originators may be safely on other projects, leaving the headache to others.</sub>

Add here that not every developer self-reflects on "submit and forget" work, and not every project management will draw a golden section between profanity and academism. 

## Appendix 1 (of 1). Mediocre code - why

Apart from environments where good code won't bloom<sup>:wilted_flower:</sup> or shall not be planted<sup>:desert:</sup> even motivated intelligent teams may not achieve high quality up to the end of a big project. 

Foremost coding is an ingredient of [Creation of software](../../design/), where quality is a derivative. Other reasons besides _classical_ over-creativity and procrastination are:

+ overweight of formal processes at the expense of design and communication,
+ "egocentrism": low feedback (code review, pair programming, coaching) and reluctance to learn (especially from critique),
+ canceled/skipped iterations/refactoring,
+ hesitation in using and contributing to shared code (from team/enterprise foundations up to open source)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<sup>:wilted_flower:</sup>&nbsp;<sub>Budget/time jaws, code conveyors, unsuited teams, bad management, or intentional obfuscation.</sub>\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<sup>:desert:</sup>&nbsp;<sub>Prototypes, stand-alone auxiliaries, temporary solutions.</sub>

Some smart individuals develop great apps alone and are so good at keeping all details and the whole picture in mind that don't need and like to lose time with code organization. However, it's exceptional and not about enterprise development.

🔚
