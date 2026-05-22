# Sequence of Matrices

Apply a sequence of M integer 2×2 matrices to each point (in the specified order).

## Problem

Given N integer points and M matrices M1..Mm, apply the matrices in order to each point: P' = Mm * ... * M2 * M1 * P.

## Input
- First line: integers N M (1 ≤ N ≤ 50000, 1 ≤ M ≤ 1000).
- Next N lines: two integers x y (|x|,|y| ≤ 10^6).
- Next M lines: four integers a b c d each (|a|,|b|,|c|,|d| ≤ 10^6) — matrix Mi in row-major order.

## Output
Print N lines: the transformed coordinates after applying all M matrices.

## Example

Input:
```
2 2
1 0
0 1
0 1 -1 0
2 0 0 2
```

Output:
```
0 -2
2 0
```

## Notes
- Computing the combined matrix C = Mm * ... * M1 first (O(M)) and then applying C to each point (O(N)) yields O(M+N) time.
- Use 64-bit integers for safety.