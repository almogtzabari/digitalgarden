---
{"dg-publish":true,"permalink":"/notes/c-rule-of-three/","tags":[null]}
---



# C++ Rule of Three
The rule of three in [[Notes/C++\|C++]] says that:
>[!QUESTION] If
if you need to implement **any** of these 3 methods:
>1. `~Class();` - Destructor
>2. `Class(Class &);` - Copy constructor
>3. `Class & operator = (Class &);` - Copy assignment

>[!WARNING] Then
>Then you need to implement all of them.

## Why?
Unless implemented, the [[Notes/Compiler\|Compiler]] will define a default for the above methods, however, if we change one of these then the default version of the other two won't be sufficient.
