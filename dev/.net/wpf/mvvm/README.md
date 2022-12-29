# MVVM and WPF

Model-View-ViewModel (abbr. MVVM) is a well accepted, easy, powerful concept of __separation of concerns__, also known as [MVP](https://martinfowler.com/eaaDev/uiArchs.html).

WinForms application can be an exemplary MVVM<sup>:wrench:</sup> but it was WPF that formed a symbiosis with MVVM and made the latter mainstream (and not only in WPF). Notably successful and stable Microsoft Visual Studio&nbsp;2010 was written from scratch in WPF relying on MVVM (Model-View-ViewModel).\
&nbsp;&nbsp;&nbsp;&nbsp;<sup>:wrench:</sup>&nbsp;<sub>In fact WPF is based on Winform's [Binding](https://learn.microsoft.com/en-us/dotnet/api/system.windows.forms.binding)</sub>

MVVM puts traditional and specific parts together:

|- __Model__  - usual [application model](../../../software-parts/app_model.md)\
|- [__ViewModel__](readme+/wpf_mvvm-viewmodel.md)\
|--- [Model-ViewModel cohesion](readme+/mvvm_vmodel-cohesion.md)\
|--- [Notification orchestration](readme+/mvvm_notification-orchestration.md)\
|- __View__     -  usual [application view](../../../software-parts/app_view.md) bound to ViewModel\
|--- [XAML view](../readme+/wpf_xaml.md)

## Wrapping Up

MVVM has been widely established, but is neither golden nor universal section. On call of specificity or creativity any other, even monolithic, form is legal.&nbsp;<sup>:triangular_ruler:</sup>\
&nbsp;&nbsp;&nbsp;&nbsp;<sup>:triangular_ruler:</sup><sub>&nbsp;Google team coined *Model-View-Whatever* for its Angular</sub>

An MVVM application may grow into an enterpise solution, but from the ground up its sketch requires few minutes&nbsp;<sup>:arrow_down:</sup>

![sketch](readme+/wpf_app-sketch.jpg)

<sup>:arrow_down:</sup>&nbsp;<sub>Project of Microsoft Visual Studio</sub>
