## One-Liner Summary
Place positive numbers at even indices and negative numbers at odd indices to form a stable alternating array.

## Pattern
Index Mapping | Two Pointers | Stable Rearrangement

## Key Trick
Reserve even indices for positives and odd indices for negatives.

## Mistake / Insight
Mistake: Trying in-place swaps which break relative order.
Insight: Deterministic index stepping by 2 preserves stability automatically.

## Status
✅

## Similar Problems
Rearrange by Parity  
Sort Array by Sign  
Alternate Positive and Negative

## Tags
array, greedy, indexing, stable
