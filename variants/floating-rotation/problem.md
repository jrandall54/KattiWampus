# Floating-point Rotation (Advanced)

Rotate points by an arbitrary angle or apply a floating-point 2×2 matrix, with explicit rounding rules.

## Problem

Given N integer points and either (A) an angle θ in degrees, or (B) a 2×2 matrix with floating-point entries, apply the transform to each point and print integer coordinates after rounding.

## Input (angle option)
- First line: integer N (1 ≤ N ≤ 5000).
- Next N lines: two integers x y (|x|,|y| ≤ 10^6).
- Last line: floating-point θ — rotate points clockwise by θ degrees.

## Input (matrix option)
- First line: integer N.
- Next N lines: x y.
- Next two lines: two floats each — rows of a 2×2 matrix.

## Output
Print N lines with two integers each: the transformed coordinates rounded to the nearest integer (ties rounded toward +infinity). Use an absolute tolerance of 1e-6 when comparing floating results before rounding.

## Example

Input:
```
1
1 1
90.0
```

Output:
```
1 -1
```

## Notes
- Convert degrees to radians and use the rotation matrix [[cosθ, -sinθ],[sinθ, cosθ]].
- Define and follow the rounding rule precisely to avoid ambiguous judge behavior.
- This variant requires careful handling of floating precision and is intended as an advanced problem.