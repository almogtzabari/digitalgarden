---
{"dg-publish":true,"permalink":"/inbox/branch-resolution/"}
---



# Branch Resolution
[[Inbox/Branch Resolution\|Branch Resolution]] is the process in which the [[Inbox/CPU\|CPU]] determines whether the branch instruction should be taken or not, and is usually located deep into the [[Inbox/CPU Pipeline\|CPU Pipeline]].

The location of the [[Inbox/Branch Resolution\|Branch Resolution]] in the pipeline affects the [[Inbox/Cycles Per Instruction\|CPI]] - earlier [[Inbox/Branch Resolution\|Branch Resolution]] means less instructions flush in case of mis-prediction, which in turn means higher [[Inbox/Cycles Per Instruction\|CPI]].
There are different ways to [[Inbox/Control Hazard in CPU#How to improve Control Hazard in CPU Control Hazard s overhead?\|reduce the overhead of mis-prediction]]
