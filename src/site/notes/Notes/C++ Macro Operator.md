---
{"dg-publish":true,"permalink":"/notes/c-macro-operator/"}
---




# [[Notes/C++\|C++]] Macro Operator \##
In [[Notes/C++\|C++]] there is a macro operator `##` which concatenates tokens in macros.
For example:
```C++
#define type i##nt
type a; // same as int a; since i##nt pastes together to "int"
```

Taken from [## macro operator - C and C++ Syntax Reference - Cprogramming.com](https://www.cprogramming.com/reference/preprocessor/token-pasting-operator.html)
![Pasted image 20220427105614.png](/img/user/Assets/Pasted%20image%2020220427105614.png)
