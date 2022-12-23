---
{"dg-publish":true,"permalink":"/notes/branch-resolution/"}
---



# Branch Resolution
[[Notes/Branch Resolution\|Branch Resolution]] is the process in which the [[Notes/CPU\|CPU]] determines whether the branch instruction should be taken or not, and is usually located deep into the [[Notes/CPU Pipeline\|CPU Pipeline]].

The location of the [[Notes/Branch Resolution\|Branch Resolution]] in the pipeline affects the [[Notes/Cycles Per Instruction\|CPI]] - earlier [[Notes/Branch Resolution\|Branch Resolution]] means less instructions flush in case of mis-prediction, which in turn means higher [[Notes/Cycles Per Instruction\|CPI]].
There are different ways to [[Notes/Control Hazard in CPU#How to improve Control Hazard in CPU Control Hazard s overhead?\|reduce the overhead of mis-prediction]]
