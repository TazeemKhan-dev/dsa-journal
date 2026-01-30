## One-Liner Summary
In-place sorting of 0s, 1s, and 2s using Dutch National Flag partitioning.

## Pattern
Three pointers, array partitioning.

## Key Trick
Maintain low, mid, high pointers and decide swaps solely based on nums[mid].

## Mistake / Insight
Never increment mid after swapping with high; the incoming value must be checked again.

## Status (❌/⚠️/✅)
✅

## Similar Problems
Move Zeroes  
Partition Array by Pivot  
Sort Colors II

## Tags
array, two-pointers, partition, in-place, dnf
