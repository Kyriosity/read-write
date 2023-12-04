# Test coverage - pitfalls

Bad tests are worse than none, thus good coverage shall be flawless.

## Falsely green tests

The worst case of bad tests is a passing one that indeed shields a fail. And the worst of the worst is when such fail/pass is sporadic and arduous to reproduce.

 Stuck in green traffic lights is an illustrative affinity.

## Excess and overlap, formalism

Rules of a project may dictate 100% unit test coverage (at least one for an accessible member), and as a rule, this will formalize proofs. The formal test is a kind of `ASSERT 2+2 IS 2*2`<sup>:large_orange_diamond:</sup>.\
&nbsp;&nbsp;&nbsp;&nbsp;<sup>:large_orange_diamond:</sup>&nbsp;<sub>Please do not take verbatim. Such real tests may be justified for floating-point checks.</sub>

The overlap means that a text _x_ will never pass if there's a test _y_ that fails. 

⏲️... TO BE CONTINUED ... 🚧
