<p dir="rtl">,<b>Junior</b> developers write poor code<br/>
,those who <b>advance</b> &thinsp;&mdash;&thinsp; good code<br/>
,<b>experts</b> escape to write code<br/>
.and <b>gurus</b> only delete code<br />
<i><samp>A&thinsp;N&thinsp;O&thinsp;N&thinsp;Y&thinsp;M&thinsp;O&thinsp;U&thinsp;S</samp></i></p>

# `Code` <nark>Quality</mark>

<table><tr></tr><tr valign="center"><td width=30%>
  <picture><img src="../../../_rsc/_img/photo/misc/pour_concrete.jpg" alt="&nbsp;pouring concrete" title="&nbsp;Image credit: jkcement.com&#013;&#010;(for illustration purposes only)" /></picture>
</td><td>
  
### Code is the <mark>cement</mark> of software. Its quality is imperceptible to spectators and doesn't matter much for booths.

### But it ought to be of superior grade for sky-scraping, heavy-duty, or complex constructions.

### As in buildings, poor quality leads to menacing cracks, which no design clamps can hold for long.

</td></tr></table>

## High-quality code

That's <sub>🪳</sub>bug-unfriendly<sub>⛔</sub> 👓reviewed/tested🧪 **`clean code`** that follows acknowledged guidelines (ꜱᴏʟɪᴅ, ᴅʀʏ, ᴋɪꜱꜱ, ...) and also:

+ [x] **reads** in both directions<sup>↔️</sup>,
+ [x] **teaches** techniques and gimmicks,
+ [x] **inspires** to contribute (<ins>rather than to re-write</ins>).

&nbsp; &nbsp; <sup>↔️</sup> <sub>An on-boarding developers can learn the domain from code, while a domain expert will grasp the implemented application logic. Sure, both assdisted and with documentation.</sub>

### <samp>Re:</samp> Bugs 🪳

Bug-**free** code can be nevertheless bug-**prone**. Code style must be bug-unfriendly to minimize the risk of introducing an error by change (regardless of whether tests will promptly detect one or not).

High-quality code shall present

+ syntax that prevents typos<sup>🎼</sup> and mistakes<sup>🥎</sup>,
+ pronounced logical flows (e.g., early returns, shallow enclosures),
+ foolproof input/import.

The highest merit is that even a breaking change won't surprise authors and users with unexpected side effects.

Code optimization (deleting redundancies, merging common logic and data, shortening syntax) that retains readability<sup>📖</sup> is prizewinning:\
**less code** yields **less soil for bugs**.

\___________

&nbsp; &nbsp; &nbsp; <sup>🎼</sup> <sub>e.g. `space.Single` instead of `" "` and other [C# tricks](../../../.net/README+/cs-hints.md)</sub>\
&nbsp; &nbsp; &nbsp; <sup>🥎</sup> <sub>Plenty of magic strings and numbers, deceptive names, accidental casts, or "ghost" arguments (to name a few).</sub>\
&nbsp; &nbsp; &nbsp; <sup>📖</sup> <sub>Languages provide more and more sugar to make one-liners of methods, but you must stop when this obfuscates lucidity (e.g., you must "unpack" to debug).</sub>

### <samp>Re:</samp> Tests 🧪

> [!NOTE]
> Test coverage may (and shall) share realization with or even origin from [Test Driven Development](../../tests/), but is **primarily** intended to examine software mechanically 
(no matter whether implemented before the subject or _post factum_).
> 

Ample, even overlapping tests may be efficient to patch buggy and badly joined applications, 
while quality code doesn't need the whole cove of prescribed/automated scrutiny: unit, integration, and performance testing.

Enough quality code allows one to focus on tests where _errare humanum est_:

* bottlenecks: intricate logic, performance, accuracy,
* subjects of frequent changes,
* dependencies on imports and external parts.

... and give more air to avoid [tests pitfalls](../../tests/asQA/README+/QA_tests-pitfalls.md).

## Conclusion

**A)** The traits listed above are <samp><b><ins>NOT</ins></b></samp> acceptance criteria, **but** utmost aims. 
Even if a team comes close to them, the code won't be a book of design revelation — it still owes quality [documentation](../../docu) or/and tutoring.

