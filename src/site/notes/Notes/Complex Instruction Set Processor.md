---
{"dg-publish":true,"permalink":"/notes/complex-instruction-set-processor/"}
---



# Complex Instruction Set Processor
[[Notes/Complex Instruction Set Processor\|Complex Instruction Set Processor]], also known CISC, means that the [[Notes/Instruction Set Architecture\|ISA]] is large and supports many instructions, some of these instructions are complex.
The idea is to allow a higher level machine language - [[Assembly\|Assembly]] programmers' job will be easier.
An example for a CISC is Intel's x86.

## Characteristics
- Many instruction types, many addressing modes
- Some instructions are complex (and require more cycles)
- ALU operations directly on memory
- Variable length instructions - frequent instructions get shorter op-code, which in turn saves memory

## Drawbacks
- Complex instructions and addressing modes
	- Complicates the processor.
	- Slows down the simple, common instructions.
	- Contradicts "Make The Common Case Fast" because it turns out that most frequent instructions are the simple ones.
- Variable length instructions are problematic
	- Difficult to decode in parallel because we don't know where an instruction ends until we decode the instruction.
