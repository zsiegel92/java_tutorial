# Welcome to Java!

[TOC]

## Array Lists

Creating Array Lists, and converting between Array Lists and arrays can be tricky. See these examples:

<iframe height="400px" width="100%" src="https://repl.it/@ZSiegel/ArrayListExample?lite=true" scrolling="no" frameborder="no" allowtransparency="true" allowfullscreen="true" sandbox="allow-forms allow-pointer-lock allow-popups allow-same-origin allow-scripts allow-modals"></iframe>


## Arrays: `int[]` vs `Integer[]`

Creating `Integer[]` and `int[]` arrays, and converting back and forth, can be tricky. Remember that `int` is a primitive data type, whereas `Integer` is an object.

When we pass an `Integer` to a function, a pointed to its location in memory is passed, and so the value it holds can be altered. When we pass an `int` variable to a function, its value is passed, and any changes happen only within the scope of the function call.

<iframe height="400px" width="100%" src="https://repl.it/@ZSiegel/intandInteger?lite=true" scrolling="no" frameborder="no" allowtransparency="true" allowfullscreen="true" sandbox="allow-forms allow-pointer-lock allow-popups allow-same-origin allow-scripts allow-modals"></iframe>
