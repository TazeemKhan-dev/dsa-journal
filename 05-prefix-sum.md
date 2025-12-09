# DSA Journal – Prefix Sum

## 🧠 When to Think About Prefix Sum
- Subarray sum equals K
- Count subarrays with sum K
- Sum divisible by K (prefix % k)
- Longest/shortest subarray with given sum
- Negative numbers allowed → sliding window fails

---

## 📝 Journal Entry Template

### Problem Name

- **Pattern:**  
- **Key Trick:**  
- **Mistake:**  
- **Identify Similar Problems:**  

---
### Q96: Longest Subarray with Sum K

- **Pattern:**  
  Prefix Sum + HashMap (first occurrence tracking)

- **Key Trick:**  
  Maintain a running prefix sum.  
  If `sum == k` → subarray from 0 to i is valid.  
  If `(sum - k)` exists in the map → a valid subarray ends at i.  
  Only store the **first occurrence** of each prefix sum to maximize length.

- **Mistake:**  
  Used `contains()` instead of `containsKey()`.  
  Also initially forgot that overwriting prefix sum reduces subarray length — always store FIRST index only.

- **Identify Similar Problems:**  
  - Any problem asking for **longest/shortest/any subarray with a target sum**  
  - Count subarrays with sum = K (same prefix idea, counting instead of length)  
  - Subarray sum divisible by K (prefix % k logic)  
  - Longest subarray with sum ≤ K (variant of sliding window + prefix tricks)  
  - Subarrays with given XOR (prefix XOR works the same way)

---

