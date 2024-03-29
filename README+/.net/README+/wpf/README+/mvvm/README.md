# MVVM and WPF

Model-View-ViewModel (abbr. MVVM) is a well-accepted, easy, powerful concept of __separation of concerns__, also known as [MVP](https://martinfowler.com/eaaDev/uiArchs.html)<sup>🔗</sup>.

WinForms application can be an exemplary MVVM<sup>:wrench:</sup> but it was WPF that formed a symbiosis with MVVM and made the latter mainstream (and not only in WPF). Notably successful and stable Microsoft Visual Studio&nbsp;2010 was written from scratch in WPF relying on MVVM (Model-View-ViewModel).\
&nbsp;&nbsp;&nbsp;&nbsp;<sup>:wrench:</sup>&nbsp;<sub>In fact WPF is based on Winform's [Binding](https://learn.microsoft.com/en-us/dotnet/api/system.windows.forms.binding)<sup>🔗</sup></sub>

## Structure

|- __Model__  - usual [application model](../../../../../software/README+/design/parts/README+/app-model.md)\
|- [__ViewModel__](readme+/wpf_mvvm-viewmodel.md)\
|- [XAML view](../wpf-xaml_view.md) *

&nbsp;&nbsp;&nbsp;&nbsp;* It can also be any other kind of [application view](../../../../../software/README+/design/parts/README+/app-view.md) bound with the ViewModel

## Sample

An MVVM application may grow into an enterprise solution, but from the ground up its sketch claims a mere few minutes<sup>:arrow_down:</sup>

<details>
<summary><b><ins>&nbsp;Simplest MVVM application&nbsp;</ins></b></summary>
&nbsp;

![sketch of WPF app](../../../../../pencraft/README+/_rsc/_img/recipes/wpf-app_sketch.jpg)

<sup>:arrow_down:</sup>&nbsp;<sub>Project of Microsoft Visual Studio</sub>
</details>

## Drawbacks and lacks

Let's stress once again that MVVM is not a template but a concept. It got  WPF implementations from Microsoft (e.g. Prism), other big names, communities, and private initiatives but neither has achieved the status of industry-standard as UI suites.

Alas, there are not too many popular pluggable "bricks" to build custom WPF-MVVM, and there's no thesis on dynamic MVP resting on tasks - not static models.

🚧🚧🚧 PENDING: Link to MVVM on promises! 🖋️

## Wrapping up

MVVM has been widely established but is neither a golden nor universal section. On call of peculiarity or creativity any other, even monolithic, form is legal.&nbsp;<sup>:triangular_ruler:</sup>

&nbsp;&nbsp;&nbsp;&nbsp;<sup>:triangular_ruler:</sup><sub>&nbsp;Google team coined *Model-View-Whatever* for its Angular</sub>

You may find WPF-related design decisions here in [use-dev](https://github.com/Kyriosity/use-dev).

