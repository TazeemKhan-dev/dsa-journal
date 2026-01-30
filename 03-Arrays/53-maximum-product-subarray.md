## One-Liner Summary
Find the contiguous subarray with the maximum product using dynamic tracking of max and min products.

## Pattern
Dynamic programming, Kadane variant.

## Key Trick
Track both maxEnding and minEnding because a negative can turn a minimum into a maximum.

## Mistake / Insight
Ignoring the minimum product breaks cases with odd/even negative counts.

## Status (❌/⚠️/✅)
✅

## Similar Problems
Maximum Sum Subarray  
Minimum Product Subarray  
Maximum Product of Three Numbers  
Maximum Circular Subarray

## Tags
array, dp, kadane, prefix-suffix, greedy
