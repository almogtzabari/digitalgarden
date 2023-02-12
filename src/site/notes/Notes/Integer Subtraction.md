---
{"dg-publish":true,"permalink":"/notes/integer-subtraction/","tags":[null]}
---



# Integer Subtraction
Subtraction is executed using the numbers adder (like [[Notes/Ripple Carry Adder\|Ripple Carry Adder]] for example).
The idea is that:
$$
A-B = A + (-B)
$$

In [[Notes/Ripple Carry Adder\|Ripple Carry Adder]] (and using [[Notes/Twos Complement Integer Representation\|Twos Complement Integer Representation]], we add [[Mux\|Muxes]] before the *B*s, along with [[NOT Gate\|NOT Gate]] in front of one of the entries, and also pass *1* to the *Cin* input of the [[Notes/Ripple Carry Adder\|Ripple Carry Adder]].

![Pasted image 20230103130746.png](/img/user/Assets/Pasted%20image%2020230103130746.png)

<iframe width="100%" height="400" src="https://www.youtube-nocookie.com/embed/Rt8bI5iEsSA" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>