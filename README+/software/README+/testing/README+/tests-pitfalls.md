# Test coverage - Pitfalls

Bad tests are worse than none, and since you can't and shan't write tests of tests their development must be focused and flawless.

## Falsely green tests

<p dir="rtl">,Testing shows the presence<br/>.not the absence of bugs
<br/><i>:grey_question: Edsger W. Dijkstra</i>, 1969*?</p>


The worst case of malfunctioning tests is a passing one that indeed shields a fail. And the worst of the worst is when such fail/pass is sporadic and arduous to reproduce. That's like a crossroad with random green lights.

The following guidelines help to avoid:

+ Ever test your test to show the red sign.
+ Right anti-test counterpart (e.g. that shall throw exceptions)

## Blind fit to green and carousel

... 🚧  To DESCRIBE 🚧 ....

## Excess and overlap, formalism

Rules of a project may dictate 100% unit test coverage (at least one for an accessible member), and as a rule, this will formalize proofs. The formal test is a kind of `ASSERT 2+2 IS 2*2`<sup>:large_orange_diamond:</sup>.\
&nbsp;&nbsp;&nbsp;&nbsp;<sup>:large_orange_diamond:</sup>&nbsp;<sub>Please do not take verbatim. Such real tests may be justified for floating-point checks.</sub>

The overlap means that a text _x_ will never pass if there's a test _y_ that fails. 

## Ideal environment

The tests, which somehow concern performance, connections, proof of smoke, 

⏲️... TO BE CONTINUED ... 🚧
