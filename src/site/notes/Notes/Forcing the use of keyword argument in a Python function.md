---
{"dg-publish":true,"permalink":"/notes/forcing-the-use-of-keyword-argument-in-a-python-function/"}
---



# Forcing the use of keyword argument in a [[Notes/Python\|Python]] function
In [[Notes/Python\|Python]], there is an option to force the user to pass arguments to a function by keyword only. To do so, all is needed is to add an `*` in front of the arguments of the function.

>[!EXAMPLE]
> ```python
> def my_func(*, arg_a, arg_b):
>    pass
>
> # This will force the user to pass arguments like this:
> my_func(arg_a=1, arg_=2)
> ```
