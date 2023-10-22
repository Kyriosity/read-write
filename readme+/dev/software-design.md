# Software design

## "Design" or "Architecture"?

Major and long-time decisions on software implementation expressed in diagrams, modules, interfaces, classes, layers, hierarchies, and patterns - is it architecture or design?

With reverence for unknown architects of the Acropolis and Colosseum, I'd voluntarily reserve the term ___architecture___ for processor families, operating systems, global computing services, and the spectrum of heterogeneous solutions.<sup>:gear:</sup>

Whereas ___design___ comprises much better planning of applications<sup>:raising_hand:</sup>, even of enterprise scale. 

&nbsp;&nbsp;&nbsp;&nbsp;<sup>:gear:</sup>&nbsp;<sub>You could have heard "architecture" addressed to _DevOps_, which also involves some development but in other though neighboring terrain.</sub>\
&nbsp;&nbsp;&nbsp;&nbsp;<sup>:raising_hand:</sup>&nbsp;<sub>Note the keyword - application. Use of somewhat developed over existing software platform for particular tasks.</sub>

## Objectives of design

Concerns of design (or architecture if you like) **are**:

- identification of entities, functions, and their naming,
- detection of conceptual collisions,
- partitioning (data, model, presentation, UI, biz logic),
- use of libraries, frameworks, and external services,
- planned audience and computing capacity,
- visualization, modeling artifact storage (at least UML sketches on whiteboards).

and are **not**: 

- user experience (UX), including tongues and assistance,
- detection of technical bottlenecks,
- versions of languages and platforms,
- details of implementation, like algorithms,
- code and docu management

## Design vs. Development

First, let's put away *coding* when typewriting of known design decisions fills up gaps in automation or shortages in design.<sup>:open_hands:</sup>\
&nbsp;&nbsp;&nbsp;&nbsp;<sup>:open_hands:</sup>&nbsp;<sub>Quite reasonable when generation or great design will be too arduous.</sub>

Next, I'd stick to the opinion that effective _design_ rests on direct involvement in _development_. Then where is the edge between? 
Whereas the same code can emerge under the hat of developer and designer.

Put simply: development resolves manifested design puzzles and plots, while design reveals new and cancels some previous.

## Pitfalls

Besides apparent perfectionism, sand castles, and NAIVE reinventing, the next trivia often undermines the way of design:

<details>
<summary>🚧<ins>&nbsp;<b>Too low-level, too high-level involvement</b>&nbsp;</ins></summary>
// TO BE explained

</details>

<details>
<summary>🚧<ins>&nbsp;<b>Surrenders thought as compromises</b>&nbsp;</ins></summary>
// TO BE explained

</details>

<details>
<summary>🚧<ins>&nbsp;<b>"Tunnel vision"</b>&nbsp;</ins></summary>
// TO BE explained

</details>

<details>
<summary>🚧<ins>&nbsp;<b>Routine by frustration</b>&nbsp;</ins></summary>
// TO BE explained

</details>

## What about UML ?

🚧 To be written...

## Wrapping up. Further topics

The topic of design is relevant to:\
|- [Samples](readme+/design_samples.md)\
|- [C# decisions](.net/readme+/design)\
|- DOCU! (which is not design)
