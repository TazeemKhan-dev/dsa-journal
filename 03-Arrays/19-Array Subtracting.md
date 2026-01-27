## One-Liner Summary
Subtract two numbers stored as digit arrays by simulating elementary-school subtraction with borrow from right to left.

## Pattern
Digit-wise simulation  
Borrow propagation  
Reverse construction

## Key Trick
At each position:
    Subtract current digits and existing borrow  
    If result is negative, add 10 and set borrow to 1  
    Store the resulting digit

## Mistake / Insight
Mistake  
Forgetting to handle borrow before subtracting the second array digit.

Insight  
The borrow must be applied first to arr1 digit, then arr2 is subtracted. This guarantees correct cascading borrow.

## Status
✅

## Similar Problems
Add Arrays  
Multiply Strings  
Plus One  
Subtract Linked List Numbers

## Tags
array  
math  
borrow  
simulation  
digits
