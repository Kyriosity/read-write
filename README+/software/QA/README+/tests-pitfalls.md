........... 🚧🐝🚧 ... WORK in PROGRESS... 🚧✏️🚧

# Software testing &mdash; Pitfalls 

<p dir=rtl>Testers hate it when<br />.developers know these catches<br/>(Clickbait🪝)</p>

## Conceptual

### Tests of tests

Writing tests of test frameworks may put one into the infernal loop while running and analyzing application tests, which will find the errors there.

### Falsely green tests

The worst case of malfunctioning tests is a passing one that indeed shields a fail. And the worst of the worst is when such fail-pass is sporadic and arduous to reproduce - imagine a crossroad with the random switch of green lights.

The following guidelines help to avoid the trap:

+ Periodically break and then check vital tests to show the red sign.
+ Add counterpart test with the opposite result (e.g. that shall throw exceptions)

### TDD tribute

Procedures _Test Driven Development_ can serve in coverage - not practices.

<table><tr></tr><tr align="center"><td width="30%">⚙️&thinsp;<b>TDD</b></td><td>Proof coverage</td>
  </tr><tr valign="top"><td>
  <p>🔴&thinsp;Red</p>
  <p>🟢&thinsp;Green</p>
  <p>🟡&thinsp;Refactor</p>
</td><td>
  Write something, make it pass, and improve is the antipattern for coverage. Critical parts of the code must be thoroughly covered with both positive and negative ("inverted") asserts.
</td></tr></table>

### One-to-one with DRIVER (not DATA)

LINK to use-dev

## Practical

### Formalism


### Direct reference to implementation

Contrary to TDD unit tests. Providers as adapters. // WRITE FOR TDD !

### Blind fit to green and carousel

Woodoo fix\
... 🚧  To DESCRIBE 🚧 ....

### Excess and overlap

Rules of a project may dictate 100% unit test coverage (at least one for an accessible member), and as a rule, this will formalize proofs. The formal test is a kind of `ASSERT 2+2 IS 2*2`<sup>:large_orange_diamond:</sup>.\
&nbsp;&nbsp;&nbsp;&nbsp;<sup>:large_orange_diamond:</sup>&nbsp;<sub>Please do not take verbatim. Such tests may be justified for floating-point checks.</sub>

The overlap means that a text _x_ will never pass if there's a test _y_ that fails. 

### Extra-long naming

Results from the URGE to make tests lists to specification and come short of organization.

`ValidateShouldReturnErrorWhenFirstNameIsNull()`

Would you admit such a name in the code? Why should it be in the test classes?

### Ideal environment

The tests, which somehow concern performance, connections, communication, proof of smoke, 

⏲️... TO BE CONTINUED ... 🚧
