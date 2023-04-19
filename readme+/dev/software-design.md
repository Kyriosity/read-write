## Architecture vs. design

Decisions on how software solutions will be written in terms of top diagrams, modules, interfaces, classes, layers, hierarchies, patterns -- is it architecture or design?\
Voluntary<sup>:house:</sup> I'd reserve the term ___architecture___ for processors' lines, operating systems, global computing services, spectrum of IT solutions.\
&nbsp;&nbsp;&nbsp;&nbsp;<sup>:house:</sup>&nbsp;<sub>with reverence for architects of Acropolis and Colosseum</sub>

Whereas ___design___ comprises much better the development of applications, even of enterprise scale. Note the keyword - application (use of somewhat developed for particular tasks).

Other concerns of design (or architecture if you like) are:
- identification of entities, functions and their naming,
- detection of conceptual collisions,
- visualization, storing of modeling artefacts (at least UML sketches on whiteboards),
- partitioning (data, model, presentation, UI, biz logic)
- use of libraries, frameworks and external services
- planned audience and computing capacity

and are not: 
- user experince (UX), incl. tongues and assistance
- detection of technical bottlenecks,
- versions of languages and platforms 
- algorithms and patterns,
- any details of implementation,
- code and docu managemement

Design reveals further topics:\
|- [Samples](readme+/design_samples.md)\
|- [C# design decisions](.net/readme+/design)
