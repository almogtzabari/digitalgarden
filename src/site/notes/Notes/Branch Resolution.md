---
{"dg-publish":true,"permalink":"/notes/branch-resolution/","tags":[null]}
---



# Branch Resolution
[[Notes/Branch Resolution\|Branch Resolution]] is the process in which the [[Notes/Central Processing Unit\|Central Processing Unit]] determines whether the branch instruction should be taken or not, and is usually located deep into the [[Notes/CPU Pipeline\|CPU Pipeline]].

The location of the [[Notes/Branch Resolution\|Branch Resolution]] in the pipeline affects the [[Notes/Cycles Per Instruction\|CPI]] - earlier [[Notes/Branch Resolution\|Branch Resolution]] means less instructions flush in case of mis-prediction, which in turn means lower [[Notes/Cycles Per Instruction\|CPI]] (lower [[Notes/Cycles Per Instruction\|CPI]] is better).

There are different ways to [[Notes/Branch Prediction\|reduce the overhead of mis-prediction]].
