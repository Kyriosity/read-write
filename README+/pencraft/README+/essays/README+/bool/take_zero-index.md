# Zero index as a bad choice &thinsp;&mdash;&thinsp; a&nbsp;Take

<div align="right">Puzzle: What's common for <i>Paris</i>, <i>Australia</i>, <code>C++</code>, and Java❔</div>
<div align="right">Hint: differs from Chile, FOTRAN, Basic, and Common Era</div>
<div align="right">Answer: base number of floors, arrays, and years.</div>



REAL BUG when cross-referencing language modules (e.g. C# to Basic).

// NOTE: 0 is the default for Basic while can be changed

<table><tr><th width="50%">0️⃣-based</th><th width="50%">1️⃣-based</th></tr>
<tr><td colspan="2" align="center">int i = default</td></tr>
<tr><td>points to the first element, when the array may be of 0 size</td><td>points to no element</td></tr>
<tr><td colspan="2" align="center">is first element </td></tr>
<tr><td>i == 0</td><td><code>i == 1</code></td></tr>
<tr><td colspan="2" align="center">is last elenent</td></tr>
<tr><td>i == count - 1</td><td><code>i == count</code></td></tr>
<tr><td colspan="2" align="center">is in upper bound</td></tr>
<tr><td>i < count</td><td><code><b>i</b> =< count</code></td></tr>
<tr><td colspan="2" align="center">is over bound</td></tr>
<tr><td>i > count - 1</td><td><code>i > count</code></td></tr>
</table>

🚧 PLACEHOLDER 🚧

___________\
🔚 .. 2025 ..
