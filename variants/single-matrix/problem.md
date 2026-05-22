# Single Matrix

Apply a single integer 2×2 matrix to each point.

## Problem

Given N integer points (x, y) and an integer 2×2 matrix A = [[a, b], [c, d]], compute A * (x, y) for every input point and print the transformed coordinates in the same order.

## Input
- First line: integer N (1 ≤ N ≤ 100000).
- Next N lines: two integers x and y (|x|,|y| ≤ 10^6).
- Last line: four integers a b c d (|a|,|b|,|c|,|d| ≤ 10^6) — the matrix in row-major order.

## Output
Print N lines. Each line: `x' y'` where

x' = a*x + b*y

y' = c*x + d*y

## Example

Input:
```
3
1 2
0 -1
5 5
0 1 -1 0
```

Output:
```
2 -1
-1 0
5 -5
```

## Notes
- Use 64-bit signed integers for intermediate results.
- Complexity: O(N).
- This variant is beginner-friendly and focuses on matrix application correctness.