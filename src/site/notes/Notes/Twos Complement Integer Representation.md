---
{"dg-publish":true,"dg-path":"Twos Complement Integer Representation.md","permalink":"/twos-complement-integer-representation/","tags":[null]}
---



# Twos Complement Integer Representation
The Twos Complement is the method we currently use for representing integers.
While its a bit inconvenient to us to read a negative number, it does make the arithmetic much easier.


<iframe width="100%" height="400" src="https://www.youtube-nocookie.com/embed/zbV941Qcdwo" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## How to represent a positive number
Positive numbers are represented using the same binary format.
One thing to notice is that the [[Notes/Most Significant Bit\|MSB]] is a sign bit. For positive numbers this bit is $0$.
## How to represent a negative number
1. Represent as positive binary number
2. Flip all bits
3. Add 1

>[!EXAMPLE] Example: Representing $-10$
> 1. 10 in binary is 01010
> 2. Flip bits: 01010 -> 10101
> 3. Add 1: 10101 -> 10110
> 
> $$\Rightarrow\boxed{-10 = 10110}$$

## How to convert a negative number to positive
1. Subtract 1
2. Flip bits

>[!EXAMPLE] Example: converting $-10$ to $10$
> -10 in binary is 10110
> 1. Subtract 1: 10110 -> 10101
> 2. Flip bits: 10101 -> 01010
> 
> $$\Rightarrow\boxed{10 = 01010}$$