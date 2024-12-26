# Application model &mdash; Reminder

The _Model_, though a rather obscure term, is a cornerstone of software engineering, which shapes and formalizes entities and tasks of the application.

A model may rank from the dumbest `new Brick { w = 20, d = 12, h = 6,5 }` up to a universe of media franchises, from private proof of concept to enterprise solution, bubble sort to 3D engine.

## Insight into model data

First and foremost, _model_ is not identical to _data_, it's a vital but optional part. A model may render non-memorized processing (e.g. input and output of hash calculation).

Model data can be a homogeneous monolith of primitive data types, as well as distributed and heterogeneous high-level abstraction.\
Serving not only business or other primary data but may present collateral settings, statistics, roaming, or temporary storage.

It can be:

+ hardcoded, stubbed, mocked, randomized, or even _null_-ed
+ transient vs. persistent
+ read from a file, db, cloud, pipe, service, queue; recognized speech
+ plain (naked) or decorated with logic
+ with or without custom or foreign CRUD/CQRS<sup>:capital_abcd:</sup> routines

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<sup>:capital_abcd:</sup>&nbsp;<sub>acronyms of **C**reate/**R**ead/**U**pdate/**D**elete and **C**ommand **Q**uery **R**esponsibility **S**egregation</sub>

### Model data and data storage

The model is not data (there could be a model with no data at all, like a math processor).

:construction: TO BE WRITTEN :construction:

## Planning a model

The keystone decision is structure: whether the model will be relational, object-oriented, functional, document-oriented, sort of graph, markup, pile, or other kind of disorder. It will be a challenge to swap later. 

The structure shall not imply programming language or be inspired by your language of choice. Think in pseudo-code.

## Writing a model

First and foremost, keep in mind providers and interfaces. That is, any part of the model contacts other parts or sources from abstract providers, which easily may swap adjacent parts.
The model shall be thread- and async-friendly, even if it's not required. 

:construction: TO BE CONTINUED w/ EXAMPLES :construction:

**Further reading:**\
|- [Tasks as models](https://github.com/Kyriosity/use-dev/blob/main/README%2B/decisions/README%2B/model_as_tasks.md) ➡️(use-dev)

🔚
