# Test Drive &nbsp;&mdash;&nbsp; Big Watershed

<table><tr valign="center"><td>
<picture><img width="250px" alt="&nbsp;Y-fork: black on yellow" src="../../../../../_rsc/_img/signs/road/Y-fork_yellow(cleanpng.com)_250px.png" title="&nbsp;Courtesy of www.cleanpng.com" /></picture>    
</td><td><p>In rainy midsummer 2024 I was bicycling to hear a casual <b>TD<mark>D</mark></b>  lecture as doubts crept in &mdash; where am I going:</p>
   <p align="center">Must this <mark><b>D</b></mark> be for <b><i>Design</i></b> or <b><i>Development</i></b>❓</p>
<p>It wasn't about the destination of this ride, but the principal divergence. 
For the record, the title of the lecture resonated with my anxiety:  "Failed with TDD? Here you know why."</p>
<p align="center">Mystery solved: it was <a href="https://en.wikipedia.org/wiki/Test-driven_development">Test Driven <b>Development</b></a><sup><b>w</b></sup>.</p>
</td></tr></table>

But the de-abbreviation raised another doubt: where's _Design_? &mdash; I actively searched by <kbd>**T&thinsp;D&thinsp;D**</kbd> and fairly retrospected the found&nbsp;...<sup>🙋</sup> 

Presentations and lectures favored _development_ with _design_ as a natural<sup>🌵</sup> spin-off, not much bothering about distinction and some exploited both terms interchangeably. 
Books and tutorials showed up inclined to techniques, patterns, and testing frameworks.

Test-driven Development, fine for discourses, bootcamps, and `class`<samp>es</samp>, and encouraging to start features, didn't set forth for me to design just a mediocre project: hypothetical or tried.

&nbsp;&nbsp;&nbsp;&nbsp;<sup>🙋</sup> <sub>Albeit being energetic in the recherche I couldn't go through the best part of treatises. There must be better findings, and there could be better alternating conclusions.</sub>\
&nbsp;&nbsp;&nbsp;&nbsp;<sup>🌵</sup> <sub><b>Natural</b> since any complete snippet can't escape design or must fit into the given.</sub>

<table align="center" valign="center"><tr><td>⬇️&nbsp;&nbsp;<b>I&thinsp;N&thinsp;T&thinsp;E&thinsp;N&thinsp;T&thinsp;I&thinsp;O&thinsp;N&thinsp;A&thinsp;L&thinsp;L&thinsp;Y</b></td>
   <td align="center"><picture><img alt="&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;L O N G&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;R E A D&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;" src="../../../../../_rsc/_img/signs/LongRead/blur_300px.jpg" /></picture></td>
   <td><b>P&thinsp;L&thinsp;E&thinsp;A&thinsp;S&thinsp;E&nbsp;&nbsp;S&thinsp;T&thinsp;A&thinsp;Y&thinsp;&nbsp;&nbsp;O&thinsp;N</b>&nbsp;&nbsp;⬇️</td></tr></table>

<table align="center"><tr></tr><tr><td><ins>&thinsp;
   The initial </ins><mark><b><code>O&thinsp;R</code></b></mark><ins>-question was answered first </ins><code><b>A&thinsp;N&thinsp;D</b></code><ins> and then refined to </ins><code><b>X&thinsp;O&thinsp;R</b></code><ins>
&thinsp;</ins></td></tr></table>

## Could I explain my shismatic take?

<details align="center"><summary><ins><b>&nbsp;This shadow of doubt was from the <samp>RISING</samp>&nbsp;&nbsp;R&thinsp;I&thinsp;D&thinsp;G&thinsp;E, dividing syntax and implementation behind it:&nbsp;</b></ins></summary>
&nbsp;

<div align="center"><picture><img src="../../../../../_rsc/_img/illus/tests/TddWatershed.jpg" alt="&nbsp;&nbsp;...Drawing: Test watershed illustration as nature..." /></picture></div>
<!-- pic --!>
<!--                                               WATERSHED CANVAS        --!>
<!-- pic --!>
</details>

