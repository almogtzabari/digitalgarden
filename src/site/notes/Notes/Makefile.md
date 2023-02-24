---
{"dg-publish":true,"permalink":"/notes/makefile/","tags":[null]}
---



# Makefile
## What is a Makefile?
A Makefile is a file used in [[Notes/Software\|software]] development to automate the process of building and compiling [[Notes/Software\|software]] programs. It's typically used in projects that are written in [[Notes/Programming\|programming]] languages like [[C\|C]], [[Notes/C++\|C++]], and Fortran, but it can be used for other types of projects as well. The Makefile contains a set of rules and dependencies that describe how the [[Notes/Software\|software]] is built, and how its components are related to each other.

When you run the "make" command, it reads the Makefile and determines the current state of the [[Notes/Software\|software]] project. If any of the components of the project have been modified, the make command will recompile those components and link them to form the final executable program. If none of the components have been modified, the make command will skip the build process and simply return the current state of the [[Notes/Software\|software]].

The key benefit of using a Makefile is that it saves time and effort by automating the build process. With a well-written Makefile, developers can simply type "make" to compile their [[Notes/Software\|software]], without having to manually track dependencies and recompile individual components. This makes it easier to keep track of the build process and ensures that the [[Notes/Software\|software]] is always up-to-date and in a consistent state.

## Makefile Structure
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