# Software - Models

The planning and presenting of software features oblige one with pictorial background. We'll rely on the next samples more than others.

## Chess

This popular, easy to "get into" board game of all times renders a definitely favorable playground for software logics.  Other traits are...

### Reversibility: full and plain

With conventional record of moves any game can be tracked back to any point. Reverse is just a specular move (with recovery of taken figures).

### Value-action: mutual substitution

A game "macro" can be either moves (*actions* that change the board) or alternating board layout (*value*, which moves result). 
Layout can be reproduced from moves and vice versa, thus mixed notation is also functional (though extraordinary).

### Multiuser

Chess assumes two players, who make moves in turn or decide to end the game, but there's an arbiter and timer, who follow the game and may change its progress.
Thus any action (start, move, resign, undo) requires approval or notification of others.

### Not only move

Various actors set async props of a move/action:

+ player, arbiter -> move/action notation
+ player -> comment (optional)
+ clock -> timestamp
+ engine/expert -> assessment (optional)


### Boundaries: duration, size and space

Playing chess is predictably finite<sup>:1234:</sup>, while any initiative may unleash the figures, 8x8 layout or time control and also result in perpetual movement.

&nbsp;&nbsp;&nbsp;&nbsp;<sup>:1234:</sup>&nbsp;<sub>Theory and rules limit moves to 5949 with prevailing numbers on practice far below fivescore</sub>

Concise notation of moves and layout could allow IBM&nbsp;305 RAMAC in 1957 to maintain archive of all known tournaments and present on demand.

## Mathematics

The study of logic and **math** with its formalism has predetermined programming. 
And as hardware instructions could run decent algebra low-to-high level languages could render mostly used mathematical functions for users.
More specific functios can be found in external libraries and if not are subject of tailored development: from casual task to scientific work. 

Math funcs inputs and results aren't only numbers but compound and highly abstract structures. 
A simple or not formula may spare loads of modifications storage and still be swift. 
Contrariwise long or resource consuming calculation can serve as _proof-of-work_, performance tests, simulation of load.

### Reversibility

Codes may rely on mathematical *invertibility* (to undo, browse changes) while [one-way functions](https://en.wikipedia.org/wiki/One-way_function) may suite for trace or hack safity.

Values difference may suggest a math operation to reproduce, or disclose a function (e.g. one point for exponent, and two for line).

### Optimization

Parallelization (multi-threading) of algorithms, mostly applicable, tangiably speeds up calculations even on mediocre two-core machines.

## Raster images

Editor of raster images is the richest and multi-faceted support of thinking in application design: presentation, processing and persistence. 
All of these three ask for optimization, both logical and tricky.

Maps of pixels range from grayscale thumbnails to giant high-density multi-layered canvases or animations. 

### Changes

Changes on canvas differ from unique artisctic strokes to strict functions, and may apply to the whole image, its masked parts, selected colors or layers. 
Actions vary from simple (flip, rotate) to highly processed retouching or effects.
