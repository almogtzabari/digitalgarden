---
{"dg-publish":true,"permalink":"/notes/amdahls-law-for-speedup/"}
---



# Amdahl's Law for speedup
In general, Amdahl's Law says that it is better to speed-up the more frequent tasks over the less frequent, even if the speed-up is small.

## Speedup definition
Speedup of a program is defined as:
$$
speed\_up = \frac{old\_cpu\_time}{new\_cpu\_time}
$$
## The Law
If we improve $F$ fraction of our program by $speed\_up(F)$ then the overall speedup is as follows:
$$
speed\_up = \frac{1}{(1-F) + \frac{speed\_up(F)}{F}}
$$