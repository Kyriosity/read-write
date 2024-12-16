# Software &mdash; Quality Assurance &mdash; Programmatic tests

<table><tr valign="top"><td><picture><img width="300px" alt="&nbsp;Software tests pyramid" src="../../../_rsc/_img/illus/test_pyramid-500px.jpg"></picture><br />
(every test subject is a unit of its own)</td><td>
  <p><i>Programmatic test</i> <b>is a fundamental QA stone.</b></p>
<blockquote><b>Programmatic ≠ automated.</b><br />But tests are the intrinsic subject of automation when applicable and beneficial.</blockquote>
</td></tr></table>

## Test frameworks and languages

Writing tests in the language of their subjects is natural, practical, and facilitates [TDD](../asDrive), but

- UI has no programming language (like other amorphous themes).
- Some languages (SQL) or markup (HTML) aren't suited to describe tests or are too obsolete (mostly to be maintained).
- A domain may be written in a set of languages, or similar requirements implemented with different tools (e.g. JavaScript for front- and Java for backend).

Solution? Any popular language has some mainstream frameworks. As well many frameworks allow tests of UI and modules written in any language.<sup>🏛️</sup>\
&nbsp;&nbsp;&nbsp;&nbsp;<sup>🏛️</sup> <sub>E.g. even old and rare languages got test support as fastly found for reference [cobol-check](https://github.com/openmainframeproject/cobol-check).</sub>

## Automation

// ToBe written

## Down to the practice

The more pragmatic use-dev repo discusses and renders [tests stuff](https://github.com/Kyriosity/use-dev/tree/main/README+/tests).

\___________\
🔚 ... but [README+](README+) ...
