# Closure Issue in setTimeout Loop

This repository demonstrates a common closure issue in JavaScript when using `setTimeout` within a loop. The problem arises because the callback function within `setTimeout` doesn't capture the value of `i` at the time it's created, but rather captures a reference to the variable `i`. By the time the `setTimeout` callbacks execute, the loop has already finished, and `i` holds its final value (10).

## Bug

The `bug.js` file contains the problematic code.  Running this code will print '10' ten times instead of 0 through 9.

## Solution

The `bugSolution.js` file shows how to fix this issue using an immediately invoked function expression (IIFE) or `let` to create a new scope for each iteration of the loop.