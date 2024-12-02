# Software &mdash; Quality Assurance (QA)

> **Frivolous, fleeting, and exponential spirit makes the programming inherently and largely error-prone** (and QA-fated). 

Software is pure abstraction ether, and its creators have no fear of breaking changes (as close as their fingers to the keyboard). Commits can be rolled back, and there's always a gap until delivery to production (for last-minute fixes or bugs introduction).

```mermaid
graph TB
 c1-->QA2
    subgraph "<h3><a href="https://github.com/Kyriosity/read-write/tree/main/README%2B/software/tests">Programmatic Tests</a></h3>"
    c1("<b>Proof</br>coverage</b>")
      TDD("<b>Test driven</b>")-->TDDev("Development")
      TDD-->TDDes("Design")
     c1 o--o TDDev
    end
    subgraph "<h3>Quality Assurance</h3>"
    a1(<b>Code</b>)-->a2(<a href="https://github.com/Kyriosity/read-write/blob/main/README%2B/software/QA/README+/code-quality.md">Quality</a>)
  a1-->a3("Review")
    T1("<b>Testing</b>")-->QA1("Manual")
    T1("<b>Testing</b>")-->QA2(Automated)
    end
```

## Errors

**QA** couldn't exist without errors, which are not only bugs but poor performance, frustrating user experience, missing functionality, and ... concealed features.

A dedicated discussion deserves to be packed in its own [Errors](README+/errors/) subfolder.

## Natural born quality

There were and will be remarkable projects done from scratch without allotted proof and validation measures (let alone code reviews and test automation) but robust from the first release. 
This may (and _may not_) happen in localized high-pro teams of responsible individuals but is an exclusion to underline the must-have of __QA__.

Writing [quality code](README+/code-quality.md) must be an objective but teams will be uneven, distributed/fluctuating, and stressed. Add the human nature to sweep problems under the carpet - quite big and thick in the software.

## Preliminary

Experience... 

When security risks are a concern other approaches for hacking vulnerability come into play (and devs aren't writing code in a criminal-minded mode).
Project this statement to all other cases where IT pundits don't have all the expertise to test the domain.

## Production

Guidelines, Code review, 

## Released

_Tests_ and _Testing_ are great umbrella terms for the check of code and its products (including documentation). Bug searching and quality proofing tests are optional but highly recommended and a natural share of software creation. 

### Manual (spontaneous and planned)

Unlike the olden days with blind commits of punchcards and tapes most development allows to evaluate its product (in whole or by feature) with every step: just build and run.

This makes the developer the original, most prepared, and, when responsible, most effective and critical tester.

### Programmatic tests

[Programmatic tests](../tests) - executable code routines - are the biggest cornerstone of modern QA.

#### Test automation

// ToDescribe:

\___________\
:end: ... but [README+](README+)
