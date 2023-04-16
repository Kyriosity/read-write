# MVVM - Model & ViewModel cohesion

## Classic aggregation

As [Microsoft guidelines](https://docs.microsoft.com/en-us/archive/msdn-magazine/2009/february/patterns-wpf-apps-with-the-model-view-viewmodel-design-pattern) suggest ViewModels will usually aggregate Models in straightforward fashion:

<details>
  <summary><ins>&nbsp;Ordinary aggregation - sketch&nbsp;</ins></summary>
  
  ```csharp
  namespace Models;
  class Book
  {
      string Title { get; set; }
      // ........................................
  }
  ```
  ```csharp
  namespace ViewModels;
  class BookEditor : ViewModelBase
  {
     private Models.Book _model = // ... anyhow supplied or injected
     string Title {
        get => _model.Title;
        set { _model.Title = value; OnPropertyChanged(); }
     }
    // ........................................
  }
  ```
</details>

There's nothing foul in this practice but itchy call of "don't repeat yourself". Furthermore there're can be more ViewModels: *BookViewer* for display, *BookAbstract* for listing, *NewBook* for creation, - all multiplying the mere propagation of pretty much properties.

## Inheritance variant

|   |  |
| ------------- | ------------- |
| Let's regard model as a parent class, <br/>from which ViewModels can be derived:<br/><br/><br/><br/>| ![VModel cohesion diagram](../../_rsc/images/mvvm_vm-model-cohesion.jpg)  |

### Downcasting "impedance"

A cast of pure parent to inhereted classes/interfaces will cause ERROR in C# even when defaults would fit extensions (EXAMPLE).

... TO BE CONTINUED ...

### What about ViewModelBase

In the classic realization ViewModel will reasonably extend usually named `ViewModelBase` with common functionality, like notification. C# doesn't support multi-inheretance, and base is much more suitable for aggregation (injection) thus giving the way to model as parent. 

### Contraindications

The idea assumes that model classes are available for development or alteration. The keyword `sealed` will ABSOLUTELY dismiss the approach ... TO BE CONTINUED ...

## Alternatives

Seasoned framework and libraries provide their own _prêt-à-porter_ MVVM suites. 
