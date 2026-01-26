# 📝 DSA LOG — Q177: Roll Number Problem (Missing & Repeating)

**One-Liner Summary:**  
Find the one number that appears twice and the one number that is missing in an array containing numbers from `1` to `N`.

**Pattern:**  
Math equations, XOR cancellation, frequency counting.

**Key Trick:**  
Use the imbalance created by one extra and one missing value:
- **Math:**  
  `x - y` from sum difference and `x + y` from square-sum difference.
- **XOR:**  
  All correct numbers cancel → left with `repeating ⊕ missing`.  
  Use the **rightmost set bit** to separate them.

**Mistake to Avoid:**  
- Using `*=` instead of `+=` for sum of squares  
- Not casting to `long` before multiplication (overflow)  
- Forgetting to determine which XOR bucket is the repeating number  
- Assuming `missing = expectedSum - actualSum` when duplicates exist  

**Approaches:**  
- HashMap counting → `O(N)` time, `O(N)` space  
- Math formula (sum & square sum) → `O(N)` time, `O(1)` space  
- XOR partitioning → `O(N)` time, `O(1)` space (overflow-safe)

**Similar Problems:**  
- Set Mismatch  
- Missing Number  
- Find Duplicate Number  
- Find All Missing Numbers  
- XOR partition problems  

**Tags:**  
`Math`, `XOR`, `Bit Manipulation`, `Arrays`, `Hashing`, `Constant Space`
