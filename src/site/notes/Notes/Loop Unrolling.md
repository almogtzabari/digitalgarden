---
{"dg-publish":true,"dg-path":"Loop Unrolling.md","permalink":"/loop-unrolling/","tags":[null]}
---



# Loop Unrolling
[[Notes/Loop Unrolling\|Loop Unrolling]] is a [[Notes/Software\|software]] optimization step, usually done by the [[Notes/Compiler\|Compiler]] in order to improve performance.
The idea is to minimize the amount of branches in the code, which leads to less [[Notes/CPU Pipeline\|pipeline]] flushes.

![Pasted image 20221222180147.png](/img/user/Assets/Pasted%20image%2020221222180147.png)
{ #20ce37}


![Pasted image 20221222182603.png](/img/user/Assets/Pasted%20image%2020221222182603.png)
{ #3b5972}


## Pros
- Better performance because:
	- [[Notes/Instruction Count\|IC]] is smaller because there are less branch instructions
	- [[Notes/Cycles Per Instruction\|CPI]] is smaller because we'll have to flush the pipe less times
- Better power consumption because:
	- [[Notes/Instruction Count\|IC]] is smaller because there are less branch instructions, which leads to less "code" that needs to be executed and therefore less power.

## Cons
- Requires larger memory and larger [[Instruction Cache\|Instruction Cache]] because there are more instructions (`func(x); func(x+1); func(x+2); ...`)
- Requires more [[Register\|Register]]s
- Requires special treatment for edge cases, for example:
	- A case where the `For` loop [[Notes/Loop Unrolling#^20ce37\|above]] was to run until `98` (and not `100`)
	- A case where we the number of iterations is not known during compilation, as shown in [[Notes/Loop Unrolling#^3b5972\|this example]]. To overcome this we use a technique called [[Notes/Duffs Device Loop Unrolling Technique\|Duffs Device Loop Unrolling Technique]]