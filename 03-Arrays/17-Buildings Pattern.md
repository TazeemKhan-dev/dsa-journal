## 🧠 One-Liner Summary
Print a skyline where each array value represents the height of a building drawn using `*`.

## 🧩 Pattern
Matrix simulation, row-by-row visualization.

## 🔑 Key Trick
First find the maximum height, then print from top to bottom:  
outer loop goes from `maxHeight` down to `1`, and the inner loop scans every building to decide whether to print `*` or space.

## ⚠️ Mistake / Insight
The crucial part is realizing we don’t build column by column — we simulate the grid row by row starting from the tallest level.

## 🧠 Why I Got Stuck
Initially I thought of printing each building separately, but missed that the pattern requires synchronized row-wise printing across all columns.

## 📌 Status
⚠️

## 🔁 Similar Problems
Histogram printing  
Bar chart using stars  
Rainwater trapping visualization  
Matrix-based pattern problems  

## 🏷️ Tags
arrays, pattern-printing, simulation, loops, visualization