Design vs. Development are too dissimilar and contradictory to rotate on the same axis even admitting [evolutionary phenomenon](https://en.wikipedia.org/wiki/Continuous_design)<sup><b>w</b></sup>. 
Even if it's the same project and team, test tools/framework, and skills/techniques to write tests and implement code behind.

<table><tr><td width="50%" align="center"><b>🧪 Test ⚙️ DESIGN</b> <mark><b>Δ</b></mark> </td><td align="center">🧪 <b>Test</b> ⚙️ <b>DEVELOPMENT</b> <mark><b>δ</b></mark></td></tr><tr>
   <td><p align="center"><samp><b>W&thinsp;H&thinsp;A&thinsp;T&nbsp;&nbsp;t&thinsp;o&nbsp;&nbsp;d&thinsp;e&thinsp;v&thinsp;e&thinsp;l&thinsp;o&thinsp;p</b></samp></p>
   </td><td><p align="center"><samp><b>H&thinsp;O&thinsp;W&nbsp;&nbsp;t&thinsp;o&nbsp;&nbsp;i&thinsp;m&thinsp;p&thinsp;l&thinsp;e&thinsp;m&thinsp;e&thinsp;n&thinsp;t</b></samp></td></td>
</tr><tr valign="top"><td>
   <ul>
      <li>grope concepts and get a hands-on feeling on subjects (all the same: bookkeeping artifacts or superhero <i>ViewModel</i>),</li>
      <li>vitalize skeleton functionality, evaluate trends and risks,</li>
      <li>couple design fantasies with the tech-stack materiality,</li>
      <li>evaluate and pick more suited libraries, frameworks, and, in some cases, languages/platforms,</li>
      <li>discuss ideas, naming, and logic with consultants and users.</li>
   </ul>
   </td><td>
   <ul>
      <li>provide design of classes</li>
     <li>granulate dev items and functions</li>
      <li>define failing scenarios</li>
      <li>fill design with working code and its alternatives</li>
      <li>layout the print of test coverage</li>
   </ul></td></tr>
   // QUALIFIER INTERFACES (which may have not effect) vs WORK IFACES !
      <!--              VOLATILE vs. STABLE      --!>
<tr></tr><tr valign="top"><td><p><b>Volatile</b></p>Design tests and code behind will inevitably come through approximations and changes.</td>
<td><p><b>Stabilizing</b></p>
   Implementation must be done on defined tasks./td></tr>
</td></tr><tr></tr><tr><td>Define general interfaces and back them with test doubles</td><td>Implement this interfaces</td></tr>
</td></tr><tr></tr><tr><td>
<p>Tests and the code behind them must intensively utilize doubles (mocks, dummies, stubs) and ugly but fast implementation shortcuts (possible in most languages). When procs get fixed contours and stabilize - these doubles may GRANULATE tasks for development: test-driven or not.</p>
</td><td>
   <p>Use of the test double must be limited to indispensable (stubbing a remote service or unavailable data) and diagnose helpers (as spies).</p>
</td></tr><tr></tr>
<tr valign="top"><td><p><b>Pass</b></p><p>Compilable syntax demos are enough.</p>
Non-compilable too to exclude wrong calls.
  <p>Tests can remain for a demo and serve as a documentation frame.</p></td>
<td><p><b>Checklist</b></p><p>Exact success and fail scenarios.</p></td></tr>
<tr><td align="center" colspan="2"><ins>&nbsp;<b>Is that so handy&thinsp;?</b>&nbsp;</ins></tr>
</table>
<!--                                             NOT SO EASY     --!>
<details align="center"><summary><ins>&nbsp;<b>Unfortunately <samp>NOT</samp></b>&nbsp;</ins></summary>
&nbsp;
   
<p align="center"><picture><img alt="&nbsp; Long ridge of high peaks (image credit: kyriosity)" src="../../../../../_rsc/_img/illus/tests/TddWatershed-altView.jpg"></picture></p>

<div align="center">An aerial photo of divergent ridges and contreforts would be a more precise picture but then I'd be the first to leave this narrative because of overcomplexity.</div>

We took the two extremes: API definition vs. coding.  nitty-gritty

\___________</details>

<h3 align="center">Is it so bad and idealistic? Neither!</h3>

<h2 id="TDD-ISie" align="center">Reconcile by example: TDD ⭐I&thinsp;S&thinsp;<samp>I&thinsp;E</samp>⭐</h2>

Let's take an [ISIe](https://github.com/Kyriosity/use-dev/tree/main/README%2B/parts/_ext/ISie) example

       🚧🐝🚧 .. WORK IN PROGRESS .. 🚧🐝🚧

```mermaid
gantt
title TDD ISie
    API:a, 0-07-20, 1w
        Not():a2, 0-07-20, 1w
    class struct :crit, b, 0-07-23, 1d
    ABC Check :active, c, after b a, 1d
    Circuitry   :d, 0-07-20, until b c
```


SPIN-OFFS: TESTS MULTIFEED

## Wrap up. Advantages

### Separation of duties

### Fast effective tasks and feedback.

\___________
 <div align="center">🔚 &nbsp;🌒 ...kyriosity, images 2024-2025...</div>
