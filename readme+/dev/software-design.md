# "Architecture" or "Design"

Decisions on how software solutions will be implemented in terms of top diagrams, modules, interfaces, classes, layers, hierarchies, patterns -- is it architecture or design?

Voluntary, with reverence for architects of Acropolis and Colosseum, I'd reserve the term ___architecture___ for processor families, operating systems, global computing services, spectrum of heterogeneous solutions.<sup>:gear:</sup>\
&nbsp;&nbsp;&nbsp;&nbsp;<sup>:gear:</sup>&nbsp;<sub>"Architecture" could be heard in the address of DevOps, which also takes some development but is other though neighbouring terrain.</sub>

Whereas ___design___ comprises much better the development of applications, even of enterprise scale. Note the keyword - application (use of somewhat developed for particular tasks).

Concerns of design (or architecture if you like) **are**:
- identification of entities, functions, and their naming,
- detection of conceptual collisions,
- partitioning (data, model, presentation, UI, biz logic),
- use of libraries, frameworks and external services,
- planned audience and computing capacity,
- visualization, storing of modeling artifacts (at least UML sketches on whiteboards).

and are **not**: 

- user experience (UX), including tongues and assistance,
- detection of technical bottlenecks,
- versions of languages and platforms,
- details of implementation, like algorithms,
- code and docu management

Design comes togethers with next topics:\
|- [Samples](readme+/design_samples.md)\
|- [C# decisions](.net/readme+/design)

## Wrapping up. Design vs. development

First, let's omit *coding*, when typewriting of known design decisions fills up gaps in automation or shortages in design.<sup>:open_hands:</sup>\
&nbsp;&nbsp;&nbsp;&nbsp;<sup>:open_hands:</sup>&nbsp;<sub>Justified when automation or great design will be too arduous.</sub>

Next, I'd share the opinion that effective _design_ rests on direct involvement in _development_. Then where is the edge between? 
Whereas the same code can emerge under the hat of developer and designer.

Put simply: development resolves manifested design puzzles and plots, while desing reveals new and cancels some previous.
