---
{"dg-publish":true,"permalink":"/notes/structural-hazard-in-cpu/"}
---



# Structural Hazard in CPU
Structural hazard is a type of [[Notes/Pipeline Hazards in CPU\|Pipeline Hazards in CPU]] that occur due to limitation in our hardware.

For example, when we need to write to 3 registers but our hardware only has 2 ports for write.

Another example is when we use the memory (read/write) in 2 pipeline stages (like *Fetch* and *Memory* stages in MIPS [[Notes/CPU\|CPU]]). To overcome that we can split the memory into 2:
- Instructions memory
- Data memory
