## One-Liner Summary
Move all zeros to the end while preserving relative order of non-zero elements using two pointers.

## Pattern
Stable partition, two pointers.

## Key Trick
Maintain a pointer j for next non-zero position and swap/overwrite when nums[i] ≠ 0.

## Mistake / Insight
Blind swapping can break stability; ensure non-zero elements keep original order.

## Status (❌/⚠️/✅)
✅

## Similar Problems
Sort Colors  
Move Zeros to Beginning  
Partition Array by Pivot

## Tags
array, two-pointers, stable, in-place, partition
