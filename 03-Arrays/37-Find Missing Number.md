## One-Liner Summary
Find the missing number from range [0, n] using either sum formula or XOR cancellation.

## Pattern
Math Invariant | Bitwise XOR | Counting

## Key Trick
XOR all indices and all values together — duplicates cancel, missing survives.

## Mistake / Insight
Mistake: Using extra space or sorting unnecessarily.
Insight: XOR avoids overflow and is the safest optimal method.

## Status
✅

## Similar Problems
Find Two Missing Numbers  
Single Number (XOR)  
Missing Number in Range [1, n]

## Tags
array, math, xor, bitwise, invariant
