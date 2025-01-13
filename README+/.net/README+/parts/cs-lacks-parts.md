# C# &mdash; Nice to have &mdash; Parts and frameworks

Along with [nice-to-have syntax/features](../cs-lacks.md) there are some bigger blocks of ideal C#.

## Testing

Tests for drive or coverage are optional but a natural part of development. The three most popular frameworks for .NET (NUnit, xUnit, MSTest) have pros and cons, but neither is state-of-the-art.

Besides weak points (like bulky names), there are lacks:
- no way to auto-test code that must not compile (e.g. to exclude the wrong branches of building calls),
// EXAMPLE in USE-DEV
- no support of dynamic test data,
- no gradual asserts ➡️ [discussion of workaround](https://github.com/Kyriosity/use-dev/tree/main/README+/tests/README+/unit_test-gradual_assert.md),
- only a single data source ➡️ [multi-feed workaround](https://github.com/Kyriosity/use-dev/tree/main/README+/tests/README+/prog_tests-cut_feeds.md).

## Math

Native [`Math`](https://docs.microsoft.com/en-us/dotnet/api/system.math)<sup>🪟</sup> is pretty scarce, and neither 3d-party library is modern or all-around.

<b>C#</b> would only profit from a lightweight assembly that could: 

+ inventory more [constants](https://en.wikipedia.org/wiki/Mathematical_constant)<sup><b>w</b></sup>,
+ provide more useful functions (there are myriads uncovered),
+ approximate popular irrational values like π (Pi) to the requested length,
+ generate and check numbers in [sequences](http://oeis.org/wiki/Welcome)<sup>🔗</sup> (`bool Prime.Has(ulong num)`), detect sequences,
+ introduce complex numbers,
+ parallelize, async heavy algorithms with progress report and cancellation option

## Dates

Rudimentary `DateTime` and `DateOnly` are not intuitive (e.g. `new DateTime(1999, 9, 1, 9, 5, 6, 7)`), rather constrained (e.g. no BCE years), and inflexible. 
Built-in calendars render limited expansion.

➡️ [AbcChrono](https://github.com/Kyriosity/use-dev/tree/main/README+/parts/AbcChrono) in the _use-dev_ repo extends data handling (e.g. to origin from Bing Bang).

## Measurement systems

Definition of natural values (geometry, masses, temperature, electricity, movement u.a.) and their conversions between systems of measurements (metric, US customary, UK imperial u.a.) are more than essential tools (e.g., Celsius-Fahrenheit-Kelvin).

The approach for such is proposed in [C# Multifaceted-Value](https://github.com/Kyriosity/use-dev/tree/6ab68c7af589d37715c171e61dc51d0b5a208c73/README+/projects/U-Val)<sup>➡️</sup>.

## Lingua

Let's take some output from fictitious tree search `$"Branches: {found}, ≥ leaves: {cutoff}"`. That can be quickly refactored for narrative or voice generator:\
`$"{found} {(1 == found ? "branch has" : "branches have")} no less than {cutoff} {(1 == cutoff ? "leaf" : "leaves")}"`

If an application generates much multi-language text it won't be a big deal to implement

<details>
<summary><ins>&nbsp;Blueprint of pluralization utility&nbsp;</ins></summary>

```csharp
namespace Lingua.Grammar;

interface INumbered
{
    string Count(long num);
    string Count(double num);
}

interface IPluralForms {
    INumbered Plural((string singular, string plural) forms, string culture = "");
    INumbered Dual((string singular, string dual, string plural) forms, string culture = "");
    INumbered Trial((string singular, string dual, string trial, string plural) forms, string culture = "");
    INumbered Paucal((string singular, string paucal, string plural) forms, string culture = "");
    INumbered Custom(string[] forms, Func<long, int> indexWhole, Func<double, int>? indexFractional = null);
}
```

</details>

However
- this reinvents the wheel,
- there are other forms of grammatical numbers besides plurals,
- numbering is only a share of grammatical agreements in every single tongue,
- linguistics requires competence in more than in a pair of language families.

And what if .NET foundation classes could:
- neatly formulate declensions, conjugation, and other formations,
- define constants for unfamiliar forms of loanwords (greek, Latin u.a.),
- revise habitual [`CultureInfo`](https://docs.microsoft.com/en-us/dotnet/api/system.globalization.cultureinfo) (classify tongue families and default agreements)

And, not least, add syntax sugar like

<details>
<summary><ins>&nbsp;<b>Proposal for grammar interpolation</b>&nbsp;</ins></summary>
&nbsp;

&nbsp;&nbsp;`${number [: [format] : [forms] : []] }`, where

&nbsp;&nbsp;&nbsp;&nbsp;*number* is whole or fractional subject\
&nbsp;&nbsp;&nbsp;&nbsp;*format* specifies usual format or to put in words\
&nbsp;&nbsp;&nbsp;&nbsp;*forms* - grammar forms as in imaginary `INumbered` in the snippet above

\___________</details>

🔚 🌔 .. 2025
