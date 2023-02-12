---
{"dg-publish":true,"permalink":"/notes/register-renaming/","tags":[null]}
---



# Register Renaming
[[Notes/Register Renaming\|Register Renaming]] is a technique to overcome [[Notes/Data Hazard in CPU\|false and anti dependencies]] resulting from [[Notes/Out Of Order Execution\|Out Of Order Execution]].

The idea is to keep 2 sets of registers:
1. Architectural Registers - This is what the programmer/compiler is exposed to.
2. Physical Registers - A large pool of physical registers available for the micro-architecture.

In addition to those sets, we also keep a bi-directional mapping between those sets, which is updated between the *Decode* and *Execute* stages.

## How Does It Work?
- [[Notes/Architected Register File\|Architected Register File]] holds pointers to [[Notes/Physical Register File\|Physical Register File]] registers.
- Each register in the [[Notes/Architected Register File\|ARF]] is holding a pointer to the register in the [[Notes/Physical Register File\|PRF]] that has the latest version of the data.
- Whenever an instruction writes to a register, a [[Notes/Register Renaming\|Register Renaming]] is triggered:
	- Allocate new [[Notes/Physical Register File\|PRF]] register.
	- Update pointer in [[Notes/Architected Register File\|ARF]].

![Pasted image 20230105111305.png](/img/user/Assets/Pasted%20image%2020230105111305.png)