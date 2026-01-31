## One-Liner Summary
Merge two sorted arrays in-place by filling nums1 from the back using two pointers.

## Pattern
Two pointers, reverse merge, in-place overwrite avoidance.

## Key Trick
Compare the largest remaining elements and place the maximum at the last free index in nums1.

## Mistake / Insight
Mistake: Merging from the front overwrites useful values in nums1.  
Insight: Backward filling preserves all unprocessed elements.

## Status (❌/⚠️/✅)
✅

## Similar Problems
Merge Two Sorted Lists  
Intersection of Two Arrays II  
Median of Two Sorted Arrays  
Squares of a Sorted Array

## Tags
array, two-pointers, merge, in-place, sorting, classic-interview-pattern
