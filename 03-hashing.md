# DSA Journal – Hashing

## 🧠 When to Think About Hashing
- Need O(1) lookup, frequency, or grouping
- Detect duplicates, missing numbers
- Check existence of complement (Two-sum, etc.)
- Longest consecutive sequences
- Mapping values → indices or frequencies

---
### Q95 — Longest Consecutive Sequence

- **Pattern:**  
  HashSet (sequence-start detection)

- **Key Trick:**  
  If `num - 1` is *not* in the set, then the number is the **start of a consecutive chain**.  
  Expand only forward (`num + 1`, `num + 2`, …).  
  This ensures each sequence is counted exactly once → true `O(n)`.

- **Mistake:**  
  Initially used sorting (`O(n log n)`).  
  Also tried counting from every number instead of only sequence starts → unnecessary extra work.

- **Identify Similar Problems:**  
  - Longest band / chain / run  
  - Range merging problems  
  - Any “longest consecutive integers” problem  
  - Problems where HashSet is used for existence checking  

**Tags:** hashing, hashset, consecuitve-sequence, range-merge, array-set, O(n)-scan

---
