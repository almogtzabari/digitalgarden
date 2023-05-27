---
{"dg-publish":true,"dg-path":"Data Hazard in CPU.md","permalink":"/data-hazard-in-cpu/","tags":[null]}
---




# Data Hazard in CPU
Data hazard is a type of [[Notes/Pipeline Hazards in CPU\|Pipeline Hazards in CPU]] that occur due to dependencies of data between two or more instructions.

There are 3 main types of data hazards:
- **R**ead **A**fter **W**rite - Occurs when an instruction consumes data that was produced by earlier instruction. this is a *True-dependency* because we have to read the right data (after it is modified).
{ #af4605}

- **W**rite **A**fter **R**ead - also called *Anti-dependency* (called like this because it's the opposite of **RAW**). This can easily be resolved using [[Notes/Register Renaming\|Register Renaming]].
- **W**rite **A**fter **W**rite - also called *False-dependency*.

To overcome some of these we can either:
1. Stall - Let the hardware detect hazard and add stalls if needed. The problem with that is that it is SLOW. To overcome that we use *Forward*.
2. Forward - have a bypass fetching the relevant data to the desired [[Notes/CPU Pipeline\|pipeline]] stage. 
   Problems:
	   - Need to add extra logic ([[Mux\|Muxes]] in front of [[Notes/Arithmetic Logic Unit\|ALU]] for example, and *Forwarding Unit*).
	   - Not always possible to forward. For example when reading a register right after load from Memory (In MIPS read of registers is in decode (stage 2) but load from memory is in Memory (stage 4)) - The data we need is not yet in the [[Notes/CPU Pipeline\|Pipeline]].
	     ![Pasted image 20230102180829.png](/img/user/Assets/Pasted%20image%2020230102180829.png)
