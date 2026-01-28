## One-Liner Summary
Check whether the maximum element in the array is at least twice as large as every other element and return its index if true.

## Pattern
Array | Max & Second Max Tracking

## Key Trick
The condition only needs to be checked against the second largest element, not all elements.

## Mistake / Insight
Mistake: Comparing the largest element with every other element unnecessarily.
Insight: If max ≥ 2 × secondMax, it automatically satisfies the condition for all smaller values.

## Status
✅

## Similar Problems
Second Largest Element in an Array  
Dominant Index  
Largest Number At Least K Times of Others

## Tags
array, greedy, max-tracking, single-pass
