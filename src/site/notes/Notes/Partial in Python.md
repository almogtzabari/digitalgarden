---
{"dg-publish":true,"permalink":"/notes/partial-in-python/","tags":[null]}
---



# Partial in [[Notes/Python\|Python]]
`partial` in [[Notes/Python\|Python]] allows us to call a function with partially applied parameters.

> [!EXAMPLE]
> ```python
> from functools import partial
> 
> def add_x(num, x):
> 	return num + x
> 
> add_5 = partial(add_x, x=5)  # add_5 is now a function
> 
> print(add_5(20))  # This will print 25
> 	
> ```

