---
{"dg-publish":true,"permalink":"/notes/branch-target-buffer/"}
---



# Branch Target Buffer
[[Notes/Branch Target Buffer\|Branch Target Buffer]] is some kind of small hardware located in the Fetch stage of a [[Notes/CPU Pipeline\|CPU Pipeline]], which is responsible for [[Notes/Branch Prediction\|Branch Prediction]].

## Goals
For each incoming instruction, the [[Notes/Branch Target Buffer\|BTB]] tries to answer:
1. Is it a branch instruction?
2. If yes, is the branch going to be TAKEN?
3. If yes, where is it going to jump to?

## Structure
The [[Notes/Branch Target Buffer\|BTB]] is usually composed of a table collecting statistics about the different branch instructions in the code. This table usually have the following columns:
- PC[^1]/IP[^2]/Tag[^3] - where is this instruction located in the code (memory)?
- TAKEN/NOT TAKEN - can sometimes be more that 1 bit, for example:
	- SNT - Strongly NOT TAKEN
	- NT - NOT TAKEN
	- T - TAKEN
	- ST - Strongly TAKEN
- Target - where do we jump (address)?
- History 
	- for example: T, T, T, T, NT, T, T, T, T, NT
	- The history can be per branch instruction (called local history), or 1 for all branches (called global history).
	- **For each history POSSIBILITY there is a different predictor**. For example, if we keep a global history (1 for all branches) of length 2 (keep last 2 [[Notes/Branch Resolution\|Branch Resolution]]s), and we use a 2 bit predictor (state machine of SNT, NT, T, ST), then we have $$1[history]\cdot 2[bits\_per\_history]\cdot 2^{2}[predictors]\cdot 2[bits\_per\_predictor]$$

[^1]: Program Counter - Address of the instruction.
[^2]: Similar to PC.
[^3]: Tag is some part of the original address, for example, only the first `x` bits.