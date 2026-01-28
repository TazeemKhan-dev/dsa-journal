## One-Liner Summary
Count subarrays whose sum is divisible by k using prefix sums and matching modulo frequencies.

## Pattern
Prefix Sum | HashMap | Modulo Arithmetic

## Key Trick
If two prefix sums have the same modulo k, the subarray between them has sum divisible by k.

## Mistake / Insight
Mistake: Checking every subarray with nested loops.
Insight: Convert the problem into counting pairs of equal prefix-sum remainders.

## Status
✅

## Similar Problems
Subarray Sum Equals K  
Continuous Subarray Sum  
Count Subarrays with Given Modulo

## Tags
array, prefix-sum, hashmap, modulo, subarray
