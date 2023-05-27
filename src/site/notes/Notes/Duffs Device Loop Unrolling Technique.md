---
{"dg-publish":true,"dg-path":"Duffs Device Loop Unrolling Technique.md","permalink":"/duffs-device-loop-unrolling-technique/","tags":[null]}
---



# Duffs Device Loop Unrolling Technique
[[Notes/Duffs Device Loop Unrolling Technique\|Duffs Device]] is a technique used by most [[Notes/Compiler\|Compiler]]s to do [[Notes/Loop Unrolling\|Loop Unrolling]] which is used when the amount of iterations required for a loop is not known during compilation.

```c
for (int i=0; i<count; i++){
	*to++ = *from++;
}
```

Assuming `count` is not known during compilation, the technique says that:

```c
int n = (count + 7) / 8;
switch (count % 8) {
	case 0: do { *to = *from++;
	case 7:      *to = *from++;
	case 6:      *to = *from++;
	case 5:      *to = *from++;
	case 4:      *to = *from++;
	case 3:      *to = *from++;
	case 2:      *to = *from++;
	case 1:      *to = *from++;
		} while (--n > 0);  // This closes the 'do'
}
```
