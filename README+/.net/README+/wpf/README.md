# WPF - Reminder

Despite much scepsis, justifiable and not, and critics from the very dawn **WPF** became a fully mature successor of _WinForms_, unlike its Web companion _manqué_ - Silverlight, and cross-platform offshots (like Xamarin).

 **WPF** is the number one platform for Windows desktops with millions of commercial and enterprise applications, released and being developed.<sup>🙋</sup>
 
 Thus, WPF to .NET/Win is like The Moon to Earth - the only natural and permanent satellite. Alternatives are either petit, marginal, exotic, still immature, or already deprecated<sup>🌘</sup>.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<sup>🙋</sup> <sub>Enjoying a definite ebb in cross-platform demand</sub>\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<sup>🌘</sup> <sub>You may have heard about [Avalonia XPF](https://avaloniaui.net/XPF)<sup>🔗</sup>, Xamarin, WinUI, or [Blazor](https://learn.microsoft.com/aspnet/core/blazor/hybrid/tutorials/wpf)<sup>🔗</sup> (the latter may change the dev landscape but it's too early too predict in 2024).</sub>

For developers **WPF**:

+ is "native" to Windows (64-bit memory addressing, multitasking, and direct hardware acceleration since Windows&nbsp;7),
+ is backed by Microsoft and .NET devoted experts, dependent on its stability and progress,
+ provides full stack dev on .NET (+MS&nbsp;SQL) without the mix of platforms (and involvement of their providers), languages, and tools with differing paradigms<sup>☕</sup>,
+ implies [MVVM](https://learn.microsoft.com/en-us/dotnet/architecture/maui/mvvm)<sup>:link:</sup> and has promoted it to other platforms,
+ and grants true **RADD** (Rapid Application Development and Deployment).

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<sup>☕</sup> <sub>Compare to Java/Javascript/Typescript stacks with disputes on frontend framework and backend DB.</sub>

## Rapid Development and Deployment with WPF

The learning curve of WPF is distinctly steeper and concepts to learn are much broader than that of WinForms. 
Nonetheless, a WPF newbie<sup>🔰</sup> entering either a new or established project has the luck to delay advanced topics till less stressful times. 

&nbsp;&nbsp;&nbsp;&nbsp;<sup>🔰</sup> <sup>But experienced in .NET and thinking in patterns.</sup>

True **RAD**, which also refers to the dev environment/tools, sketching, running, creation of tests, and deployment,

### Initiatives

The best way to learn WPF is to build a basic MVVM application on a green field: proof of concept, prototype, or initial commit. 
Even better is to take a renowned freeware template, learn it, and build the application on it.

### Large projects

If the application is a ripe WPF product, its components will be a huge construction set, pieces of which a novice may soon manipulate with declarative tools. 

For example, take a pro table component from a gallery, declare it in a view, back it with the model data, and adorn it with custom logic in ViewModel.

### Deployment

Installation and update of the WPF application either as a prototype, test, or release could be as easy as unpacking an archived folder. 
A kind of container that will work "not only on my machine" without DevOps.

---

__Further notes__:\
|- [WPF and MVVM](README+/mvvm/)\
|- [WPF lacks](README+/wpf-drawbacks.md)\
|- [WPF hints](README+/wpf-hints.md)\
|- [XAML view](README+/wpf-xaml_view.md)

__Resources__:\
|- [Awesome WPF](https://github.com/Carlos487/awesome-wpf)<sup>🔗</sup> - big collection of links about literally everything that may concern WPF developers\
|- [Prism](https://github.com/PrismLibrary/Prism)<sup>🔗</sup> - reputable representative of WPF/MVVM bootstrapping 
