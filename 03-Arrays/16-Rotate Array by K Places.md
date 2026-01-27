## 🧠 One-Liner Summary
Rotate an array left or right by k positions while preserving the order of elements.

## 🧩 Pattern
Array manipulation, index mapping, reversal technique.

## 🔑 Key Trick
Either map each element to its new index using `(i ± k) % n` or use the 3-step reverse trick to rotate in-place.

## ⚠️ Mistake / Insight
I remembered the reverse method but forgot the brute-force index mapping formula `(i ± k) % n`, which is the foundation of rotation.

## 🧠 Why I Got Stuck
I knew the optimal trick but couldn’t derive it because I hadn’t connected it back to the basic “shift by 1, k times” idea.

## 📌 Status
⚠️

## 🔁 Similar Problems
Rotate Linked List by k  
Cyclic Rotation  
Reversal Algorithm for Array Rotation  
LeetCode 189 – Rotate Array  

## 🏷️ Tags
arrays, rotation, modulo, reversal, index-mapping
