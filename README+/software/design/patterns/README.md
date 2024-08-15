# Code - Patterns

The original vision of  *patterns* as code constructs has spread over software templates, project solutions, methodologies, and even developer's manners, but let's stay on its initial meaning.

As the growth of instruction sets of processors resulted in abstractions clever programmers noticed useful patterns of code to repeat and recommend. 
In the 1970s-1990s they were augmented, systematized, and popularized - the most admitted of them became dogmatic and featured in languages/frameworks.

:construction: ... TO BE CONTINUED with samples ...:pencil2:

## Pitfalls

### "Patterns-in-themselves"

Fitting the code to an appealing pattern is like inventing a sentence for a buzzword. This also refers to overuse, for example, when _Builders_ cover trivial `Create()`/`New()`.

### Pattern as anti-pattern

Unsuitable context may negate any pattern. Specimens? 

- Doubtful _singleton_ in Java or C# where injection is an option: `void ProvePeriphery(ILog sharedLog);`
- any `Lazy<...>` loading that could be done in the background

### Naming

Custom/personal (nick)names for established patterns aren't a good practice unless it's a breakthrough idea.

## Conclusion

Keen developers will intuitively follow design patterns even if they are unaware of them. However, learning is essential to know recent and use proper names and signatures.

**Going further:**\
|- Design principles and methodlogies\
|--- [reviewed SOLID](../../../pencraft/README+/opuses/contraSOLID.md) 🚧
