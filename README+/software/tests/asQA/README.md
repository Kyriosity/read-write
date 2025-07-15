# Software &nbsp;&mdash;&nbsp; <samp>Quality Assurance</samp> &rarr; Programmatic Tests

<table><tr valign="top"><td><picture><img width="400px" alt="&nbsp;Software tests pyramid" src="../../../_rsc/_img/illus/tests/test_pyramid-deco-750px.jpg"></picture></td><td>
  <h3><i>Programmatic test</i> is a QA cornerstone.</h3>
  <p>Though unit tests are at the bottom of the pyramid, any high-level test subject is a unit of its own.</p>
  <p>This works in the opposite direction: no atomic test unit could be dissolved into a lesser unit (to cover rationally without the explosion of code size). 
  Our unit tests always drag lower-level units.</p>
</td></tr></table>

## Test frameworks and languages

Writing tests in the language of their subjects is natural, practical, and facilitates [TDD](../asDrive), but

- UI has no programming language (like other amorphous themes). Amd markuo isn't one.
- Some languages (as SQL, scripts, or lower level) aren't suited to describe tests or may be too obsolete (neglected).
- A domain may be written in a mix of languages, or similar requirements can be implemented with different tools (e.g., JavaScript with typescript for front-end and Java/C#/JS for backend).

Solution? Any popular language has some mainstream frameworks. Many frameworks also allow tests of UI, units/modules written in other languages, or API.<sup>🏛️</sup>

&nbsp; &nbsp; &nbsp;<sup>🏛️</sup> <samp> E.g., even old and rare languages got test support as fastly found for reference [Cobol-check](https://github.com/openmainframeproject/cobol-check)<sup>:octocat:</sup>.</samp>

## Automation

<blockquote><b>Programmatic ≠ automated.</b><br />But tests are the intrinsic subject of automation when applicable and beneficial.</blockquote>

// ToBe written 🚧

## Down to the practice

The more pragmatic use-dev repo discusses and renders [tests stuff](https://github.com/Kyriosity/use-dev/tree/main/README+/tests).

## Poststriptum. Big problem and challenge

With all the benefits of proof coverage and TDD<sup>eV</sup>, tests constitute a second project that requires development and maintenance. 

\___________\
🔚 ... but [README+](README+) &nbsp; ... &nbsp; <sub>collage credit: LibreOffice clipart; The Outer Limits.The&nbsp;Mutant, 1964 (imdb screenshot)</sub>
