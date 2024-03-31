# WPF - Drawbacks

like Moon to the Earth.

Icos in upper Nav!

WPF is a stable, modern and so far popular platform, alive and well off despite some SAD prognoses.

It remains the number one choice for Windows applications.

HOWEVER 

however without pivotal improvements and new cutting-edge parts since its first releases.

## "WPF 2.0"

INSTEAD of Xamarin.

Since 2006 the wide use of WPF has accumulated tremendous expertise, feedback, change requests, and critical reports. Along with Microsoft resources, it's enough to release a breaking version of the subsystem - not seen hitherto in 2024.

## Templating

There's no state-of-the-art MVVM backbone from Microsoft that could spare much dev time and encourage teams to select this subsystem. Free first-class cliparts, galleries, and libraries of user controls are scattered if available at all.

PRJ-NEW
   STUDIO



## XAML

### Insufficient element IDs (names)

When a grid is big enough, any insert, delete, or move of a row or column will result in an adjustment of `Grid.Row=".."` or `Grid.Column=".."` in elements.

What if a grid definition could allow `<RowDefinition Id="Total"...` or `<ColumnDefinition Id="Tags"...` and one could set and forget `<Label Grid.Row="Total" Grid.Column="Tags">Total</Label>`.

### Bulky syntax

XML-based languages are bulky by their origin and XAML goes even further. Many names and constructs in XAML could drastically shrink but remain readable as in the following snippet.

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


## Converters

### UNDEV-D

link2 own

### Soft-pedalling of errors

Converters fail silently, covering errors or prompting you to keep the debugger open. The easiest workaround is to reserve a value or UI element ID to indicate errors.

🚧... details to be written ... 🚧

