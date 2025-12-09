# DSA Journal – Prefix Sum

## 🧠 When to Think About Prefix Sum
- Subarray sum equals K
- Count subarrays with sum K
- Sum divisible by K (prefix % k)
- Longest/shortest subarray with given sum
- Negative numbers allowed → sliding window fails

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
  Also initially forgot that overwriting prefix sum reduces subarray length — always store the FIRST index only.

- **Identify Similar Problems:**  
  - Any problem asking for **longest/shortest/any subarray with a target sum**  
  - Count subarrays with sum = K (same prefix idea, counting instead of length)  
  - Subarray sum divisible by K (prefix % k logic)  
  - Longest subarray with sum ≤ K (variant of sliding window + prefix tricks)  
  - Subarrays with given XOR (prefix XOR works the same way)

**Tags:** prefix-sum, hashmap, longest-subarray, range-sum, negative-numbers, sliding-window-incompatible

---


### Q97: Count Subarrays With Given Sum

- **Pattern:**  
  Prefix Sum + HashMap (frequency map)

- **Key Trick:**  
  Maintain a running prefix sum.  
  If `(prefixSum - k)` exists in the hashmap, it means that many subarrays ending at the current index sum to `k`.  
  Increase count by the **frequency** (not just +1).  
  Always store prefix sum frequencies to allow multiple valid starting points.

- **Mistake:**  
  I incremented count by **1** whenever I found `sum - k`, instead of adding the full frequency from the map.  
  Also, I used an `if` block incorrectly to decide when to store prefix sums — prefix sums must be added to map **every iteration**, not conditionally.

- **Identify Similar Problems:**  
  - Count subarrays with sum divisible by K (same prefix idea with modulo)  
  - Longest subarray with sum K (store first index of prefix sum)  
  - Count subarrays with XOR = K (prefix XOR version of same logic)  
  - Number of subarrays with sum zero  
  - Largest subarray with sum zero  

**Tags:** prefix-sum, hashmap, subarray-count, range-sum, frequency-map

---
