# Haskell Sort Function Subtlety

This repository demonstrates a potential issue with Haskell's `sort` function when dealing with lists containing elements that are not easily comparable. While the standard `sort` from `Data.List` generally works well for homogenous lists, supplying it with a heterogeneous list may lead to unexpected behavior or even runtime errors depending on the specific implementation and the underlying sorting algorithm. The example shows how using `sort` without explicit type safety can result in problems.

## Bug Description
The `bug.hs` file contains a minimal example that highlights the potential for issues when the list's elements are not consistent.  The `bugSolution.hs` file demonstrates solutions to mitigate this.

## How to Reproduce
1.  Clone this repository.
2.  Compile and run `bug.hs` (using GHC).  The output might vary or result in an error.
3.  Compare the results with the improved example in `bugSolution.hs`.

## Solution
The best way to prevent this issue is to carefully define the types of your lists to ensure they contain comparable elements and handle potential exceptions during sorting if necessary.