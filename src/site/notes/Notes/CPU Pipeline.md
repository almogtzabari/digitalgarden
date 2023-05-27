---
{"dg-publish":true,"dg-path":"CPU Pipeline.md","permalink":"/cpu-pipeline/","tags":[null]}
---



# CPU Pipeline
Pipeline is a concept used in the CPU which states that in order to improve throughput (how many instructions executed per cycle) we need to break the actions into separate stages, with [[Flip Flop\|Flip Flop]]s between them.

![DBBF17CB-8C77-4E8E-8300-2312F7DA89A3.png](/img/user/Assets/DBBF17CB-8C77-4E8E-8300-2312F7DA89A3.png)

## Example for different stages in a pipe
- Fectch
- Decode
- Execute
- Memory
- WriteBack
