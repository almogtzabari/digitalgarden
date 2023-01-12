---
{"dg-publish":true,"permalink":"/notes/instruction-set-architecture/","tags":[null]}
---



# Instruction Set Architecture
[[Notes/Instruction Set Architecture\|ISA]] is the instruction set that the architecture defines, and it is the lowest layer of abstraction that the user and the compiler sees. It is similar to API in the sense that it defines which API calls are available (=instructions) and the user doesn't care how it is implemented underneath.

## Considerations in ISA design
Since [[Notes/Instruction Set Architecture\|ISA]] is the interface of a processor with the external world, it is important to define it as best as we can.
Here are some considerations that we need to think of when defining an ISA:
- Instruction size
	- Long instructions take more time to fetch from memory
	- Long instructions require a larger memory (might be critical for embedded devices)
- Number of Instructions
	- Large amount of instructions means that we don't have to chain multiple instructions to achieve 1 complex instruction, which leads to reduce in runtime (assuming constant [[Notes/Cycles Per Instruction\|CPI]] and frequency).
- Simplicity
	- Cheaper hardware
	- Easier to optimize
	- Allowing high frequency and lower power consumption
