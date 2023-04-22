# C# - Tasks as properties backup

Experienced developers used to defer initialization/calculation to less or more "heavy" entities. In C# either with `Lazy<>` or custom code like this:
<details>
  <summary><ins>Deferred loading snipped</ins></summary>
  
  ```csharp
public BigAndHeavy Ram => _ram ?? LoadAndHit();
private BigAndHeavy? _ram;
  ```
</details>

This allows to **a)**&nbsp;load the stuff on&nbsp;demand only, **b)**&nbsp;spread resources peaks, **c)**&nbsp;partition the suspense. However the suspense remains.

Powers of modern home laptops are mostly idle, while platforms like .NET allow accurately run multiple processes in background. Thus it's not important to delay tasks but prepare them as much as possible in background, and seamlessly produce, when required.

## Tasks

🚧... TO BE CONTINUED ... 🚧

## Beyond simple scenarios

🚧... TO BE WRITTEN ... 🚧
