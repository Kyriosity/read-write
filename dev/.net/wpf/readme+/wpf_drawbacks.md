# Drawbacks of WPF
WPF is a stable, modern and so far popular platform, alive and well off despite of some prognoses. It remains the number one choice for Windows applications, however without pivotal improvements and new cutting-edge parts since its first releases.

## XAML
### Insufficient element ids
When a grid is big enough, any insert, delete or move of a row or column will result in adjustment of `Grid.Row=".."` or `Grid.Column=".."` in elements.\
What if a grid definition could allow `<RowDefinition Id="Total"...` or `<ColumnDefinition Id="Tags"...` and you could set and forget `<Label Grid.Row="Total" Grid.Column="Tags">Total</Label>`.

### Bulky syntax
XML-based languages are bulky by their origin and XAML goes even further. The following dummy shows possible abbreviation.
<details>
  <summary>Fictitious shortened XAML</summary>

```XAML
<Grid>
   <Grid.Cols>
      <Col Width="Auto"/>
      <Col Width="*"/>
   </Grid.Cols>
   <Grid.Rows>
      <Row Height="Auto" />
      <Row Height="Auto" />
      <Row Height="Auto" />
   </Grid.Rows>
   <Label Grid>Ja</Label>
   ...
</Grid>
```
</details>

Overall much names and constucts in XAML could be drastically shortened without loss of readability.
