---
{"dg-publish":true,"dg-path":"Strict Mode in JavaScript.md","permalink":"/strict-mode-in-java-script/"}
---




# <%+ tp.file.title %>
### What is it?
[[Notes/Strict Mode in JavaScript\|Strict Mode in JavaScript]] is a special mode in [[Notes/JavaScript\|JavaScript]] which makes it easier for us to write a secure [[Notes/JavaScript\|JavaScript]] code (less bugs and accidental errors).
This is achieved because it:

1. Forbids us to do certain things.
2. Presents us with errors where otherwise [[Notes/JavaScript\|JavaScript]] would fail silently.

### How to use?
In order to activate [[Notes/Strict Mode in JavaScript\|Strict Mode in JavaScript]], one need to write the string `'use strict'` **at the very first line of the script**.
> [!example]
> ```js
> 'use strict';
> 
> let varName = 'My script goes here...';
>```
