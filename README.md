# Rust Raw Pointer and Vector Reallocation Bug

This repository demonstrates a subtle bug that can occur in Rust when working with raw pointers and vectors. Modifying a vector through a raw pointer after operations that might reallocate the vector's memory (like push, insert, etc.) is dangerous and can cause undefined behavior. The provided example showcases this problem and its solution.

## Bug Description
The original `bug.rs` file contains code that attempts to modify a vector via a raw pointer after potentially changing the vector's capacity.  This leads to the pointer pointing to an invalid memory location resulting in unexpected behavior (potential crashes, incorrect values, etc.).

## Solution
The `bugSolution.rs` file shows a safe solution using proper methods for modifying the vector that prevents such issues.  Always prefer using safe vector methods instead of directly manipulating raw pointers unless absolutely necessary and you fully understand the implications.