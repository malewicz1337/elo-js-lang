# Custom Expression Parser and Evaluator in JavaScript

This project contains a custom expression parser and evaluator written in JavaScript. It allows parsing and evaluating expressions based on a defined syntax and scope. The code includes support for basic arithmetic operations, control structures like `if`, `while`, and `do`, and the ability to define functions.

## Installation

No additional installation is required for this script as it is written in plain JavaScript. Simply include the provided JavaScript files in your project.

## Usage

To use the expression parser and evaluator, first write an expression according to the syntax rules defined in the script. Then, run the expression using the `run` function.

### Basic Example

```javascript
run(`
    do(define(total, 0),
        define(count, 1),
        while(<(count, 11),
            do(define(total, +(total, count)),
                define(count, +(count, 1)))),
        print(total))
`);
```

This example calculates the sum of numbers from 1 to 10.

### Function Definition Example

```javascript
run(`
    do(define(plusOne, fun(a, +(a, 1))),
        print(plusOne(10)))
`);

run(`
    do(define(pow, fun(base, exp,
        if(==(exp, 0),
            1,
            *(base, pow(base, -(exp, 1)))))),
        print(pow(2, 10)))
`);
```

The first example defines a function plusOne that adds 1 to its argument. The second example defines a pow function for exponentiation.

## Features

- **Expression Parsing:** Parses expressions written in a custom syntax.
- **Control Structures:** Supports `if`, `while`, and `do` constructs.
- **Function Definition:** Allows defining functions within the script.
- **Arithmetic Operations:** Includes basic arithmetic operations like addition, subtraction, multiplication, and division.

## License

This project is licensed under the [MIT License](LICENSE.md).
