# Software &mdash; <samp>Quality Assurance</samp> &rarr; Programmatic Tests

<table><tr valign="top"><td><picture><img width="400px" alt="&nbsp;Software tests pyramid" src="../../../_rsc/_img/illus/tests/test_pyramid-deco-750px.jpg"></picture></td><td>
  <h3><i>Programmatic test</i> is a fundamental QA stone.</h3>
  <p>Though unit tests are at the bottom of the pyramid any high-level test subject is a unit of its own.</p>
  <p>This works in the opposite direction: there's no atomic test unit that couldn't be dissolved into lesser (to cover rationally without the explosion of code size). 
  Our unit tests always drag lower lever units.</p>
</td></tr></table>

## Test frameworks and languages

Writing tests in the language of their subjects is natural, practical, and facilitates [TDD](../asDrive), but

- UI has no programming language (like other amorphous themes).
- Some languages (SQL) or markup (HTML) aren't suited to describe tests or are too obsolete (mostly to be maintained).
- A domain may be written in a set of languages, or similar requirements implemented with different tools (e.g. JavaScript for front- and Java for backend).

Solution? Any popular language has some mainstream frameworks. Many frameworks also allow UI tests and modules written in any language.<sup>🏛️</sup>\
&nbsp;&nbsp;&nbsp;&nbsp;<sup>🏛️</sup> <sub>E.g. even old and rare languages got test support as fastly found for reference [Cobol-check](https://github.com/openmainframeproject/cobol-check).</sub>

## Automation

<blockquote><b>Programmatic ≠ automated.</b><br />But tests are the intrinsic subject of automation when applicable and beneficial.</blockquote>

// ToBe written

## Down to the practice

The more pragmatic use-dev repo discusses and renders [tests stuff](https://github.com/Kyriosity/use-dev/tree/main/README+/tests).

## Poststriptum. Big problem and challenge

With all the benefits of the proof coverage and TDD<sup>eV</sup>, tests make up a second project requiring development and maintenance. 

\___________\
🔚 ... but [README+](README+) ... <sub>collage credit: LibreOffice clipart; The Outer Limits.The&nbsp;Mutant, 1964 (imdb screenshot)</sub>
