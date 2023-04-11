# Test coverage - pitfalls

Bad tests are worse than none, thus a good coverage shall be flawless.

## Falsely green tests

The worst case of bad tests is a passing one that indeed shields a fail. And the worst of the worst is when such fail/pass is sporadic and not easy reproducible.

An illustrative affinity is stuck green of traffic lights.

## Excess and overlap and , formalism

Rules of a project may dictate 100% unit test coverage (at least one for an accessible member), and as a rule this will formalise proofs. Figuratevely, formal test is a kind of `ASSERT 2+2 IS 2*2`<sup>:large_orange_diamond:</sup>.\
&nbsp;&nbsp;&nbsp;&nbsp;<sup>:large_orange_diamond:</sup>&nbsp;<sub>Please do not take verbatim. Such real tests may base floating point checks.</sub>

The overlap means that a text _x_ will never pass if there's a test _y_ that fails. 

⏲️... GOOD EXAMPLES PENDING ... 🚧
