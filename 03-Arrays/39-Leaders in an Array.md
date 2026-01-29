## One-Liner Summary
Find all elements that are greater than every element to their right using a right-to-left suffix maximum scan.

## Pattern
Suffix Maximum | Reverse Traversal | Greedy Scan

## Key Trick
Traverse from the right and keep track of the maximum seen so far.

## Mistake / Insight
Mistake: Checking all elements to the right for every index.
Insight: If nums[i] equals the suffix maximum, it is a leader.

## Status
✅

## Similar Problems
Next Greater Element  
Suffix Maximum Array  
Stock Span Problem

## Tags
array, greedy, suffix, scanning
