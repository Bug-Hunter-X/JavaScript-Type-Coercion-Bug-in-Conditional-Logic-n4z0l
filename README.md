# JavaScript Type Coercion Bug

This repository demonstrates a subtle bug in JavaScript related to type coercion in conditional statements.  The function `foo` intends to check for null, negative numbers, and positive numbers. However, due to loose comparison, it handles '0' as a string incorrectly. 

The `bug.js` file contains the buggy code.  The `bugSolution.js` file demonstrates a corrected version using strict comparison (`===`).

## Bug Description
JavaScript's loose comparison (`==`) can lead to unexpected behavior when comparing values of different types.  In the original code, `x == 0` evaluates to true for both the number `0` and the string `"0"`, resulting in an incorrect return value.

## Solution
The solution uses strict comparison (`===`) to avoid type coercion.  Strict comparison only evaluates to true if both the value and the type are identical.

## How to run
1. Clone this repository.
2. Navigate to the repository directory.
3. Open `bug.js` and `bugSolution.js` to view the buggy and corrected code respectively. 
4. Run each file using Node.js (e.g. `node bug.js` and `node bugSolution.js`) to observe the output differences.