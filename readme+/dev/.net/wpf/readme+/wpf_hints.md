# Ideas from WPF praxis

## Converters
Fast and easy alternative to converters is Binding to `enum` properties, which will display a name of its short value 

## XAML

### Binding backup values

`FallbackValue` is often forgotten but must be set as the easiest mean to detect binding errors at both design and run time.\
`<TextBox Text="{Binding Title, FallbackValue=-n/a-}" />`

Similar `TargetNullValue` may confuse by delay of async set. Then it's resoanble to place any overlay, when loading.

📝... TO BE CONTINUED ... 🚧
