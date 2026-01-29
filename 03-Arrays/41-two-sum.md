## One-Liner Summary
Use the complement formula (target - current) with a HashMap to find the pair in one pass.

## Pattern
Hashing | Complement Search | One-Pass Lookup

## Key Trick
Transform a pair problem into a single lookup using:
complement = target - nums[i]

## Mistake / Insight
Mistake: Insert into map before checking → may reuse same index.
Insight: Always check complement first, then insert current.

## Status
✅

## Similar Problems
Two Sum II (sorted array)  
Three Sum  
Four Sum  
Subarray Sum Equals K

## Tags
array, hashmap, complement, algebra, lookup
