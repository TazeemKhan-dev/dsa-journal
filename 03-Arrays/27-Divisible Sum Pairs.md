## One-Liner Summary
Count all index pairs (i, j) such that the sum of elements is divisible by k using modulo complement frequency.

## Pattern
Hashing | Prefix Frequency | Modulo Arithmetic

## Key Trick
Instead of checking all pairs, count how many times the complementary remainder has appeared so far.

## Mistake / Insight
Mistake: Using nested loops for large n.
Insight: If (a+b) % k == 0, then b must be the modulo complement of a.

## Status
✅

## Similar Problems
Subarray Sum Divisible by k  
Two Sum (modulo variant)  
Count Pairs with Given Sum

## Tags
array, hashing, modulo, counting
