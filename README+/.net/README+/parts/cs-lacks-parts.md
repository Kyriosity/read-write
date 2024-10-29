# C# - Nice to have - Parts and frameworks

Along with [nice-to-have syntax/features](../cs-lacks.md) **C#** could grow with some naturally expected parts/frameworks.

## Testing

Tests for drive or coverage are optional but natural share of development. The three most popular frameworks for .NET have their pros and contras but neither is in the state-of-the-art.

**See also**:\
|- [Testing on praxis](https://github.com/Kyriosity/use-dev/tree/main/README+/tests) ➡️(use-dev)

## Math

Native [`Math`](https://docs.microsoft.com/en-us/dotnet/api/system.math)<sup>🔗</sup> is pretty scarce, and 3d-party libraries aren't in the state of the art.

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

[AbcChrono](https://github.com/Kyriosity/use-dev/tree/main/src/TuttiFrutti/AbcChrono) in the _use-dev_ repo extends data handling to Bing Bang.

## Measurement systems

Definition of natural values (geometry, masses, temperature, electricity, movement u.a.) and their conversions between systems of measurements (metric, US customary, UK imperial u.a.) are more than essential tools (e.g., Celsius-Fahrenheit-Kelvin).

Meanwhile, you may try and extend [C# Multifaceted-Value](https://github.com/Kyriosity/use-dev/tree/6ab68c7af589d37715c171e61dc51d0b5a208c73/README+/projects/U-Val)<sup>➡️</sup> to organize units in your applications.

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
- linguistics goes far beyond competence in a few tongue families.

And what if .NET foundation classes could:
- neatly formulate declensions, conjugation, and other formations,
- define constants for unfamiliar forms of loanwords (greek, Latin u.a.),
- revise habitual [`CultureInfo`](https://docs.microsoft.com/en-us/dotnet/api/system.globalization.cultureinfo) (classify tongue families and default agreements)

And, not least, add syntax sugar like

<details>
<summary><b>Proposal for grammar interpolation</b></summary>
&nbsp;&nbsp;`${number [: [format] : [forms] : []] }`, where

&nbsp;&nbsp;&nbsp;&nbsp;*number* is whole or fractional subject\
&nbsp;&nbsp;&nbsp;&nbsp;*format* specifies usual format or to put in words\
&nbsp;&nbsp;&nbsp;&nbsp;*forms* - grammar forms as in imaginary `INumbered` in the snippet above

</details>

\___________\
🔚
