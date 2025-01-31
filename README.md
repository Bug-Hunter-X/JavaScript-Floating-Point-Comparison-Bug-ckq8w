# JavaScript Floating-Point Comparison Bug

This repository demonstrates a common, yet subtle, bug in JavaScript related to comparing floating-point numbers using strict equality (===).  Strict equality can fail when comparing floating-point numbers due to the inherent limitations of floating-point precision.

## The Bug

The `foo` function is intended to check if two numbers are equal. However, due to the use of `===`, it fails for numbers that are very close but not exactly equal due to floating-point precision issues.

## The Solution

The solution is to avoid strict equality for floating-point comparisons and instead use a tolerance-based comparison. This accounts for minor differences due to precision.

## How to reproduce the bug and the solution

1. Clone the repo.
2. Open the 'bug.js' file and execute the `foo` function with different input values. Note the unexpected results in specific cases where floating-point inaccuracies manifest.
3. Open the 'bugSolution.js' file. It shows how to solve this by using a tolerance-based comparison that handles floating-point precision limitations. 