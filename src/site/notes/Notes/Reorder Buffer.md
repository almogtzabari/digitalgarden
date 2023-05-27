---
{"dg-publish":true,"dg-path":"Reorder Buffer.md","permalink":"/reorder-buffer/","tags":[null]}
---



# Reorder Buffer
The [[Notes/Reorder Buffer\|Reorder Buffer]] is a hardware unit used in [[Notes/Out Of Order Execution\|Out Of Order Execution]], and can also be thought of as the physical registers.

The [[Notes/Reorder Buffer\|ROB]] is a cyclic buffer (FIFO queue) that each of its rows store:
- Instruction number
- Instruction - `add R2, R1, R1` for example
- Target register (architectonic register)
- Result (value)
- Status (yes/no/committed)

On *Decode* stage instructions are inserted into the [[Notes/Reorder Buffer\|ROB]],
after the *Execution* stage the result is written into the [[Notes/Reorder Buffer\|ROB]], and the instructions leave the [[Notes/Reorder Buffer\|ROB]] after they are committed.

![Pasted image 20230103162503.png](/img/user/Assets/Pasted%20image%2020230103162503.png)