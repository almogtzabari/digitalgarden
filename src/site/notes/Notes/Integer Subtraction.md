---
{"dg-publish":true,"permalink":"/notes/integer-subtraction/"}
---



# Integer Subtraction
Subtraction is executed using the numbers adder (like [[Notes/Ripple Carry Adder\|Ripple Carry Adder]] for example).
The idea is that:
$$
A-B = A + (-B)
$$

In [[Notes/Ripple Carry Adder\|Ripple Carry Adder]] (and using [[Notes/Twos Complement\|Twos Complement]], we add [[Mux\|Muxes]] before the *B*s, along with [[NOT Gate\|NOT Gate]] if front of one of the entries, and also pass *1* to the *Cin* input of the [[Notes/Ripple Carry Adder\|Ripple Carry Adder]].


<iframe width="100%" height="400" src="https://www.youtube-nocookie.com/embed/Rt8bI5iEsSA" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>