# WPF &nbsp;&mdash;&nbsp; from praxis &nbsp;&mdash;&nbsp; Hints

[![C#](https://custom-icon-badges.demolab.com/badge/WPF-keyboard_fresh-orangered.svg?logo=cshrp&logoColor=white&color=tomato)](#)

## Converters

+ A fast and easy alternative to converters is direct binding to `enum` properties, which will display the name of its numeric values.

## XAML

### _Divide et impera_ 

For new applications (or their parts), XAML may grow with the speed of bamboo (meter-long files during a day). 
Here, the "inversion of control" is vital: don't let XAML drive you, but prepare the structure (files) ahead to tame the bloating.

### Binding - backup values

Developers often neglect backup values<sup>🙋</sup> while they must be considered for every new `Binding`.

+ `FallbackValue` detects binding errors at both design and run time.\
`<TextBox Text="{Binding Title, FallbackValue=-n/a-}" />`

Similar `TargetNullValue` may confuse when the delay of the async set. Then it's reasonable to place any overlay when loading.

&nbsp;&nbsp;&nbsp;&nbsp;<sup>🙋</sup> Microsoft [doesn't teach](https://learn.microsoft.com/dotnet/desktop/wpf/data/binding-declarations-overview)<sup>🪟</sup> it from the very beginning as should.

\__________\
🔚 📝... TO BE CONTINUED ... 🚧
