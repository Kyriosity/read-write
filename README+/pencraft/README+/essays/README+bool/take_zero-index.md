# Zero index as false design decision &thinsp;&mdash;&thinsp; a&nbsp;Take

Puzzle: What's common for the UK and Germany with C++ and Java 
Hing: differs from Chile and Basic?
Answer: base index, 0 vs. 1



REAL BUG when cross-referencing language modules (e.g. C# to Java).

// NOTE: 0 is the default for Basic whlle can be changed


<table><tr><th width="50%">0-based</th><th width="50%">1-based</th></tr>
<tr><td colspan="2" align="center">int i = default</td></tr>
<tr><td>points to the first element, when the array may be of 0 size</td><td>points to no element</td></tr>
<tr><td>is first element </td></tr>
<tr><td>i == 0</td><td><code>i == 1</code></td></tr>
<tr><td colspan="2" align="center">is last elenent</td></tr>
<tr><td>i == count - 1</td><td><code>i == count</code></td></tr>
<tr><td colspan="2" align="center">is over bound</td></tr>
<tr><td>i > count - 1</td><td><code>i > count</code></td></tr>
</table>

BELOW LOWER BOUND ()

IS LAST INDEX

🚧 PLACEHOLDER 🚧

___________\
🔚 .. 2025 ..
