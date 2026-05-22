# Exponentiation

Apply a matrix A exactly K times to each point by computing A^K.

## Problem

Given N integer points and a 2×2 integer matrix A, compute A^K * P for every point P.

## Input
- First line: integer N (1 ≤ N ≤ 100000).
- Next N lines: two integers x y (|x|,|y| ≤ 10^6).
- Next line: four integers a b c d (|a|,|b|,|c|,|d| ≤ 10^6) — matrix A.
- Last line: integer K (0 ≤ K ≤ 10^18).

## Output
Print N lines: the coordinates after applying A^K to each point.

## Example

Input:
```
2
1 0
0 1
0 1 -1 0
2
```

Output:
```
-1 0
0 -1
```

## Notes
- Compute A^K with fast exponentiation (binary exponentiation) in O(log K) matrix multiplications, then apply to all points in O(N).
- If A or K are such that entries grow beyond 64-bit, consider adding an explicit modulus; this statement assumes input bounds keep results within 64-bit signed integers.