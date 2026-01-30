## One-Liner Summary
Transform the array into the next lexicographically greater permutation in-place.

## Pattern
Greedy, suffix analysis, two pointers.

## Key Trick
Find pivot from right, swap with next greater element, then reverse suffix.

## Mistake / Insight
If the array is fully descending, the next permutation is the fully ascending one.

## Status (❌/⚠️/✅)
✅

## Similar Problems
Previous Permutation  
Kth Permutation  
Generate All Permutations  
Permutations II

## Tags
array, greedy, permutation, two-pointers, lexicographical
