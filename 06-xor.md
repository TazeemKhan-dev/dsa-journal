# DSA Journal – Prefix Sum

## 🧠 When to Think About XOR
- Subarray XOR equals K (use prefix XOR + HashMap)
- Longest subarray with XOR K
- Count of subarrays with XOR pattern
- XOR-based reversibility: a ^ b = c → a = b ^ c
- Bitwise tricks / toggling / parity problems
- Maximum XOR subarray (Trie required)
- XOR prefix queries

**Tag Guide:** xor, prefix-xor, hashmap, bitwise, reversible-logic, trie-compatible


---
### Q98: Count Subarrays with Given XOR K

- **Pattern:**  
  Prefix XOR + HashMap (frequency of prefix XORs)

- **Key Trick:**  
  Maintain a running prefix XOR.  
  For each index, if `(xor ^ k)` exists in the map, then all previous occurrences of `(xor ^ k)` represent valid subarrays ending at the current index.  
  This uses the XOR identity:  
  `subarrayXor = prefixXor[i] ^ prefixXor[j]`  
  HashMap stores frequencies so multiple matching subarrays are counted correctly.

- **Mistake:**  
  I forgot to insert the base case `map.put(0, 1)` which is required for subarrays starting at index 0.  
  Also initially forgot that the correct check is `xor ^ k`, not comparing `xor == k` alone — XOR needs reversal to find previous matching prefix.

- **Identify Similar Problems:**  
  - Count subarrays with sum = K (prefix sum version of same logic)  
  - Longest subarray with XOR = K  
  - Count subarrays with XOR ≤ K (advanced, trie-based)  
  - Subarray XOR queries using prefix XOR arrays  
  - Any problem where XOR relation `a ^ b = c` is used to reverse compute one operand  

**Tags:** prefix-xor, hashmap, xor-logic, subarray-count, range-xor, reversible-operations

---
### 🔑 LOG — Q177 Find Repeating & Missing Number

- **Pattern:** Prefix math / XOR / Frequency counting  
- **Key Trick:** repeated - missing = sumDiff, repeated + missing = sqDiff/sumDiff  
- **Mistake to Avoid:** Using simple (expectedSum - actualSum) → fails when one value appears twice  
- **Correct Flow:** compute math or XOR → isolate repeating & missing  
- **Similar Problems:**  
  * Missing number (single missing)  
  * Find duplicate in array  
  * Multiple missing / multiple duplicates  
- **Tags:** Math, XOR, HashMap, Arrays, Number properties
