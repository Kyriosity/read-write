<p dir="rtl">,Junior developer writes poor code<br/>
,advanced one - good code<br/>
,expert writes no code<br/>
guru deletes code<br/></p>
<p dir="rtl"><i>Anonymous</i></p>

# Code - Quality

Code quality is the **cement** of software. It's imperceptible for spectators and doesn't matter much for booths, but it ought to be of superior grade for sky-scraping, heavy-duty, or complex constructions — poor quality, as in buildings, leads to menacing cracks.

## High-quality code

That's <sub>🪳</sub>bug-unfriendly<sub>⛔</sub> 👓reviewed/tested🧪 **`clean code`** that follows acknowledged guidelines (ꜱᴏʟɪᴅ, ᴅʀʏ, ᴋɪꜱꜱ, ...) and also:

+ [x] **reads** in both directions<sup>↔️</sup>,
+ [x] **teaches** techniques and gimmicks,
+ [x] **inspires** to contribute (rather than "it's better to rewrite that")

&nbsp;&nbsp;&nbsp;&nbsp;<sup>↔️</sup> <sub>On-boarding developers can learn the domain from code (sure, not alone) while the domain expert (with some assistance) will grasp the implemented application logic.</sub>

### Re: Bugs 🪳

Even bug-**free** code can be bug-**prone**. Code style must be bug-unfriendly to minimize risks of introducing an error by change (no matter whether unit tests will pick one).

High-quality code has

+ syntax that minimizes the risk of typos<sup>🎼</sup> and mistakes (like deceptive names, accidental casts or "ghost" arguments),
+ visible logical flow (e.g. early returns, shallow enclosures).

The highest merit is that even a breaking change won't surprise devs and users with unexpected side effects.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<sup>🎼</sup>&nbsp;<sub>e.g. `String.Empty` instead of `""` and some [C# tricks](../../../../.net/README+/b.deduced/cs-hints.md)</sub>

### Re: Tests 🧪

Test coverage may (and shall) share the same functionality with [Test-Domain Driven Design](../../design/tdd-ddd.md) but is intended to mechanically examine software (no matter implemented prior to the subject or a posteriori).

Efficient, ample test coverage allows only patching buggy and badly joined applications, while good code doesn't need a whole scale of automated scrutiny: unit, integration, and performance testing.

_Errare humanum est_, and quality code allows one to focus tests on ...

* bottlenecks: intricate logic, performance, accuracy,
* subjects of frequent changes,
* dependencies on imports and external parts.

... and get more breath to avoid [tests pitfalls](tests-pitfalls.md).

## Moralité

With all that said, why does deficient code prevail and _clean code_ migrate to buzzwords? 

1. Poor-quality code is written much faster, cheaper, and without heated debates<sup>🥴</sup>. And as it does the job counter-arguments fade.
2. Benefits of quality code lag for all beneficiaries<sup>:family_man_woman_boy_boy:</sup> as well as exponentially growing issues from bad software parts. The point when controllable chaos goes out of control, or a security breach opens may be crucial but lay far in the next releases.<sup>:parachute:</sup>
3. Intention for quality is good but if efforts aren't complete then still deficient code will come with a massive overhead. 

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<sup>🥴</sup>&nbsp;<sub>Provided one doesn't bother with [development] principles.</sub>\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<sup>:family_man_woman_boy_boy:</sup>&nbsp;<sub>Customers, developers, tester, users and project organizers.</sub>\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<sup>:parachute:</sup>&nbsp;<sub>When its originators may be safely on other projects, leaving the headache to others.</sub>

Add here that not every developer self-reflects on "submit and forget" work, and not every project management will draw a golden section between profanity and academism. 

## Afterword

**1)** Coding isn't a self-contained activity but an ingredient of [![Arc Deco.](../../../../_rsc/_img/ArcDeco/ArcDeco-bar-12px.jpg)](../../../README.md), where quality is a derivative and bonus.
   
**2)** The traits listed above are NOT acceptance criteria, but utmost aims. Even if a team comes close to them the code won't be a book of design revelation and its comprehension will depend on good [documentation](../../dev-docu.md).

## Appendix (1 of 1). Still mediocre code - why?!

Apart from environments where seeds of good code won't bloom<sup>:wilted_flower:</sup> or shall not be planted<sup>:desert:</sup> even motivated smart teams may not reach high quality in good working and design conditions. 

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<sup>:wilted_flower:</sup>&nbsp;<sub>Budget/time jaws, code conveyors, unsuited teams, bad management, or intentional obfuscation.</sub>\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<sup>:desert:</sup>&nbsp;<sub>Prototypes, stand-alone auxiliaries, temporary solutions.</sub>

Besides _classical_ over-creativity and procrastination the reasons could be:

+ overweight of formal processes at the expense of design and communication,
+ "egocentrism": low feedback (code review, pair programming, coaching) and reluctance to learn (especially from critique),
+ canceled/postponed iterations/refactoring/cleaning,
+ hesitation in using and contributing to shared code (from team/enterprise foundations up to open source)

Some smart individuals develop great apps alone and are so good at keeping all details and the whole picture in mind that don't need and like to lose time with code organization. However, it's exceptional and not about enterprise development.

🔚 THE END (c<sup>#</sup>)2024
