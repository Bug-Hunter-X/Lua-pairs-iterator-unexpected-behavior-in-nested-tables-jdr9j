# Lua pairs iterator unexpected behavior in nested tables

This repository demonstrates a subtle bug related to Lua's `pairs` iterator when used within nested tables and modifications occur during iteration. The issue arises when a recursive function traverses a nested table, and changes are made to the table structure within the iteration.

The `bug.lua` file contains the erroneous code. The `bugSolution.lua` file provides a corrected version using a different approach to iterate.

## Bug Description

The `pairs` iterator in Lua does not guarantee the order of iteration. If the table's structure is modified during iteration, `pairs` may skip elements.

## Solution

The solution demonstrates using a different iteration strategy to avoid the issue. Consider using a copy of the table or other appropriate methods based on specific needs.