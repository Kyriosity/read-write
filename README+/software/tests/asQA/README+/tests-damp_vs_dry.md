# Programmatic Tests &mdash; DAMP not DRY

<table><tr><td><p>Either <a href="../../asDrive">TDD</a> or proof of the provided code, <b>a conventional approach</b> is to</p>
    <ul>
        <li>pick a software <b>entity</b> (class, function, or something else),</li>
        <li>consider a significant <b>use case</b> of it,</li>
        <li>and write a <b>test method</b> over this.</li>
    </ul>
</td><td><p align="center">
↗️&nbsp;<b>A<samp>RRANGE</samp></b>&nbsp;➡️ <br />➡️&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<b>A<samp>CT</samp></b>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;➡️ <br />➡️&nbsp;&nbsp;<b>A<samp>SSERT&nbsp;&nbsp;↩️</samp></b></p></td><td>
    After polishing the logic and wording,<br />consider and write other test cases. 
</td></tr></table>

Developing tests this way shall (<ins>not guaranteed</ins>) wrap features in pleasant _<b>D</b>escriptive <b>A</b>nd <b>M</b>eaninigful <b>P</b>hrases_ (_abbr._ <b>DAMP</b>).\
&nbsp;&nbsp;&nbsp;&nbsp;<sub>Particularly with adorning tools like [Cucumber](https://cucumber.io/docs/guides/10-minute-tutorial/?lang=java#write-a-scenario) that wrap tests into phrases, apprehensible not only by programmers but normal folks.</sub>

No need to point out the virtues of this approach but one great flaw: <ins>&nbsp;<b>S&thinsp;I&thinsp;Z&thinsp;E</b>&nbsp;</ins> &mdash; fermented by number of cases, rows of data, and their combinations, shared functionality, and repeating steps for alternative actions or different asserts.

<table><tr><td><picture><img alt="&nbsp;Black box of test (not of application)" src="../../../../_rsc/_img/memes/ItTestsSmth.jpg" /></picture>
</td><td>
<p>Dveloping tests this way will create a sound core, which with little documentation will describe the application and prove code essentials.</p>
<p>Adding more and more tests will slightly dissolve this core into a badly exorbitant maintainable bulk. With scrappy coverage, accumulated negligence, and impeded navigation.</p>    
</td></tr></table>

Another option is continuous refactoring with **DRY** (<i><b>D</b>on't <b>R</b>repeat <b>Y</b>ourself</i>) first of all.

# <samp>DRY</samp> it - <samp>A</samp>rrange

## Feed expansion

```mermaid
graph TD
    idCx[(Context<br />&lpar;Arrange&rpar;)] -->|<br />&nbsp;&nbsp;Arguments,&nbsp;&nbsp;<br />&nbsp;&nbsp;Test Data,&nbsp;&nbsp;<br />&nbsp;&nbsp;Settings&nbsp;&nbsp;<br />...| UT(TEST<br />Arange/Act/Assert)
    idFnc((Functionality<br />&lpar;Act&rpar;)) -->|<br />&nbsp;&nbsp;Implementation A, B, C, ...&nbsp;<br >&nbsp;Sample func, ...&nbsp;</br>&nbsp;Stubs, Dummies&nbsp;&nbsp;<br />...| UT
    idSrv>Providers<br />&lpar;Arrange&rpar;] -->|<br />&nbsp;&nbsp;Imports, Services&nbsp;&nbsp;<br />&nbsp;&nbsp;vs. Mocks, Doubles&nbsp;&nbsp;<br />...| UT
    idAbs{Input abuse<br />&lpar;Arrange, Act&rpar;} -->|&nbsp;&nbsp;<i>null</i>s, out-of-range&nbsp;<br />&nbsp;&nbsp;<i>exception</i> makers,&nbsp;<br />&nbsp;invalid/illegal calls/funcs&nbsp;<br />...| UT

```

use-dev [decisions](https://github.com/Kyriosity/use-dev/blob/main/README+/tests/README+/prog_tests-cut_feeds..md)

### Dimensional growth

### Combinatorial explosion

This is the greatest hit.

## Arrange &mdash; Multitype

Add here that argument combinations can matter and their MULTITYPE POLY (e.g. integer and floating point for the same calculation and even values).

# <samp>DRY</samp> it - <samp>A</samp>ssert

Then asserts are **Y** axis

### Single or multiple


Napo Leon

## Wrap up. DRY but not drain 

DAMP or DRY? Neither but a compromise. 
ERODE BUT KEEP

Was it all about unit tests? Yes, but it can work for others in the pyramid. ELUSIVE and NO DISTINCT DIVISION

Does it concern Test Driven Design? Yes but with the bias that DAMP must prevail there.

🔚

