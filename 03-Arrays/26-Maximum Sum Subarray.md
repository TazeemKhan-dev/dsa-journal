## One-Liner Summary
Find the maximum sum over all contiguous subarrays using Kadane’s dynamic programming approach.

## Pattern
Dynamic Programming | Sliding Window (Implicit)

## Key Trick
At each index, either extend the previous subarray or start a new one.

## Mistake / Insight
Mistake: Trying all subarrays (O(n²)).
Insight: Negative prefix never helps a future maximum.

## Status
✅

## Similar Problems
Maximum Product Subarray  
Maximum Sum Circular Subarray  
Subarray with Given Sum

## Tags
array, dynamic-programming, kadane, prefix
