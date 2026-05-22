# ROADMAP

## Project Goal

This project is a learning project whose goal is to teach how to build a Kattis-style programming problem from the ground up. The end state is not just a working solution, but a complete problem package that could be submitted for use:

- a clear problem statement
- a correct reference solution
- a starter code file for solvers
- a well-designed test suite
- expected output files
- a local workflow for compiling and checking tests
- a rubric or evaluation guide
- enough understanding to teach the process to someone else

The current example problem idea is a 90-degree clockwise rotation of grid points around the origin.

## What This Project Should Teach

1. How to turn an idea into a fully specified programming problem.
2. How to write a Kattis-style statement that is unambiguous.
3. How to define input, output, constraints, and examples.
4. How to design a correct algorithm before coding.
5. How to write a reference implementation.
6. How to build tests that catch common mistakes.
7. How to create expected outputs for every test.
8. How to run local validation with compile/run/diff checks.
9. How to package the work so it is usable by other people.
10. How to explain the whole process to someone else.

## Current Problem Idea

The current challenge idea is:

- Input: an integer N followed by N ordered pairs of integers
- Task: rotate each point 90 degrees clockwise around the origin
- Output: print the rotated points in the same order
- Transform: (x, y) -> (y, -x)

This is a beginner-friendly problem because the math is simple, the output is deterministic, and the main difficulty is learning how to build a clean contest problem package.

## Roadmap Phases

### Phase 1: Define the Problem

Before writing any code, lock the problem contract.

What to decide:
- the title of the problem
- the exact task description
- the input format
- the output format
- the coordinate limits
- the range of N
- whether the input is assumed valid
- whether the ordering of points must be preserved
- whether the rotation is clockwise or counterclockwise

Why this matters:
- If the statement is unclear, the tests and solution will drift.
- A Kattis-style problem needs a precise contract.
- Most submission failures come from mismatch between the statement and the actual program behavior.

What success looks like:
- You can explain the problem in one paragraph.
- You can write the input and output rules without ambiguity.
- You can manually solve a sample input and get the expected output.

### Phase 2: Design the Solution

After the contract is fixed, design the algorithm.

For the current rotation problem:
- read N
- read each point
- convert each point using the rotation rule
- print the result immediately or store and print later

Why this matters:
- The solution should be as simple as possible.
- The algorithm should match the statement exactly.
- A clean solution helps you build good tests.

What success looks like:
- You can explain the transform in plain language.
- You can explain the same transform using math.
- You can state the runtime and memory usage.

### Phase 3: Write the Statement

Create the full problem statement as if another person will solve it without help.

The statement should include:
- Overview
- Input
- Output
- Constraints
- Example input
- Example output
- Any notes needed to prevent confusion

What to emphasize:
- The rotation direction must be obvious.
- The output format must be exact.
- The ordering of points must be preserved.
- The constraints must match the intended difficulty.

What success looks like:
- A student can read the statement and implement the problem correctly.
- The examples are consistent with the actual transform.
- There are no hidden assumptions.

### Phase 4: Build the Reference Solution

Write the solution that you know is correct.

For this project, the reference solution should:
- use standard input
- read integers in the correct order
- apply the transform (x, y) -> (y, -x)
- print one transformed point per line
- preserve the original ordering

Why this matters:
- The reference solution is the source of truth for expected output.
- It helps validate the tests.
- It gives you something to compare against when troubleshooting.

What success looks like:
- The solution compiles cleanly.
- The solution passes every test case.
- The solution matches the statement exactly.

### Phase 5: Design the Test Suite

Tests should prove that the problem is correct, not just that the sample works.

Test categories to include:
- a basic mixed-sign case
- a single-point case
- a case with the origin only
- axis-aligned points
- repeated points
- all-negative points
- boundary values at the coordinate limits
- a larger N case to confirm consistency and order
- a formatting trap case
- a deterministic regression case

Why this matters:
- One sample is not enough.
- Good tests catch sign errors, ordering errors, and formatting errors.
- A test suite is part of the problem design, not an afterthought.

What success looks like:
- Every test has a reason to exist.
- Every expected output is checked against the true transform.
- The suite catches common wrong answers.

### Phase 6: Create Expected Outputs

Every input file needs a matching output file.

How to do it:
- compute the transformed points using the reference rule
- verify small cases manually
- verify large deterministic cases carefully
- make sure line breaks and spacing are exact

Why this matters:
- Incorrect expected outputs make the tests useless.
- Contest systems compare output exactly.
- This step teaches discipline about formatting.

What success looks like:
- Each input file has a matching output file.
- The output is consistent with the statement and solution.
- There are no extra spaces or missing lines.

### Phase 7: Build a Local Validation Workflow

Create a repeatable process for checking the problem locally.

The workflow should:
- compile the solution
- run it on each test input
- compare actual output to expected output
- report which case passed or failed

Why this matters:
- This is how you catch mistakes before submission.
- It teaches the habit of verifying work systematically.
- It makes debugging faster.

What success looks like:
- You can run the whole suite in one command or one short script.
- A failing case can be identified by name.
- Formatting problems are visible immediately.

### Phase 8: Write the Rubric

If this is also a teaching or grading exercise, document how it will be evaluated.

Rubric categories:
- correctness of the transform
- output formatting
- handling of edge cases
- clarity of the code and explanation

Why this matters:
- Students should know what matters most.
- A rubric helps keep the project aligned to its learning goals.
- It makes the problem easier to teach and review.

What success looks like:
- The rubric matches the actual difficulty of the problem.
- The rubric does not reward irrelevant work.
- The scoring is understandable and fair.

### Phase 9: Teach-Back

The final step is to make sure you can explain the whole process to someone else.

Teach-back should include:
- how the problem was designed
- how the algorithm was chosen
- how the tests were built
- how the outputs were verified
- how the submission-ready package was assembled

Why this matters:
- If you can teach it, you understand it.
- This project is a learning project, not just a coding exercise.
- Teaching reveals gaps in your understanding.

What success looks like:
- You can walk another person through the entire process from scratch.
- You can answer questions about why each artifact exists.
- You can help someone build a similar problem later.

## Workspace File Plan

The matrix folder will eventually hold the challenge assets, organized around the current problem idea.

Planned files:
- matrix.java: current blank Java scaffold
- ROADMAP.md: this learning and implementation roadmap
- problem.md: the problem statement
- tests/input/*.txt: input test cases
- tests/output/*.txt: expected outputs
- run_tests.sh: local test runner
- rubric.md: grading or evaluation guide

## Recommended Build Order

1. Finalize the problem contract.
2. Write the statement.
3. Write the reference solution.
4. Create the test plan.
5. Generate input and output files.
6. Build the local runner.
7. Run and debug the full suite.
8. Write the rubric.
9. Perform the teach-back explanation.

## Quality Checklist

Before considering the project complete, confirm the following:

- The statement is unambiguous.
- The sample matches the actual solution.
- The reference solution passes every test.
- The test suite covers normal and edge cases.
- The output formatting is exact.
- The local workflow is reproducible.
- The rubric matches the project goals.
- You can explain the full process to someone else.

## Notes

This roadmap intentionally focuses on the process of building a Kattis-style problem from the ground up. The current rotation challenge is the example problem being used to teach the workflow, but the process should generalize to other contest problems later.
