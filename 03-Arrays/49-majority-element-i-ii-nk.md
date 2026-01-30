## One-Liner Summary
Find elements appearing more than n/2, n/3, or n/k times using elimination (Boyer–Moore voting).

## Pattern
Frequency threshold, elimination, voting algorithm.

## Key Trick
At most (k−1) elements can exceed n/k, so maintain only (k−1) candidates and cancel others.

## Mistake / Insight
Always verify candidates for n/3 and n/k; elimination alone can give false positives.

## Status (❌/⚠️/✅)
✅

## Similar Problems
Top K Frequent Elements  
Frequent Elements in Stream  
Majority in Sliding Window  
Mode of Array

## Tags
array, boyer-moore, voting, frequency, math, greedy
