# Application model - reminder

_Model_, though a rather obscure term, is a cornerstone of software engineering, which shapes and formalizes entities and tasks of application.\
A model may rank from a dumbest `new Brick { W = 20, D = 12, H = 6,5 }` up to a universe of media franchise, from private proof of concept to enterprise solution, from bubble sort to 3D engine.

## Insight of model data

First and foremost, _model_ is not identical to _data_, its vital but nevertheless optional part. A model may render pure functionality (e.g. input and output of hash calculation).

Model data can be a homogeneous monolith of primitive data types, as well as distributed and heterogeneous high-level abstraction.\
Serving not only business or other primary data but may present collateral settings, statistics, roaming or temporary storage.

It can be:

+ hardcoded, stubbed, mocked, randomized or even _null_-ed
+ transient vs. persistent
+ read from a file, db, cloud, pipe, service, queue; recognized speech
+ plain (naked) or decorated with logic
+ with or without custom or foreign CRUD/CQRS<sup>:capital_abcd:</sup> routines

&nbsp;&nbsp;&nbsp;&nbsp;<sup>:capital_abcd:</sup>&nbsp;<sub>acronyms of **C**reate/**R**ead/**U**pdate/**D**elete and **C**ommand **Q**uery **R**esponsibility **S**egregation</sub>

### Model data and data storage

Model is not data (there're could be model with no data at all, like math processor).

:construction: TO BE WRITTEN :construction:

## Planning a model

The keystone decision is structure: whether the model will be relational, object-oriented, functional, document-oriented, sort of graph, markup,pile or other kind of disorder. It will be a challenge to swap later.\
The structure shall not imply programming language or be inspired by your language of choice. Think in pseudo-code.

## Writing a model

First and foremost, think in providers and interfaces. That is, any part of the model contacts other parts or sources from abstract providers, which easily may swap adjacent parts.
The model shall be thread and async friendly, even if it's not required. 

:construction: TO BE CONTINUED w/ EXAMPLES :construction:
