---
{"dg-publish":true,"permalink":"/inbox/pipeline-hazards-in-cpu/"}
---



# [[Inbox/CPU Pipeline\|Pipeline]] Hazards in CPU

## Different kinds of hazards
### Structural Hazard
Stems from our hardware.
For example, when we need to write to 3 registers but our hardware only has 2 ports for write.

### Data Hazard
Stems from the data dependencies

To overcome these we can either:
1. Stall - wait for the data to be available
2. Forward - have a bypass fetching the relevant data to the desired [[Inbox/CPU Pipeline\|pipeline]] stage.

### Control Hazard
This hazard is related to branch instructions, and stems from the fact that the [[Inbox/CPU Pipeline\|pipeline]] stage that determines whether we should jump (called [[Branch Resolution\|Branch Resolution]]) is located deep in the pipe.