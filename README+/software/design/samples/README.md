# Design - Samples

The planning and presentation of software features require a pictorial and encouraging background. We'll rely often on the next samples:\
|- ♟️ [Chess](#chess)\
|- 🧮 [Math](#math)\
|- 🎨 [Raster images](#raster-images)\
|- 🧱 [Still plain models](#still-plain-models)

## Chess

<p dir=rtl>Chess speaks for itself<br><i><b>Hans Moke Niemann</b>, GM, 2022</i></p>

This popular board strategy of all times with fast-to-learn rules renders a favorable playground for software logic.  Other traits are...

### Reversibility: full and plain

The conventional record of moves allows one to track a finished or in-progress game back to any point. The _reverse_ is just a specular move (with the recovery of taken figures).

### Value-action substitution

A game "macro" can be either moves (*actions* that change the board) or alternating board layout (*value*, which moves result). 
The layout can be reproduced from moves and vice versa, thus mixed notation is also functional (though extraordinary).

### Multiuser

Chess assumes two players (i.e. multiuser application), who make moves in turn or decide to end the game, but there's a judge and timer, who follow the game and may change its progress.
Thus any action (start, move, resign, undo) requires the approval or notification of others.

### Multi-value note of the _move_

Various actors set async props of a move/action:

+ player, arbiter &rarr; move/action notation
+ clock &rarr; timestamp
+ player &rarr; comment* (optional)
+ engine/expert &rarr; assessment* (optional)

### Duration, size, space

Playing chess is predictably finite<sup>:1234:</sup>, while any initiative may unleash the figures, _8x8_ layout, or time control and result in perpetual movement.\
&nbsp;&nbsp;&nbsp;&nbsp;<sup>:1234:</sup>&nbsp;<sub>Theory and rules limit moves to 5`949 with prevailing numbers on practice far below fivescore.</sub>

Concise notation of moves and layout could allow IBM&nbsp;305 RAMAC in 1957 to maintain and output an archive of all known tournaments.

---

## Math

<p dir=rtl>,If numbers aren't beautiful<br />.I don't know what is<br ><i><b>Paul Erdos</b> (1913-1996)<br />ultra-mathematician</i></p>

The study of logic and **math** with its formalism has predetermined programming. As hardware could run decent algebra instructions low and high-level languages on it could render fundamental mathematical functions for programmers.

More specific functions can be found in external libraries and if not are the subject of tailored development: from a casual task for non-mathematicians to scientific work (as some _computer-assisted-proofs_). 

* Arguments and results of functions are not only numbers but also compound and highly abstract structures. 
* A simple or not formula may spare loads of modification storage and still be swift. 
* Contrariwise long or resource-consuming calculations can serve as _proof-of-work_, performance tests, and simulation of load.

### Reversibility

Codes may rely on mathematical *invertibility* (to undo and browse changes) while [one-way functions](https://en.wikipedia.org/wiki/One-way_function)<sup><b>w</b></sup> may suit for trace or hack safety.

Values difference may suggest a math operation to reproduce, or disclose a function (e.g. one point for an exponent, and two for a line).

### Optimization

Parallelization (multi-threading) of algorithms, when applicable, tangibly speeds up calculations even on mediocre two-core machines.

---

## Raster images

<p dir=rtl>,When I am in a painting<br>.I'm not aware of what I'm doing<br><i><b>Jackson Pollock</b> (1912-1956) </i></p>

Editor of raster images is the richest and most multi-faceted support for thinking in application design: presentation, processing, and persistence. 
All of these three ask for optimization (equally logical and tricky).

Maps of pixels range from grayscale thumbnails to giant high-density multi-layered canvases or animations. 

### Changes

Changes on canvas differ from unique artistic strokes to strict functions and may apply to the whole image, its masked parts, selected colors, or layers. 
Actions vary from simple (flip, rotate) to highly processed retouching or effects.

---

## Still plain models

<p dir=rtl>In some mysterious way woods have<br />
.never seemed to me to be <mark>static</mark> things<br />
;In physical terms, I move through them<br />
,yet in metaphysical ones<br />
.they seem to move through me<br />
___________<br />
<b>John Fowles</b> (1926-2005), <i>[post]modernist</i></p>

<ins>First and foremost</ins>, software design asks for "static" bare figures, which make core models. The preceding samples are more functional ("dynamic") &mdash; they have properties and hierarchies but are more demonstrative of processes that change them.

"Static" models can be altered and async too, but they must demonstratively represent hierarchies, parametrization, and initialization. 
One of their custom implementations is available as use-dev➡️ [AbcModels](https://github.com/Kyriosity/use-dev/tree/main/src/TuttiFrutti/AbcModels).

---

## Wrapping up

Developers can select this or that sample/model that fits features under development, and implement (or re-use) prototypes with tests. 

However, put them all together on the mental green field of growing application to plan:

+ multitasking,
+ multi-culture,
+ undo-redo,
+ conversions.

and mix them (e.g. async undo-redo,  or multi-culture as units).

---

🔚
