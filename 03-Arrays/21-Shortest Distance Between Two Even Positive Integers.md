## One-Liner Summary
Track indices of even positive numbers during a single scan and keep the minimum distance between consecutive occurrences.

## Pattern
Array | Single Scan | Index Tracking

## Key Trick
The shortest distance can only occur between consecutive even positive elements in traversal order.

## Mistake / Insight
Mistake: Comparing every pair of even elements.
Insight: Once indices are sorted by traversal, checking only consecutive ones is sufficient.

## Status
✅

## Similar Problems
Shortest Distance Between Two Odd Numbers  
Minimum Distance Between Repeated Elements  
Minimum Index Difference in an Array

## Tags
array, greedy, single-pass, index-tracking
