## One-Liner Summary
Count pairs (i, j) where i < j and nums[i] > 2 * nums[j] using merge sort.

## Pattern
Divide and conquer, two pointers, merge sort.

## Key Trick
During merge, if left[i] > 2 * right[j], then all remaining left elements form valid pairs with right[j].

## Mistake / Insight
Always cast to long in comparison to avoid overflow in 2 * nums[j].

## Status (❌/⚠️/✅)
✅

## Similar Problems
Count Inversions  
Reverse Pairs II  
Count Smaller After Self  
Important Reverse Pairs

## Tags
array, divide-and-conquer, merge-sort, two-pointers, math
