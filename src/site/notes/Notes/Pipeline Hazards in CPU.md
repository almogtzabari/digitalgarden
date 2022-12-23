---
{"dg-publish":true,"permalink":"/notes/pipeline-hazards-in-cpu/"}
---



# [[Notes/CPU Pipeline\|Pipeline]] Hazards in CPU

## Different kinds of hazards
### Structural Hazard
Stems from our hardware.
For example, when we need to write to 3 registers but our hardware only has 2 ports for write.

### Data Hazard
Stems from the data dependencies

To overcome these we can either:
1. Stall - wait for the data to be available
2. Forward - have a bypass fetching the relevant data to the desired [[Notes/CPU Pipeline\|pipeline]] stage.

### [[Notes/Control Hazard in CPU\|Control Hazard]]

<div class="transclusion internal-embed is-loaded"><div class="markdown-embed">

$<div class="markdown-embed-title">

# Control Hazard

</div>





# Control Hazard in CPU
[[Notes/Control Hazard in CPU\|Control Hazard in CPU]] is a type of [[Notes/Pipeline Hazards in CPU\|Pipeline Hazards in CPU]] related to branch instructions, which occur due to the fact that the [[Notes/Branch Resolution\|Branch Resolution]] is located deep in the [[Notes/CPU Pipeline\|Pipeline]]. In order to reduce the overhead of this kind of hazards we use [[Inbox/Branch Prediction\|Branch Prediction]] techniques. ^6e8c96

</div></div>
