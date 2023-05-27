---
{"dg-publish":true,"dg-path":"Inline Functions In C++.md","permalink":"/inline-functions-in-c/"}
---



# Inline Functions In [[Notes/C++\|C++]]
## Why do we need inline functions?
Look at the following code:
```c
for (int i=0; i<999999; i++){
	ret = do_some_function(args);
}
```

If the function execute a small number of instructions, then the overhead of calling a function (passing arguments and returning the return value) is not negligible, and for that reason inline function exist ==> to save a function call.
