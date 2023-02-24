---
{"dg-publish":true,"permalink":"/inbox/inline-functions-in-c/","tags":[null]}
---



# Inline Functions In C++
## Why do we need inline functions?
Look at the following code:
```c
for (int i=0; i<999999; i++){
	ret = do_some_function(args);
}
```

If the function execute a small number of instructions, then the overhead of calling a function (passing arguments and returning the return value) is not negligible, and for that reason inline function exist ==> to save a function call.
