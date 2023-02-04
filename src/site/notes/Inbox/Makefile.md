---
{"dg-publish":true,"permalink":"/inbox/makefile/","tags":[null]}
---



# Makefile
A Makefile is a file defining the rules of how to compile/build, and has the following structure:
```makefile
target: dependencies
	action
```
Where:
- *target* - this is how we ask the Makefile to run this target. For example, to use `make clean` we need to define a target call `clean`.
- *dependencies* - Space-separated list of files to look for changes. 
- *action* - Which action to take in case of "changes detected".

## Simple Makefile Example
```makefile
// Makefile

output: main.o control_unit.o sensor.o memory.o
	g++ main.o control_unit.o sensor.o memory.o -o output

main.o: main.cpp
	g++ -c main.cpp

control_unit.o: control_unit.cpp control_unit.h
	g++ -c control_unit.cpp

sensor.o: sensor.cpp sensor.h
	g++ -c sensor.cpp

memory.o: memory.cpp memory.h
	g++ -c memory.cpp

clean:
	rm *.o output
```

---

## Full Example
>[!EXAMPLE] Full Example
>A Full example of a project along with its folder structure and Makefile can be found [here](https://github.com/TheNetAdmin/Makefile-Templates/tree/master/SmallProject)