# Code - Patterns

The famed vision of code constructs as [Design Patterns](https://en.wikipedia.org/wiki/Design_Patterns)<sup>🔗</sup> has spread over software templates, project solutions, methodologies, and even developers' manners, but let's stay on its initial meaning.

As the growth of hardware instruction sets pushed abstractions to the next level, clever programmers spotted useful code patterns to follow and recommend. 
In the 1970s-1990s they were augmented, systematized, and popularized - the most admitted of them became dogmatic and featured in languages/frameworks.

:construction: ... TO BE CONTINUED with samples ...:pencil2:

## Pitfalls

### "Patterns-for-themselves"

Coercing the code to an appealing pattern is like inventing a sentence for a buzzword. 

#### Complicating

This also refers to overuse when, for example,  _Builders_ cover trivial constructors or their  `Create()`/`New()`.

### Pattern as anti-pattern

Unsuitable context may negate any pattern. Specimens? 

- Doubtful _singleton_ in Java or C# where injection is an escape: `void ProvePeriphery(ILog sharedLog);`
- any `Lazy<...>` loading that could be done async

### Naming

Custom/personal (nick)names for established patterns aren't a good way unless it's a breakthrough idea or a remarkable workaround.

## Conclusion

Keen developers will intuitively follow design patterns even if they are unaware of them. However, learning is essential to know recent and use proper names and signatures.

**Going further:**\
|- [**Patterns realization**](https://github.com/Kyriosity/use-dev/tree/main/README+/patterns) ➡️ (_use-dev_)

|- Design principles and methodlogies\
|--- [reviewed SOLID](../../../pencraft/README+/essays/README+/contraSOLID.md) 🚧
