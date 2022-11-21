---
{"dg-publish":true,"permalink":"/notes/assert-in-python/"}
---



# Assert in Python
## Equivalent
An simple assert statement in [[Notes/Python\|Python]] is equivalent to the following:
```python
if __debug__:
    if not expression:
	    raise AssertionError
```
## Reasons to use `assert`
1. It Helps detect problems early in your program, where the cause is clear, rather than later when some other operation fails. A type error in Python, for example, can go through several layers of code before actually raising an `Exception` if not caught early on.
2. It works as documentation for other developers reading the code, who see the `assert` and can confidently say that its condition holds from now on.

## Syntax
```python
assert condition, optional_message
```

> [!EXAMPLE]
> ```python
> assert x == 10, "X was supposed to be 10 but is not!"
> ```

> [!Caution] Caution
> Do not use parenthesis as it will run the `assert` with a tuple as it's first argument, which is not desired.
>> [!error] Wrong
>> ```python
>> assert(x==10, "X was supposed to be 10 but is not!")



## References
- [What is the use of "assert" in Python? - Stack Overflow](https://stackoverflow.com/questions/5142418/what-is-the-use-of-assert-in-python)
- [Python 3.11.0 documentation - The assert statement](https://docs.python.org/3/reference/simple_stmts.html#assert)