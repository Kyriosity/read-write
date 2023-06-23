# Design - Samples

The planning and presentation of software features oblige one with a pictorial background. We'll rely often on next samples:\
|- [Chess](#chess)\
|- [Mathematics](#mathematics)\
|- [Raster images](#raster-images)

## Chess

This popular, easy to "get into" board game of all times renders a definitely favorable playground for software logic.  Other traits are...

### Reversibility, full and plain

The conventional record of moves allows one to track a finished or in-progress game back to any point. The _reverse_ is just a specular move (with the recovery of taken figures).

### Value-action substitution

A game "macro" can be either moves (*actions* that change the board) or alternating board layout (*value*, which moves result). 
The layout can be reproduced from moves and vice versa, thus mixed notation is also functional (though extraordinary).

### Multiuser

Chess assumes two players (i.e. multiuser application), who make moves in turn or decide to end the game, but there's an arbiter and timer, who follow the game and may change its progress.
Thus any action (start, move, resign, undo) requires the approval or notification of others.

### Multi-value note of the _move_

Various actors set async props of a move/action:

+ player, arbiter -> move/action notation
+ clock -> timestamp
+ player -> comment* (optional)
+ engine/expert -> assessment* (optional)

### Duration, size, space

Playing chess is predictably finite<sup>:1234:</sup>, while any initiative may unleash the figures, _8x8_ layout, or time control and as well result in perpetual movement.

&nbsp;&nbsp;&nbsp;&nbsp;<sup>:1234:</sup>&nbsp;<sub>Theory and rules limit moves to 5949 with prevailing numbers on practice far below fivescore</sub>

Concise notation of moves and layout could allow IBM&nbsp;305 RAMAC in 1957 to maintain and output an archive of all known tournaments.

## Mathematics

The study of logic and **math** with its formalism has predetermined programming. As hardware could run decent algebra instructions low and high-level languages on it could render fundamental mathematical functions for programmers.

More specific functions can be found in external libraries and if not are the subject of tailored development: from a casual task for non-mathematicians to scientific work (as some _computer-assisted-proofs_). 

* Arguments and results of functions aren't only numbers but also compound and highly abstract structures. 
* A simple or not formula may spare loads of modification storage and still be swift. 
* Contrariwise long or resource-consuming calculations can serve as _proof-of-work_, performance tests, and simulation of load.

### Reversibility

Codes may rely on mathematical *invertibility* (to undo and browse changes) while [one-way functions](https://en.wikipedia.org/wiki/One-way_function) may suit for trace or hack safety.

Values difference may suggest a math operation to reproduce, or disclose a function (e.g. one point for exponent, and two for line).

### Optimization

Parallelization (multi-threading) of algorithms, when applicable, tangibly speeds up calculations even on mediocre two-core machines.

## Raster images

Editor of raster images is the richest and multi-faceted support of thinking in application design: presentation, processing, and persistence. 
All of these three ask for optimization, equally logical and tricky.

Maps of pixels range from grayscale thumbnails to giant high-density multi-layered canvases or animations. 

### Changes

Changes on canvas differ from unique artistic strokes to strict functions and may apply to the whole image, its masked parts, selected colors, or layers. 
Actions vary from simple (flip, rotate) to highly processed retouching or effects.
