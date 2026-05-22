# Rotate Points

Rotate a list of 2D integer points 90 degrees clockwise around the origin.

## Problem

Given N ordered pairs of integers representing points (x, y), rotate each point 90 degrees clockwise around the origin and output the transformed points in the same order.

## Input

- The first line contains an integer N (1 ≤ N ≤ 1000) — the number of points.
- Each of the next N lines contains two integers x and y (-10^6 ≤ x, y ≤ 10^6) separated by a space.

You may assume the input is valid and contains exactly N pairs after the first line.

## Output

Print N lines. Each line should contain two integers x' and y' separated by a space — the coordinates of the point after a 90-degree clockwise rotation, in the same order as the input.

The transform is:

 (x, y) → (y, -x)

## Example

Input

```
4
1 2
-3 0
0 0
5 -7
```

Output

```
2 -1
0 3
0 0
-7 -5
```

## Notes

- Ordering must be preserved: the i-th output line corresponds to the i-th input point.
- Coordinate and N limits above are chosen as sensible defaults for a beginner-friendly problem; they keep values small enough for simple integer arithmetic while allowing enough variety to test edge cases.
