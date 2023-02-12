---
{"dg-publish":true,"permalink":"/notes/integer-multiplication/","tags":[null]}
---



# Integer Multiplication
How do we multiply `1011` (called *multiplicand*) by `0101` (called *multiplier*)?
This is usually done inside the [[Notes/Central Processing Unit\|Central Processing Unit]] using *add* and *shift* operations, involving the [[Notes/Arithmetic Logic Unit\|ALU]] (and [[Notes/Full Adder\|Full Adder]])

## An Iterative Algorithm
### The Idea
The idea is to iteratively shift the *multiplicand* left by 1 and the *multiplier* right by 1, and if the LSB of the *multiplier* is 1 -> add the shifted *multiplicand* to the intermediate result.


### Pseudo code
```python
def multiply(multiplicand, multiplier):
	result = 0
	while multiplier > 0:
		temp = result + multiplicand
		if multiplier.lsb == 1:
			result = temp
		multiplier >> 1
		multiplicand << 1
	return result
```

### Notes
- If the *multiplicand* is `n` bits and *multiplier* is `m` bits then the result is `n+m` bits.
- The registers of the *multiplicand* and the results need to be `n+m` bits, whereas the register of the *multiplier* can remain `m` bits.

### How to implement in hardware
<iframe width="100%" height="400" src="https://www.youtube-nocookie.com/embed/IeRm--sokdg" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

![Pasted image 20230103100241.png](/img/user/Assets/Pasted%20image%2020230103100241.png)
