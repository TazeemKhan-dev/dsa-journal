## One-Liner Summary
Use two pointers to overwrite duplicates in-place while preserving order, allowing either one or at most two occurrences.

## Pattern
Two Pointers | In-place Array | Sliding Write Window

## Key Trick
Leverage sorted order: compare current element with the element `k` positions behind the write pointer.

## Mistake / Insight
Mistake: Using extra space or hashing for a sorted array.
Insight: Sorted order guarantees duplicates are adjacent, so simple index comparison is enough.

## Status
✅

## Similar Problems
Remove Element  
Move Zeroes  
Deduplicate Linked List

## Tags
array, two-pointers, in-place, deduplication
