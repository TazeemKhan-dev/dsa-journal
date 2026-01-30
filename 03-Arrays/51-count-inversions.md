## One-Liner Summary
Count how far an array is from being sorted by counting all (i, j) where i < j and nums[i] > nums[j].

## Pattern
Divide and conquer, merge sort, prefix counting.

## Key Trick
During merge, if left[i] > right[j], then all remaining left elements form inversions with right[j].

## Mistake / Insight
Using int for inversion count overflows; always use long.

## Status (❌/⚠️/✅)
✅

## Similar Problems
Reverse Pairs  
Count Smaller After Self  
Number of Swaps to Sort  
Minimum Adjacent Swaps

## Tags
array, divide-and-conquer, merge-sort, fenwick-tree, math
