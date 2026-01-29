## One-Liner Summary
Merge two sorted arrays using two pointers while skipping duplicates to form a sorted union.

## Pattern
Two Pointers | Merge Pattern | In-place Dedup Logic

## Key Trick
At every step, add the smaller element and skip it if it equals the last added value.

## Mistake / Insight
Mistake: Using a Set and sorting again.
Insight: Sorted input allows linear-time merge + local deduplication.

## Status
✅

## Similar Problems
Intersection of Two Sorted Arrays  
Merge Two Sorted Arrays  
Remove Duplicates from Sorted Array

## Tags
array, two-pointers, merge, deduplication
