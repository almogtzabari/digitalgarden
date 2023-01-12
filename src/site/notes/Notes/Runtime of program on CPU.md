---
{"dg-publish":true,"permalink":"/notes/runtime-of-program-on-cpu/","tags":[null]}
---



# Runtime of program on CPU
The runtime of a program that run on CPU is given by:
$$
CPU\_Time = IC\cdot CPI\cdot CT
$$
{ #accf4d}


Where:
- [[Notes/Instruction Count\|IC]] - how many instructions the program has
- [[Notes/Cycles Per Instruction\|CPI]] - how many cycles are required to run the average instruction
- **CT - Cycle Time** - how much time is spent on a cycle.

The units are:
$$
[Instructions]\cdot \frac{Cycles}{Instructions}\cdot \frac{Time}{Cycle} = [Time]
$$