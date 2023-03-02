---
{"dg-publish":true,"permalink":"/notes/how-to-print-a-fixed-width-number-in-python-with-f-string-digits-before-decimal-point/"}
---




# How to print a fixed width number in [[Notes/Python\|Python]] with [[Notes/F-string\|F-string]] (digits before decimal point)
In order to print (with [[Notes/F-string\|F-string]]) a number with a fixed amount of digits **before** the decimal point, one has to a add `:0<count>` inside the `{}`.

> [!example]
>```Python
>print(f"{251:05}")
>```
>> [!note] Result
>>
>> 00251