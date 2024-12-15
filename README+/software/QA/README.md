# Software &mdash; Quality Assurance (QA)

> **Frivolous, fleeting, and exponential spirit makes the programming inherently and largely error-prone** (and QA-fated). 

Software is pure abstraction ether, where breaking changes are as close as their fingers to the keyboard. Commits can be rolled back, and there's always a gap until delivery to production (for last-minute fixes or bug introduction).

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

**QA** couldn't exist without errors - the catch-all term which inmates deserved their own [corner](README+/errors/).

## Natural born quality

There were and will be remarkable projects done from scratch without allotted proof and validation measures (let alone code reviews and test automation) but robust from the first release. 
This may (and _may not_) happen in localized high-pro teams of responsible individuals but is an exclusion to underline the must-have of __QA__.

> Writing [quality code](README+/code-quality.md) must be an objective but teams will be uneven, distributed/fluctuating, and stressed. Add the human nature to sweep problems under the carpet - quite big and thick in the software.

## Preliminary

Experience in

+ domain/subjects,
+ tools (as a platform and programming language),
+ fails and retreats (also of others).

When security risks are a concern other approaches for hacking vulnerability come into play (and devs aren't writing code in a criminal-minded mode).
Protrude this statement to all other cases where IT pundits don't have all the expertise to test the domain.

## Production

<table><tr><td><picture><img width="250px" alt="&nbsp;Drake helps Lil Yachty with laptop (&quot;Life Is Good&quot;)" title="&nbsp;Drake helps Lil Yachty with laptop (&quot;Life Is Good&quot;)" src="../../_rsc/_img/memes/Drake_LilYachty-LifeIsGood_laptop.jpg" /></picture></td><td>
 <p>These are continuous measures within the team:</p>
 <ul>
  <li>Code reviews, pair programming, friendly discussions, and lessons.</li>
  <li>Preferred approaches as <a href="../tests/asDrive/">Test Driven Development</a>.</li>
 <li>Selection of popular or custom <a href="https://github.com/Kyriosity/use-dev/tree/main/README+/frames">guidelines</a> and <a href="https://github.com/Kyriosity/use-dev/tree/main/README%2B/techniques">techniques</a>.</li>
 </ul>
</td></tr></table>

## Produced

### Feedback

Customer feedback is the top mark (not only on the positive scale) and not every user is eager to share it.

### Tests

_Tests_ and _Testing_ are a CENTERPIECE of QA and <ins>&thinsp;w&thinsp;i&thinsp;d&thinsp;e&thinsp;</ins> umbrella terms for the check of code and its products (including documentation). Bug searching and quality proofing tests are optional but highly recommended and a natural share of software creation. 

### Manual (spontaneous and planned)

Opening this page was your manual test. 
 
Unlike the olden days with blind commits of punchcards and tapes most development allows one to evaluate its product (in whole or by feature) with every step and at time: just build and run.

This makes the developer the original, most prepared, and, when responsible, most effective and critical tester.

### Programmatic tests

[Programmatic tests](../tests) - executable code routines - are the biggest cornerstone of modern QA.

#### Test automation

// ToDescribe:

\___________\
:end: ... continued in ... [Errors](README+/errors/) ... [Code quality](README+/code-quality.md) ... [QA Tests](../tests/asQA/) ... [Pitfalls](README+/QA-pitfalls.md) ... TDD
