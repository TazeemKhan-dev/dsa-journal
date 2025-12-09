# DSA Journal – Trees
## 🧠 When to Think About Trees + DFS
- Parent-child hierarchical relationships  
- Compute number of nodes under each node  
- Path-sum, depth, height, diameter  
- Any problem that resembles “organizational hierarchy”  
- Postorder DFS where child results combine at parent  
- Tree DP (subtree values aggregated via DFS)

**Tag Guide:** dfs, tree, subtree, hierarchy, postorder, graph-traversal, memoization

---
### Q166: Employees and Manager

- **Pattern:**  
  DFS on Tree (subtree size computation)

- **Key Trick:**  
  Convert employee→manager mapping into a tree where the CEO is the root.  
  Use DFS to compute the size of each subtree.  
  The number of employees under any manager = subtree_size - 1.  
  Memoization ensures each subtree is computed once.

- **Mistake:**  
  Initially re-traversed subtrees multiple times (O(N²) approach).  
  Also missed separating "return subtree size" from "store report count".

- **Identify Similar Problems:**  
  - Count nodes in each subtree of a tree  
  - Number of descendants of each node  
  - Company hierarchy / organizational chart problems  
  - Tree DP (postorder traversal computing values)  
  - Sum of subtree values (same DFS pattern)  

**Tags:** dfs, tree, hierarchy, subtree-size, adjacency-list, memoization, graph-traversal

---
