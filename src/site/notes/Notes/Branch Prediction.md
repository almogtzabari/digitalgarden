---
{"dg-publish":true,"permalink":"/notes/branch-prediction/","tags":[null]}
---



# Branch Prediction
The goal of [[Notes/Branch Prediction\|Branch Prediction]] is to reduce the overhead caused by [[Notes/Control Hazard in CPU\|Control Hazard in CPU]] by predicting whether the code "jumps" and therefore predicting where to fetch the next instructions from.

There are several ways/techniques for [[Notes/Branch Prediction\|Branch Prediction]]:
- [[Notes/Branch Prediction#Static Prediction\|Static Precdiction]]
- [[Notes/Branch Prediction#Dynamic Prediction\| Dynamic Prediction]]
	- [[Notes/Branch Target Buffer\|BTB]]
	- Local / Global
- [[Notes/Branch Prediction#Delayed Branch\|Delayed Branch]]
	- Canceling branch


### Static Prediction
Static prediction means that **the [[Notes/Central Processing Unit\|Central Processing Unit]] always assumes that branch instructions are NOT TAKEN** and fetch the next instructions accordingly (chronological order). 
- Pros
	- If the branch is **NOT TAKEN** then we avoided overhead.
- Cons
	- If the branch was **TAKEN**, the [[Notes/Central Processing Unit\|Central Processing Unit]] will flush the [[Notes/CPU Pipeline\|Pipeline]] from the beginning all the way to the [[Notes/Branch Resolution\|Branch Resolution]]. This affects the performance and the power consumption.

### Dynamic Prediction
Dynamic prediction means that the [[Notes/Central Processing Unit\|Central Processing Unit]] "learns" (statistically) the branch instructions during runtime and decides whether to jump or not accordingly.
- Pros
	- Can achieve high prediction accuracy (around 90%+), which is usually much higher than [[Notes/Control Hazard in CPU#Static prediction\|Static prediction]].
	- If accurate, can save power.
- Cons
	- Requires extra logic.
	- Requires some power.

### Delayed Branch
Delayed branch means that we predefine in the hardware architecture (meaning the [[Notes/Compiler\|Compiler]] is aware of that) that every branch instruction must be followed by `n` amount of instructions **that need to be executed ANYWAY** (n-slots delayed branch).

If the [[Notes/Compiler\|Compiler]] cannot find an instruction that needs to be executed anyway, it will put a [[Notes/NOP in CPU\|NOP]].

The [[Notes/Compiler\|Compiler]] can choose the instructions:
- From before the branch instruction.
- From the target of the branch (from where we jump to).
	This is only possible if the instruction (that the compiler choose) does not affect the code flow in case we don't jump, meaning:
	- If we do jump - we execute this instruction anyway -> no problem.
	- If we don't jump - we (for example) modified R4, but R4 is not used in the part of the code without the jump -> no problem.
- From fall through (from where we continued as if the jump was NOT TAKEN). Again, the [[Notes/Compiler\|Compiler]] must bring an instruction that will not affect the flow if the branch was to be TAKEN.

![Pasted image 20221223091619.png](/img/user/Assets/Pasted%20image%2020221223091619.png)

- Pros
	- My thoughts: **There's no prediction here**, so as long as the [[Notes/Compiler\|Compiler]] able to find instructions that need to be executed anyway, we don't lose any performance/power.
- Cons
	- Makes the code **architecture dependent** because if we wish to run the code on another architecture where `m-slots delayed` is used (and not `n-slots delayed`) we have to recompile the code for that architecture (with a different [[Notes/Compiler\|Compiler]]).