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
### Q165: Missing Numbers

- **Pattern:**  
  HashMap Frequency Comparison (multiset difference)

- **Key Trick:**  
  Count frequencies in both arrays and compare them.  
  A number is considered “missing” if:  
  - It appears more times in `brr` than in `arr`, or  
  - It appears in `brr` but not in `arr`.  
  Only add each number once and sort the final list.

- **Mistake:**  
  Initially forgot to check **frequency difference**, not just element existence.  
  Also missed the case where an element exists in both arrays but appears **fewer times** in `arr`.

- **Identify Similar Problems:**  
  - Compare two multisets or lists  
  - Find extra numbers in an array  
  - Check mismatched frequencies between two datasets  
  - Missing numbers in a given range (variation)  
  - Count differences between two frequency maps  

**Tags:** hashing, frequency-map, multiset-difference, array-comparison, sorting-required

---

# 📝 DSA LOG — Q170: Problem With Given Difference

**One-Liner Summary:**  
Check if any two numbers differ by exactly `B` using hashing or two pointers.

**Pattern:**  
Difference problems, hashing lookup, two-pointer on sorted array.

**Key Trick:**  
For every `x`, check:  
- `x + B` exists  
- `x - B` exists  
(Handles absolute difference naturally.)  
If `B == 0`, check for duplicates.

**Mistake to Avoid:**  
- Forgetting absolute difference  
- Not handling `B = 0`  
- Two pointers overlapping (`i == j`)  
- Using O(N²) on N=100000 arrays  

**Approaches:**  
- Brute Force → O(N²)  
- Two Pointers (after sort) → O(N log N)  
- HashSet (best) → O(N)

**Similar Problems:**  
- Two Sum  
- Pair With Given Sum  
- Count pairs with difference K  
- Duplicate within K distance

**Tags:**  
`Hashing`, `Two Pointers`, `Arrays`, `Difference`, `Searching`

# 📝 DSA LOG — Q171: Array Pairs Divisible By K

**One-Liner Summary:**  
Check if all elements can be paired such that each pair’s sum is divisible by `k`.

**Pattern:**  
Remainder pairing, modular arithmetic, frequency matching.

**Key Trick:**  
Use remainder frequencies:  
- r pairs with k-r  
- Special cases:  
  - remainder 0 → count must be even  
  - remainder k/2 (when k even) → count must be even  

**Mistake to Avoid:**  
- Not normalizing negative remainders  
- Forgetting special case `k % 2 == 0`  
- Directly using sorting / two pointers (doesn’t work here)  
- Checking only freq[r] but not freq[k-r]

**Approaches:**  
- Remainder frequency array (O(n + k))  
- HashMap version (slower but same logic)

**Similar Problems:**  
- Check if array can be paired with difference k  
- Pairs divisible by 60 (LeetCode bikes problem)  
- Count pairs divisible by k  
- Pair sum constraints with modular arithmetic  

**Tags:**  
`Hashing`, `Math`, `Remainders`, `Arrays`, `Modulo`, `Pairing`

# 📝 DSA LOG — Q172: Largest Subarray with 0 Sum

**One-Liner Summary:**  
Find the longest contiguous segment where the sum equals zero using prefix sums + hashmap.

**Pattern:**  
Prefix sum, hashmap, subarray sum equals target.

**Key Trick:**  
If a prefix sum repeats, the subarray between indices cancels to zero.  
Store only the *earliest* occurrence of each prefix sum to maximize length.

**Mistake to Avoid:**  
- Forgetting to check when prefix sum itself becomes zero  
- Overwriting prefix sum entries in the map  
- Using brute force on large arrays  
- Not handling negative numbers (prefix logic works fine)

**Approaches:**  
- Brute Force O(N²)  
- Prefix Sum + HashMap O(N) (optimal)

**Similar Problems:**  
- Longest subarray with sum = K  
- Count subarrays with sum = 0  
- Largest subarray divisible by K  
- Subarray sum equals target (LeetCode)

**Tags:**  
`Hashing`, `Prefix Sum`, `Subarrays`, `Arrays`, `Zero Sum`

### 🔑 LOG — Q173 Group Anagrams

- **Pattern:** HashMap grouping + Custom sorting rule  
- **Key Trick:** Sort groups by *first encountered word*, not by anagram key  
- **Mistake to Avoid:** Sorting using sorted-key (like "act", "aet") → WRONG order  
- **Correct Flow:** build groups → record first word → sort groups by firstWord → print in input order  
- **Similar Problems:**  
  * Group Anagrams (LeetCode 49)  
  * Word Frequency Hashing  
  * Custom Sorting by Metadata  
- **Tags:** HashMap, Strings, Sorting, Anagrams, Custom Comparator

### 🔑 LOG — Q176 Count Number of Pairs With Absolute Difference K

- **Pattern:** HashMap frequency + HashSet uniqueness  
- **Key Trick:** Separate cases → k = 0 (freq ≥ 2), k > 0 (check x + k)  
- **Mistake to Avoid:** Checking both (x + k) and (x - k) → double counts  
- **Correct Flow:** build freq → if k=0 count repeats → else check unique keys  
- **Similar Problems:**  
  * Count pairs with sum K  
  * Two-sum variations  
  * Count distinct value pairs  
- **Tags:** HashMap, HashSet, Differences, Unordered Pairs, Frequency counting

### 🔑 LOG — Q176 Count Number of Pairs With Absolute Difference K

- **Pattern:** HashMap frequency + HashSet uniqueness  
- **Key Trick:** Separate cases → k = 0 (freq ≥ 2), k > 0 (check x + k)  
- **Mistake to Avoid:** Checking both (x + k) and (x - k) → double counts  
- **Correct Flow:** build freq → if k=0 count repeats → else check unique keys  
- **Similar Problems:**  
  * Count pairs with sum K  
  * Two-sum variations  
  * Count distinct value pairs  
- **Tags:** HashMap, HashSet, Differences, Unordered Pairs, Frequency counting
