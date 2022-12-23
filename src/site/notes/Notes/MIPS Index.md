---
{"dg-publish":true,"permalink":"/notes/mips-index/"}
---



# MIPS Index
MIPS, or Million Instructions Per Second given by:
$$
MIPS = \frac{IC}{CPUTime \cdot 10^6}
$$
Where:
- [[Notes/Instruction Count\|IC]] - how many instructions does the program has
- [[Notes/Runtime of program on CPU\|CPUTime]] - How much time it takes for the program to run

If we use 
<div class="transclusion internal-embed is-loaded"><div class="markdown-embed">






# Runtime of program on CPU
The runtime of a program that run on CPU is given by:
$
CPU\_Time = IC\cdot CPI\cdot CT
$

^accf4d

Where:
- [[Notes/Instruction Count\|IC]] - how many instructions the program has
- [[Notes/Cycles Per Instruction\|CPI]] - how many cycles are required to run the average instruction
- **CT - Cycle Time** - how much time is spent on a cycle.

The units are:
$
[Instructions]\cdot \frac{Cycles}{Instructions}\cdot \frac{Time}{Cycle} = [Time]
$

</div></div>
 we get:
$$
MIPS = \frac{IC}{IC\cdot CPI\cdot CT \cdot 10^6} = \frac{1}{CPI\cdot CT \cdot 10^6}
$$
$$
\Rightarrow \boxed{MIPS = \frac{1}{CPI\cdot CT\cdot 10^6}}
$$