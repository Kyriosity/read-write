# "Architecture" or "Design"

Major and long-time decisions on software implementation expressed in diagrams, modules, interfaces, classes, layers, hierarchies, and patterns - is it architecture or design?

With reverence for unknown architects of the Acropolis and Colosseum, I'd voluntarily reserve the term ___architecture___ for processor families, operating systems, global computing services, and the spectrum of heterogeneous solutions.<sup>:gear:</sup>

Whereas ___design___ comprises much better the development of applications<sup>:raising_hand:</sup>, even of enterprise scale. 

&nbsp;&nbsp;&nbsp;&nbsp;<sup>:gear:</sup>&nbsp;<sub>You could have heard "architecture" addressed to _DevOps_, which also involves some development but in other though neighboring terrain.</sub>\
&nbsp;&nbsp;&nbsp;&nbsp;<sup>:raising_hand:</sup>&nbsp;<sub>Note the keyword - application. Use of somewhat developed over existing software platform for particular tasks.</sub>

## Objectives

Concerns of design (or architecture if you like) **are**:

- identification of entities, functions, and their naming,
- detection of conceptual collisions,
- partitioning (data, model, presentation, UI, biz logic),
- use of libraries, frameworks, and external services,
- planned audience and computing capacity,
- visualization, storing of modeling artifacts (at least UML sketches on whiteboards).

and are **not**: 

- user experience (UX), including tongues and assistance,
- detection of technical bottlenecks,
- versions of languages and platforms,
- details of implementation, like algorithms,
- code and docu management

## Wrapping up. Design vs. development

First, let's put away *coding* when typewriting of known design decisions fills up gaps in automation or shortages in design.<sup>:open_hands:</sup>\
&nbsp;&nbsp;&nbsp;&nbsp;<sup>:open_hands:</sup>&nbsp;<sub>Justified when generation or great design will be too arduous.</sub>

Next, I'd stick to the opinion that effective _design_ rests on direct involvement in _development_. Then where is the edge between? 
Whereas the same code can emerge under the hat of developer and designer.

Put simply: development resolves manifested design puzzles and plots, while design reveals new and cancels some previous.

The topic of design is relevant to:\
|- [Samples](readme+/design_samples.md)\
|- [C# decisions](.net/readme+/design)
