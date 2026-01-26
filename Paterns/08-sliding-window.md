# DSA Journal – Sliding Window
## 🧠 When to Think About Sliding Window
- “Longest/shortest substring/subarray …”
- Window grows/shrinks based on condition
- All elements are non-negative (classic window)
- Character-based windows (frequency maps)
- Fixed-size vs variable-size windows


---

# 📝 DSA LOG — Q179: Minimum Window Substring

**One-Liner Summary:**  
Find the smallest substring of `s` that contains all characters of `t` (including duplicates) using a sliding window.

**Pattern:**  
Sliding Window (expand → validate → shrink), frequency counting.

**Key Trick:**  
- Maintain two maps:  
  - `need` → required frequency from `t`  
  - `window` → current window frequency  
- Use a **count** variable to track how many characters of `t` are satisfied.
- Expand with `right`, shrink with `left` **using `while`**, not `if`.

**Mistake to Avoid:**  
- Shrinking with `if` instead of `while` (won’t minimize window fully)  
- Using `start` instead of `left` while computing window length  
- Using `<=` while decrementing count during shrink  
- Checking only presence instead of frequency  
- Forgetting `t.length() > s.length()` edge case  

**Approaches:**  
- Brute Force → `O(N^3)` (check all substrings, TLE)  
- Sliding Window + HashMap → `O(N)` time, `O(K)` space (optimal)

**Similar Problems:**  
- Longest Substring Without Repeating Characters  
- Longest Substring with At Most K Distinct Characters  
- Substring Containing All Vowels  
- Smallest Window Containing All Distinct Characters  

**Tags:**  
`Sliding Window`, `HashMap`, `Two Pointers`, `Strings`, `Frequency Counting`
---

# 📝 DSA LOG — Q180: Distinct Window (Smallest Substring with All Distinct Characters)

**One-Liner Summary:**  
Find the smallest substring of a string that contains **all distinct characters present in the entire string** at least once.

**Pattern:**  
Sliding Window (expand → validate → shrink), two pointers, frequency tracking.

**Key Trick:**  
- First compute the **number of distinct characters** in the full string (`required`).
- While expanding the window, increase `formed` **only when a character’s frequency becomes 1**.
- Shrink the window while `formed == required` to minimize length.
- Decrease `formed` **only when a character’s frequency drops to 0** during shrink.

**Mistake to Avoid:**  
- Treating this like classic *Minimum Window Substring* with frequency requirements (here, frequency = 1 is enough).  
- Forgetting to precompute the total number of distinct characters in `s`.  
- Shrinking with `if` instead of `while`.  
- Decreasing `formed` when frequency becomes `>= 1` instead of exactly `0`.

**Approaches:**  
- Brute Force → `O(N^3)` (generate substrings + check distinct coverage).  
- Sliding Window + HashMap → `O(N)` time, `O(K)` space (optimal), where `K` = distinct characters.

**Similar Problems:**  
- Minimum Window Substring  
- Longest Substring with All Distinct Characters  
- Longest Substring with At Most K Distinct Characters  
- Substring Containing All Vowels  

**Tags:**  
`Sliding Window`, `Two Pointers`, `Strings`, `HashMap`, `Frequency Counting`
---

# 📝 DSA LOG — Q181: Substring With K Unique Characters

**One-Liner Summary:**  
Find the length of the longest substring that contains **exactly `k` distinct characters** using a sliding window.

**Pattern:**  
Sliding Window (two pointers), frequency HashMap, window size optimization.

**Key Trick:**  
- Maintain a HashMap to track character frequencies in the current window.
- `map.size()` directly represents the number of unique characters.
- Expand the window with `right`.
- Shrink from `left` **only when `map.size() > k`**.
- Update the answer **only when `map.size() == k`**.

**Mistake to Avoid:**  
- Updating the answer when `map.size() < k` (this is **exactly k**, not at most k).  
- Forgetting to remove a character from the map when its frequency becomes `0`.  
- Confusing this with the “at most k distinct characters” problem.  
- Returning `0` instead of `-1` when no valid substring exists.  

**Approaches:**  
- Brute Force → `O(N^3)` (generate substrings + count unique each time).  
- Sliding Window + HashMap → `O(N)` time, `O(K)` space (optimal).

**Similar Problems:**  
- Longest Substring with At Most K Distinct Characters  
- Longest Substring with All Distinct Characters  
- Distinct Window (smallest substring with all distinct chars)  
- Minimum Window Substring  

**Tags:**  
`Sliding Window`, `Two Pointers`, `Strings`, `HashMap`, `Distinct Characters`

---
