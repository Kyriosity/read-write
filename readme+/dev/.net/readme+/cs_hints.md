# Ideas from C# praxis

## Coding hints

<details>
<summary><b>Negate with <i>exclusive or</i></b></summary>
  
```diff csharp
-      isLoading = !isLoading
+      isLoading ^= true; // explicit
```

```diff csharp
// invert a longish chained property in legacy API:
-    Controller_A.CPU2.Circuits.TriggerY1.Input.S_plus = !Controller_A.CPU2.Circuits.TriggerV1.Input.S_plus;
// i'd intentionally done a typo, which you could have missed and which can still designate a valid name
+    Controller_A.CPU2.Circuits.TriggerY1.Input.S_plus ^= true; // terser and "typo"-safe 
```

</details>

<details>
<summary><b>Argument</b> <code>out</code> <b>for readability</b></summary>

```csharp
if (!CheckPauseComplete(out var msRemaining))
   _module.Sleep(msRemaining);
```

</details>

<details>
<summary><b>Discard with underscore</b></summary>

```csharp
// null guard with *null-coalescing* 
_ = order?? throw new ArgumentNullException(nameof(order)); // though `if()` is more readable 
```

```csharp
 // remove visual noise of nominal arguments
  void OnMouseMove(sender _, EventArgs __) { MyApp.Unfreeze(); };
```

 ```csharp
 // to point that return value isn't required or a method is called for side-effect only
 _ = myShoppingCart.Pay(); // habitually i don't care for receipt
 ```

  ```csharp
 // mock objects (e.g. to invoke constructor logic only) 
  _ = new ResourceBlocker(filename);
   ```

+ Not a discard but pleasing

```csharp
const int milesToMars_CloseApproach = 38_600_000;
var rfidTagFilter = 0b_0111_1100_0100_0011;
```

</details>

<details>
<summary><b>Benchmark/profile easy with</b> <code>using</code></summary>

```csharp
using (var benchmark = new Benchmark()) {
    // benchmarked flow here
}

class Benchmark : IDisposable
{
   string _caller;

   public Benchmark([CallerMemberName] string caller = "<undefined>") {
      _caller = caller;
      // start logging/profiling
   }    

   public void Dispose() {
      // stop logging/profiling
   }
}
```
</details>

<details>
<summary><code>nameof</code>&nbsp;<b>is good, but</b> <code>CallerMemberName</code>&nbsp;<b>may be better</b></summary>  
The snippet above (benchmark `using`) must have decently clarified this. It's tempting to copy `nameof()` from another call and forget to alter.

</details>

<details>
<summary><b>Name "magic" assignments</b></summary>
  
```diff csharp
-     legacySystem.ModuleD1.Abracadabra = true; // specifies that text input is treated case-sensitive
+     const bool InputIsCaseSensitive = true;
+     legacySystem.ModuleD1.Abracadabra = InputIsCaseSensitive;
```
```diff csharp
-     Info(shortMessage).Popup(3200);
+     Info(shortMessage).Popup(Ux.MinToNoticePrompt.Milliseconds);
```
</details>

## Organization of entities
<details>
<summary><b>Named tuples as design shortcuts</b></summary>

Piles of interfaces, classes and structs for every single trifle may obscure contours of OOD. Then _named tuples_ are a sound compromise, when limited to SPARSE cases.

```csharp
...
(int width, int depth, int height, DateTime availableFrom) FindMinPackageBox(Product[] products);
...
if (storehouse.FindMinPackage(ERSATzSupply).availableFrom > DateTime.Today.AddDays(7)) {
... 
```

This shortcut can further cut initialization and streamline assignments:

```csharp
// given a chess game log ...
 chessGame.Move = "c5";
// you'd love to briefly annotate moves 
chessGame.Move = ("c5", "Sicilian Defence");
// that is backed with
(string notation, string comment) Move { get; set; }
```

Unrestricted tuples, named or not, will be great helpers for prototyping code contracts, until they will solidify to interfaces and definitions.
</details>

<details>
<summary><b>Default values in enum</b></summary>

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

## Going further...
+ [Cheatsheet](cs_cheatsheet.md)
+ Technologies\
| --- [Ideas from WPF praxis](../wpf/readme+/wpf_hints.md)
