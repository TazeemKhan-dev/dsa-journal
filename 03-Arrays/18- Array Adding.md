## One-Liner Summary
Add two numbers stored as digit arrays by simulating elementary-school addition from right to left with carry.

## Pattern
Digit-wise simulation  
Carry propagation  
Reverse construction

## Key Trick
Store `sum % 10` as the current digit and propagate `sum / 10` as carry, while traversing from the last index of both arrays.

## Mistake / Insight
Mistake  
Forgetting that digits are collected in reverse order and returning them without reversing.

Insight  
The exact sequence matters:  
    First store `sum % 10` into result  
    Then move `sum / 10` into carry  
This guarantees correct digit extraction and carry flow.

## Status
✅

## Similar Problems
Add Two Numbers (Linked List)  
Multiply Strings  
Plus One  
Subtract Arrays

## Tags
array  
math  
carry  
simulation  
digits
