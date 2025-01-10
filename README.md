# Implicit Type Coercion Bug in JavaScript
This repository demonstrates a common bug in JavaScript related to implicit type coercion.  The bug arises from the use of the + operator with mixed data types (string and number), leading to unexpected string concatenation instead of numerical addition.

## Bug Description
The `foo` function takes two arguments and adds them. The `bar` function calls `foo` and multiplies the result by 2.  When numeric values are passed, it works correctly. However, when a string is passed as an argument, implicit type coercion leads to string concatenation in `foo`, resulting in an incorrect final result in `bar`.

## Solution
The solution involves explicitly converting the input arguments to numbers using `Number()` before performing the addition. This ensures consistent numerical operations regardless of the input types.

## How to Reproduce
1. Clone this repository.
2. Open `bug.js` and run it in a JavaScript environment (e.g., Node.js, browser console). Observe the unexpected output when a string is passed.
3. Open `bugSolution.js` and run it. Observe the correct output after the fix.

This example highlights the importance of explicit type checking and conversion in JavaScript to avoid unexpected behavior due to implicit type coercion.