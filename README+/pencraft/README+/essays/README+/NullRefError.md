<h1 align="center"><code>Null</code>, its reference, and the Mistake<br />🔎&empty;</h1>

<table><tr valign="top"><td><picture><img alt="&thinsp; Gibson Dam, Montana - drain (Wiki)" src="../../../../_rsc/_img/photo/build/Gibson_Dam-Montana-drain.jpg" 
   title="&nbsp;Gibson Dam, Montana, drain&#010;Source: Wiki media" /></picture>
</td><td>

**`NullReference`** earned a horrible reputation of an _exceptional_ pest. Its outbreaks appear literally from `nothing` and are too common to be _exceptions_ &thinsp;&mdash;&thinsp; 
they strike everywhere, in managed and unmanaged environments, and have mercy on neither junior developers nor mature systems.

[Sir Tony Hoare](../../quotes/README+/contributors/README.md#tony-hoare) voluntarily took the blame for being this Frankenstein who brought the 
[billion-dollar mistake](https://www.infoq.com/presentations/Null-References-The-Billion-Dollar-Mistake-Tony-Hoare/)<sup>🎥</sup> into the software Eden. 

A sinister _Gordian_ blockchain that nobody great can cut to stop collecting its billion toll.

**P.S.** `Null` may be disguised as `Nothing`, `nil`, `none`, `undef[ined]`, or even `NaN`.

</td></tr></table>

<sup>🎥</sup> However, if you can't make the 1950s subscripts **and** today's unassigned declarations meet &nbsp;&mdash;&nbsp; you are not alone. 

<h4 align="center">Let my shaky pen and subjective experience sketch the NullReference reflection:</h4>

```mermaid

radar-beta
 showLegend true
  axis App["A P P L I C A T I O N"], s["O W N   C O D E"], e["N E W"]
  axis OS["P L A T F O R M S"], g[" E X T E R N A L"], a[" L E G A C Y"]
  curve LOGIC["APP LOGIC"]{85, 90, 80, 70, 75, 50}
  curve PHYS["'PHYSICAL'"]{5, 9, 0, 70, 70, 90}
  curve TECH["'TECHNICAL'"]{20, 25, 20, 27, 30, 30}

  max 100
  min 0
```

* "**Physical**" &thinsp;&mdash;&thinsp; could occur when a pointer/reference comes out of physical/logical/allocated memory
* "**Technical**" &thinsp;&mdash;&thinsp; not supposed to occur. In the extreme case, a number is `null`.
* **App Logic** &thinsp;&mdash;&thinsp; actually unassigned or nulled declarations. _<samp>Mea culpa</samp>_.

In my opinion, `NullReference` is natural, and an exception over it is only a symptom. **Charging `null` for errors is like accusing `zero` for one can divide by it.**

<h2 align="center">Much Ado About <code>Nothing</code>&thinsp;?</h2>

<table><tr></tr><tr align="center"><td width="40%"><b>Y&thinsp;E&thinsp;S</b></td><td width="20%" >and</td><td width="40%" ><b>N&thinsp;O</b></td>
</tr><tr valign="center"><td>
  
Null references aren't CPU vulnerabilities as [Meltdown](https://en.wikipedia.org/wiki/Meltdown_(security_vulnerability))<sup><b>w</b></sup> that no software patch can fix. 
It's not even a peer to the Y2K problem, which stemmed from the explicit negligence to eliminate with explicit enhancement.

Botched global updates, blackouts, and catastrophic failures were caused by logical errors of different origins, in which exception names played a secondary role. 

Except one type &thinsp;&mdash;&thinsp; many disasters multiplied and spread because there was no sign of exception or error.
  
</td><td><picture><img alt="&nbsp; Yin&Yang under null sign" src="../../../../_rsc/_img/signs/YinYangNull.png" /></picture></picture></td><td>

Middle and big software providers permanently collect reports on errors, which crash their products, get handled, or run undercover (unnoticed).

Their statistics give `NullReference` the first place (from my experience too). 
Many of these errors are difficult enough to trace, reproduce, and debug, and if they aren't regular or critical, they can stay for years with the lowest priority for investigation.

Time and size populate projects' closets with ghost `NullReference` errors &thinsp;&mdash;&thinsp; the syndrome of the design decadence, which mostly gets symptomatic treatment.

</td></tr></table>

<h2 align="center">The Mistake&thinsp;?</h2>

First of all, `NullReference` is not a bubo, bug, stub, or rudiment. It's a natural, initial, and valid state of objects. And when neglected, it notifies sincerely about this rude error.

Implicit default or proforma values instead of `null` obviously pave the way to epic fails.

### Blaming the messenger

Bugs in delivered software are annoying since _1)_ [it worked on my machine](../../memes/README+/polyptych_works.md), and _2)_ they will be a headache to debug. No wonder NullReference got its reputation.

The bad idea is that silencing it may cure the problem (though sometimes it works).

### "Scapegoating" (≠ Goatscaping) 

When the source of a problem isn't evident, it's a time to explain it with the order of planets, air from bogs, bad morale, or errors of others. 
It's easier to refer the perplexed cases of `NullReference` to the peculiarities and bugs of the underlying platforms.

<h2 align="center">Null <mark>&empty;🚿</mark> Washing</h2>

**Math**, as the mother of all sciences, is believed to solve all their problems. Ironically, it has no concept of _null_ to aid its closest application. **Let's do it ourselves.**

&nbsp; &nbsp; <sup>&empty;</sup> <samp>Null in math means zero or empty set. As it's _zero_ in German.</samp>\
&nbsp; &nbsp; <sup>&empty;</sup> <samp>Hardware has a kind of &thinsp;&mdash;&thinsp; the bit or byte that state can't be read.</samp>

<p dir="rtl">.<b><code>Null</code></b> is for programming, as <code><b>zero</b></code> is for math</p>

<h1 align = "center">Part Tw&empty;. Back to keyboard</h1>

First of all, there's no magic wand to get rid of the `NullReference` errors, as clickbait titles try to sell.

Besides [quality code](../../../../software/QA/README+/code-quality.md) and apparent measures the following practices may ensure assignment:

+ Eliminating declarations\
Builders/Factories/Wizard

+ Distinguighig unset and null\
Javascript

\___________\
🔚 &empty; 2025  image credits: Wiki Commons, kyriosity
