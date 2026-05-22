# Composition Queries

Range composition of matrices and applying composed transforms to query points.

## Problem

You are given K integer 2×2 matrices A1..Ak. Then you must answer Q queries. Each query provides L R x y and asks for the result of applying the composed matrix A_R * ... * A_L to point (x,y).

## Input
- First line: integers K Q (1 ≤ K, Q ≤ 200000).
- Next K lines: four integers a b c d each (|a|,|b|,|c|,|d| ≤ 10^6) — matrices A1..Ak.
- Next Q lines: four integers L R x y (1 ≤ L ≤ R ≤ K; |x|,|y| ≤ 10^6).

## Output
For each query, print two integers: the coordinates after applying the composed matrix over [L,R] to (x,y).

## Example

Input:
```
3 3
1 0 0 1
0 1 -1 0
2 0 0 2
1 2 1 0
2 3 1 1
1 3 2 3
```

Output:
```
0 -1
2 0
-6 4
```

## Notes
- Use a segment tree (or other range-query structure) that composes matrices to answer each query in O(log K).
- For large answers that may overflow 64-bit, consider an alternate problem variant that asks for results modulo 1e9+7; this statement uses unbounded 64-bit with constrained inputs.