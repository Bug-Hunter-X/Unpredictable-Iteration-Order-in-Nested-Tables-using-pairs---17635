# Lua Nested Table Iteration Order Bug

This repository demonstrates a potential issue with Lua's `pairs` iterator when dealing with nested tables. The `pairs` function does not guarantee a specific iteration order, which can lead to unexpected behavior in recursive functions or any code that depends on a consistent order of traversal.

## Bug Description
The provided Lua code recursively iterates over a nested table.  However, the order in which `pairs` iterates over the keys is not consistent across different Lua implementations or even different runs of the same program. This lack of order consistency can cause unexpected issues if your code relies on the iteration order.

## Solution
The solution involves using a different approach that explicitly controls the iteration order, like sorting the keys before iteration or using a different data structure to manage the table traversal.

## How to reproduce
1. Clone this repository.
2. Run the `bug.lua` file using a Lua interpreter.
3. Observe that the output (although functionally correct) might change slightly in different runs due to the unpredictable iteration order.