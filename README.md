# F# Mutable Variable Swap Bug

This repository demonstrates a common error in F# when working with mutable variables and functions that intend to swap values.  The issue stems from F#'s pass-by-reference behavior for mutable variables.  The solution showcases how to correctly swap variables using techniques that avoid unintended side effects.

## Bug Description
The `swap` function attempts to swap the values of two mutable variables. However, due to pass-by-reference, modifying the variables inside the function directly modifies the original variables, leading to unexpected results.  The expected output is a swap of values, but the actual output shows both variables having the same value after the function call.

## Solution
The solution addresses the problem by creating a new tuple containing the swapped values and returning this tuple.  This avoids directly modifying the original variables, thus producing the expected output.
