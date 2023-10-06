# Drawbacks of WPF

WPF is a stable, modern and so far popular platform, alive and well off despite some prognoses. It remains the number one choice for Windows applications, however without pivotal improvements and new cutting-edge parts since its first releases.

## Converters

### Soft-pedalling of errors

Converters fail silently, covering errors or prompting you to keep the debugger open. The easiest workaround is to reserve a value or UI element ID to indicate errors.

🚧... details to be written ... 🚧

## XAML

### Insufficient element ids
When a grid is big enough, any insert, delete, or move of a row or column will result in an adjustment of `Grid.Row=".."` or `Grid.Column=".."` in elements.\
What if a grid definition could allow `<RowDefinition Id="Total"...` or `<ColumnDefinition Id="Tags"...` and you could set and forget `<Label Grid.Row="Total" Grid.Column="Tags">Total</Label>`.

### Bulky syntax
XML-based languages are bulky by their origin and XAML goes even further. Many names and constructs in XAML could drastically shrink without loss of readability as in the following snippet.

<details>
<summary><ins>&nbsp;</inst>Fictitious shortened XAML&nbsp;</ins></summary>

```XAML
<Grid>
   <Grid.Rows>
      <Row Height="Auto" />
      <Row Height="Auto" />
      <Row Height="Auto" />
   </Grid.Rows>
   <Grid.Cols>
      <Col Width="Auto"/>
      <Col Width="*"/>
   </Grid.Cols>
   <Label Grid="1,0">Ja</Label>
   ...
</Grid>
```
</details>

