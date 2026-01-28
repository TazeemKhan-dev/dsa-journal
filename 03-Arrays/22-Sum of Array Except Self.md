## One-Liner Summary
Compute the total sum once and subtract the current element from it to get the sum of all other elements.

## Pattern
Array | Prefix Concept | Total Aggregation

## Key Trick
Instead of recomputing sums for each index, reuse the total sum and subtract the current value.

## Mistake / Insight
Mistake: Using nested loops to sum elements for every index.
Insight: Since subtraction is allowed, total sum makes the problem linear.

## Status
✅

## Similar Problems
Product of Array Except Self  
Running Sum of Array  
Prefix Sum Applications

## Tags
array, prefix-sum, math, optimization
