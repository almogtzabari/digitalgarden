---
{"dg-publish":true,"permalink":"/inbox/forcing-the-use-of-keyword-argument-in-a-python-function/"}
---



# Forcing the use of keyword argument in a Python function
There is an option to force the user to pass arguments to a function by keyword only. To do that, all is needed, is to add an `*` arguments of the function.

>[!EXAMPLE]
> ```python
> def my_func(*, arg_a, arg_b):
>    pass
>
> # This will force the user to pass arguments like this:
> my_func(arg_a=1, arg_=2)
> ```
