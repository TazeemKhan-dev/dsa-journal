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
### Q: Employees and Manager — Count Employees Under Each Manager

- **Pattern:**  
  DFS on Tree (postorder subtree-size computation)

- **Key Trick:**  
  Convert the `employee → manager` map into an adjacency list (`manager → direct reports`).  
  Identify the CEO (`employee == manager`).  
  DFS returns **subtree size including self**, but store **subtree size − 1** as the total employees under that manager.

- **Mistake Avoided:**  
  Not confusing:  
  - **DFS return value** = total subtree size (including the node)  
  - **Stored result** = total employees under the manager (excluding self)

- **Identify Similar Problems:**  
  - Count descendants in each subtree  
  - Organization chart queries  
  - Tree DP: computing subtree sums  
  - Counting nodes in a subtree  
  - Any postorder DFS aggregation problems  

**Tags:** dfs, tree, hierarchy, subtree-size, adjacency-list, tree-dp, postorder
