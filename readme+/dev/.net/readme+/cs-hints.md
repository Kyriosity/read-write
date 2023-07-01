# C# - Derived from praxis

## Syntactic

<details>
<summary><ins>Negate with <i>exclusive or</i></ins></summary>
  
```diff csharp
-      isLoading = !isLoading // open for typos with other var
+      isLoading ^= true; // explicit inversion
+      isLoading = !offLoading // explicitly other var
```

```diff csharp
// Invert a longish chained property in legacy API:
-    Controller_A.CPU2.Circuits.TriggerY1.Input.S_plus = !Controller_A.CPU2.Circuits.TriggerV1.Input.S_plus;
// Have you noticed a typo, which I inserted on purpose, and which can still designate a valid prop
+    Controller_A.CPU2.Circuits.TriggerY1.Input.S_plus ^= true; // terser and "typo"-safe 
```

</details>

<details>
<summary><ins>Argument</ins> <code>out</code> <ins>for readability</ins></summary>

```csharp
if (!PauseOver(out var remaining))
   _worker.Sleep(remaining);
```

</details>

<details>
<summary><ins>Discard with underscore</ins></summary>

```csharp
 // Remove visual noise of nominal arguments
  void OnMouseMove(object _, EventArgs __) { MyApp.Unfreeze(); };
// explicitly tells that signature parameters aren't used
```

 ```csharp
 // to point that return value isn't required or a method/constructor is called for side-effect only
 _ = myShoppingCart.Pay(); // habitually i don't care for receipt returned 
 _ = new ResourceBlocker(filename); // stub objects (e.g. to invoke and prove constructor logic only) 
```
  
+ But not always the best choice
  
```csharp
// null guard with *null-coalescing* ...
_ = myOrder?? throw new ArgumentNullException(nameof(myOrder)); 
// ... has a readable and shorter way
ArgumentNullException.ThrowIfNull(myOrder);
```
  
+ Not a discard but pleasing

```csharp
const int milesToMars_CloseApproach = 38_600_000;
var rfidTagFilter = 0b_0111_1100_0100_0011;
```

</details>

<details>
<summary><ins>Name "magic" constants</ins></summary>
  
Making a "magic value" to constants or predefined values doesn't clean the code unless named good.   
  
```diff csharp
-     legacySystem.ModuleD1.Abracadabra = true; // specifies that text input is treated as case-sensitive
+     const bool InputIsCaseSensitive = true;
+     legacySystem.ModuleD1.Abracadabra = InputIsCaseSensitive;
```
```diff csharp
-     const int popupDuration = 3200;
-     Info(shortMessage).Popup(popupDuration); 
+     Info(shortMessage).Popup(Ux.MinToNoticePrompt.Milliseconds);
```
</details>

&nbsp;
## Gimmicks

<details>
<summary><ins>Benchmark/profile with</ins> <code>using</code></summary>

```csharp
using (var benchmark = new Benchmark()) {
    // benchmarked flow here
}

class Benchmark : IDisposable
{
   string _caller;

   public Benchmark([CallerMemberName] string caller = "<undefined>") {
      _caller = caller;
      // Start logging/profiling
   }    

   public void Dispose() {
      // stop logging/profiling
   }
}
```
</details>

&nbsp;
## Organization of entities

<details>
<summary><ins>Named tuples as design shortcuts</ins></summary>

Piles of interfaces, classes, and structs for every single trifle may obscure the contours of OOD. Then _named tuples_ are a sound compromise, when limited to sparse occasions.

```csharp
...
(int width, int depth, int height, DateTime availableFrom) FindMinPackageBox(Product[] products);
...
if (storehouse.FindMinPackage(goods).availableFrom < DateTime.Today.AddDays(3)) {
    goods.PremiumSupply = true;
... 
```

Further use is to streamline assignments:

```csharp
// Given a chess game log ...
 chessGame.Move = "c5";
// .. you'd like to annotate moves 
chessGame.Move = ("c5", "Sicilian Defence");
// that is backed with
(string notation, string comment) Move { get; set; }
```

Unrestricted tuples, named or not, will be great helpers for prototyping code contracts until they will solidify into interfaces and definitions.
</details>

<details>
<summary><ins>Distinct default of enums</ins></summary>

Reserve, when appropriate, _none_, _undefined_ or _unknown_ as zero-value to prevent unexpected default assignment and consequent bugs.
```csharp
enum FundamentalStatesOfMatter
{
    Unknown, // implicitly = 0,
    Solid, // won't be assigned by default e.g. to a motor coolant
    Liquid,
    Gas,
    Plasma
}
```

</details>

&nbsp;
## Subsystems

+ WPF ...\
| - [WPF hints](../wpf/readme+/wpf-hints.md)
