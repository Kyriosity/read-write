# Test coverage - Pitfalls

NOTE: Test coverage notwithstanding whether it was written first or after the implementation it not a test 

## Conceptual

### Test coverage as design drive

 [TDD](../../design/tdd-ddd.md) 

### Tests of tests

Writing tests of test framework may put one into the infernal loop while running and analyzing applications tests will find out the errors there.

### Falsely green tests

<p dir="rtl">,Testing shows the presence<br/>.not the absence of bugs
<br/><i>Edsger W. Dijkstra</i>, 1969<sup>❔</sup></p>

The worst case of malfunctioning tests is a passing one that indeed shields a fail. And the worst is when such fail/pass is sporadic and arduous to reproduce - imagine a crossroad with the random switch of green lights.

The following guidelines help to avoid the trap:

+ Periodically "test" your test to show the red sign (not at the beginning only).
+ Add counterpart test with the opposite result (e.g. that shall throw exceptions)

### Red first illusion

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

Results from the URGE to make tests lists to specification and lack of organization.

`ValidateShouldReturnErrorWhenFirstNameIsNull()`

Would you admit such a name in the code? Why should it be in the test classes?

### Ideal environment

The tests, which somehow concern performance, connections, communication, proof of smoke, 

⏲️... TO BE CONTINUED ... 🚧
