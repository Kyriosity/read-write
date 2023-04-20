# C# - Tasks as properties backup

Thinking in friendly UX it's good to apply deferred (aka lazy) initialization/calculation to less or more "heavy" entities. Either with C# `Lazy<>` or custom code like this:
<details>
  <summary><ins>Deferred loading snipped</ins></summary>
  
  ```csharp
public BigAndHeavy Ram => _ram ?? LoadAndHit();
private BigAndHeavy? _ram;
  ```
</details>

This allows to **a)**&nbsp;load the stuff on&nbsp;demand only, **b)**&nbsp;spread resources peaks, **c)**&nbsp;partition the suspense. However the suspense remains.

Any modern PC has enough power to process seamlessly in background.

## Tasks

🚧... TO BE CONTINUED ... 🚧
