---
{"dg-publish":true,"permalink":"/notes/register-renaming/"}
---



# Register Renaming
[[Notes/Register Renaming\|Register Renaming]] is a technique to overcome [[Notes/Data Hazard in CPU\|false and anti dependencies]] resulting from [[Notes/Out Of Order Execution\|Out Of Order Execution]].

The idea is to keep 2 sets of registers:
1. Architectural Registers - This is what the programmer/compiler is exposed to.
2. Physical Registers - A large pool of physical registers available for the micro-architecture.

In addition to those sets, we also keep a bi-directional mapping between those sets, which is updated between the *Decode* and *Execute* stages.