**B)** While design hammers formworks of code <mark>concrete</mark>, [coding frames](https://github.com/Kyriosity/use-dev/tree/main/README%2B/frames) reinforce it.

**C)** Coding isn't a self-contained activity but an ingredient of <sub>[![Arc Deco.](../../../_rsc/_img/ArcDeco/ArcDeco-bar-14px_rounded.png)](../../../software/ArcDeco/README.md)</sub>&thinsp;, 
where quality is a motive, derivative, and bonus.

Quality code <ins>introduces</ins> good design rather than prompts deciphering and patching.

## Moralité

With all that said, **why does flawed code prevail and _clean code_ migrate to buzzwords?**

**1.** Poor-quality code is written much faster, cheaper, and without heated debates.<sup>🥴</sup> And as it does the job, especially on short sprints, counter-arguments fade.

**2.** Benefits of quality code lag for all beneficiaries<sup>:family_man_woman_boy_boy:</sup> and exponentially growing issues from bad software parts.\
The point when controllable chaos goes out of control or a security breach manifests itself may be crucial, but will be found far in the next releases.<sup>:parachute:</sup>

**3.** Intention for quality is good, but if efforts aren't complete, deficient code will still come &thinsp;&mdash;&thinsp; now with a massive overhead. 

Top up with the fact that not every developer self-reflects on "_submit and forget_" practice, and not every project lead/manager will draw a golden section between profanity and academism. 

\___________\
&nbsp; &nbsp; &nbsp; &nbsp; <sup>🥴</sup>&nbsp;<sub>Provided one doesn't bother with [development] principles.</sub>\
&nbsp; &nbsp; &nbsp; &nbsp; <sup>:family_man_woman_boy_boy:</sup>&nbsp;<sub>Customers, developers, testers, users, and project organizers.</sub>\
&nbsp; &nbsp; &nbsp; &nbsp; <sup>:parachute:</sup>&nbsp;<sub>When its originators may be safely on other projects, leaving the headache to others.</sub>

<table><tr></tr><tr valign="top"><td>

## Afterword. Still mediocre code &nbsp;&mdash;&nbsp; Why<samp>⁉️</samp>

Apart from environments where seeds of good code won't bloom<sup>:wilted_flower:</sup> or shall not be planted<sup>:desert:</sup>, 
**Motivated smart teams may not reach high quality in very good conditions with enough resources and freedoms.**

Besides _classical_ over-creativity and procrastination, the trivial reasons could be:

+ gross of formal processes at the expense of design and communication,
+ "egocentrism": low feedback (code review, pair programming, coaching) and reluctance to learn (especially from critique),
+ canceled/postponed iterations/refactoring/cleaning,
+ hesitation in using and contributing to shared code (from team/enterprise foundations up to open source)

Also, prominent individuals may develop great parts/apps alone and are so good at keeping all details and the whole picture in mind that they don't need to and like to lose time with code organization. 

However, these cases are exceptional and not about enterprise development.

\___________\
&nbsp; &nbsp; <sup>:wilted_flower:</sup> <samp>Budget/time jaws, code conveyors, unsuited teams, bad management, or intentional obfuscation.</samp>\
&nbsp; &nbsp; <sup>:desert:</sup> <samp>Prototypes, stand-alone auxiliaries, temporary solutions.</samp>

</td><td width="30%">
  <a href="../../../_rsc/_img/photo/blog/mount/DevVsMonolyth.jpg"><img alt="&nbsp;Stone monolyth" src="../../../_rsc/_img/photo/nat/DerAlteSchwede.jpg" title="Waterfall monolyth again..." /></a>
</td></tr></table>

🔚 ...🌜2023-2025
