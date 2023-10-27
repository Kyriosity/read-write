# Software design - private derivations

## "Design" or "Architecture"?

Major and long-time decisions on software implementation expressed in diagrams, modules, interfaces, classes, layers, hierarchies, and patterns - is it architecture or design?

With reverence for unknown architects of the Acropolis and Colosseum, I'd voluntarily reserve the term ___architecture___ for processor families, operating systems, global computing services, and the spectrum of heterogeneous solutions.<sup>:gear:</sup>

Whereas ___design___ comprises much better outlining of applications<sup>:raising_hand:</sup>, even of enterprise scale.

&nbsp;&nbsp;&nbsp;&nbsp;<sup>:gear:</sup>&nbsp;<sub>You could have heard "architecture" addressed to _DevOps_, which also involves coding/scripting in other though neighboring terrain.</sub>\
&nbsp;&nbsp;&nbsp;&nbsp;<sup>:raising_hand:</sup>&nbsp;<sub>Note the keyword - application. Use of somewhat developed over existing software platform for exact tasks.</sub>\

## Objectives of design

Concerns of design (or architecture if you like) **are**:

+ identification of entities, functions, and the [naming](/readme+/dev/code-naming.md/) of them,
+ detection of conceptual collisions, // ToDo: example required
+ [partitioning](/readme+/dev/software-parts/) (data, model, presentation, UI, biz logic),
+ use of [external](/readme+/dev/software-parts/ext_parts.md) libraries, frameworks, and services,
+ principal [language-specific decisions](.net/readme+/design)\
+ maintenance of [design samples](readme+/design_samples.md)
+ planned audience and computing capacity, // ToDo: EXPLAIN
+ visualization and presentation of modeling (like UML sketches)

and are **not**: 

- user experience (UX), including tongues (unless it's a linguistic app) and assistance,
- detection of technical bottlenecks, // ToDo: example required
- versions of languages and platforms,
- details of implementation, like algorithms, // ToDo: ReThink
- code and docu management (as management system choice),
- maintenance of documentation 

## The role of the designer (architect).

I'd stick to the opinion that effective _design_ rests on direct involvement in _development_.

// To BE WRITTEN 🚧

## Design vs. Development

First, let's put away *coding* when typewriting of known design decisions fills up gaps in automation or shortages in design.<sup>:open_hands:</sup>\
&nbsp;&nbsp;&nbsp;&nbsp;<sup>:open_hands:</sup>&nbsp;<sub>Quite reasonable when generation or great design will be too arduous.</sub>

The same code can emerge under the hat of the developer and designer. Then what is the edge between? 

Put simply: development resolves manifested design puzzles and plots, while design reveals new and cancels some previous. There's no edge since design and dev work intercepts much.

## Pitfalls

Besides trivial perfectionism, self-overestimate, and epic fails the next trivia often undermines the way of design:

<details>
<summary>🚧<ins>&nbsp;<b>Too much low-level share</b>&nbsp;</ins></summary>
// TO BE explained
  
  Burden of
  
Is a counter-part of high-level

</details>

<details>
<summary>🚧<ins>&nbsp;<b>Too little middle-level share</b>&nbsp;</ins></summary>
// TO BE explained
Is a counter-part of high-level

It's about DIVERSION

</details>

<details>
<summary>🚧<ins>&nbsp;<b>Surrenders admitted as compromises</b>&nbsp;</ins></summary>
// TO BE explained

</details>

<details>
<summary>🚧<ins>&nbsp;<b>"Tunnel vision"</b>&nbsp;</ins></summary>
// TO BE explained

</details>

<details>
<summary>🚧<ins>&nbsp;<b>Degradation to formalism</b>&nbsp;</ins></summary>
// TO BE explained

</details>

