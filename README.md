# Just

Just is a programming language that compiles to JavaScript

## Goals

- Simple type system
- Fully functional
- Optmized output
- No undefined
- Interop with js

## Ideas

- No `function` reserved work
- Return type before function definition
- If return type is provided, the last line of the function body is returned
- If return type is `void` nothing is returned, even from the last line
- If the next argument is the same type as previous, you can avoid it
- No `let` `var` `const` for variable/constant assignment

```just
// Return type, arguments type
number sum(number a, number b) {
    a + b
}

// Arguments type reuse
number sub(number a, b) {
    a - b
}

// JS interop, void type
from "std:console" use { log }

void print_error(string message) {
    log(message)
}

// Variable assignment
string name = "Hello, World"
number age = 10;

// Inline dictionaries
dict { string name, number age } person = { name, age }

// Named dictionaries
dict { string name, number age } Person

Person person = { name, age }
```
