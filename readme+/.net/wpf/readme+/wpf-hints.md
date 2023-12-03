# WPF - Hints from praxis

## Converters
A fast and easy alternative to converters is Binding to `enum` properties, which will display the name of its numeric value.

## XAML

### Binding backup values

`FallbackValue` is often forgotten but must be set as the easiest means to detect binding errors at both design and run time.\
`<TextBox Text="{Binding Title, FallbackValue=-n/a-}" />`

Similar `TargetNullValue` may be confused by the delay of async set. Then it's reasonable to place any overlay when loading.

📝... TO BE CONTINUED ... 🚧
