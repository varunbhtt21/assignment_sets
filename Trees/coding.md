# Trees - Coding Problems

---

## Problem 1: Hierarchical Data Level Scanner

**Difficulty:** Medium
**Company:** LinkedIn, Microsoft, Amazon

### Problem Statement

A social network platform needs to analyze user connections in a hierarchical structure. Given the `root` of a binary tree, return the level order traversal of its nodes' values (i.e., from left to right, level by level).

Level order traversal visits all nodes at the current level before moving to the next level.

### Input Format
- The root node of a binary tree

### Output Format
- Return a list of lists, where each inner list contains node values at that level

### Constraints
- The number of nodes in the tree is in the range `[0, 2000]`
- `-1000 <= Node.val <= 1000`

### Examples

**Example 1:**
```
Input: root = [3,9,20,null,null,15,7]
Output: [[3],[9,20],[15,7]]
```

**Example 2:**
```
Input: root = [1]
Output: [[1]]
```

**Example 3:**
```
Input: root = []
Output: []
```

### Test Cases

#### Test Case 1
**Input:**
```
[3,9,20,null,null,15,7]
```
**Output:**
```
[[3],[9,20],[15,7]]
```
**Explanation:** Level 0: [3], Level 1: [9,20], Level 2: [15,7].

---

#### Test Case 2
**Input:**
```
[1]
```
**Output:**
```
[[1]]
```
**Explanation:** Single node tree has only one level.

---

#### Test Case 3
**Input:**
```
[]
```
**Output:**
```
[]
```
**Explanation:** Empty tree returns empty list.

---

#### Test Case 4
**Input:**
```
[1,2,3,4,5]
```
**Output:**
```
[[1],[2,3],[4,5]]
```
**Explanation:** Complete binary tree with 3 levels.

---

#### Test Case 5
**Input:**
```
[1,2,null,3,null,4]
```
**Output:**
```
[[1],[2],[3],[4]]
```
**Explanation:** Left-skewed tree, each level has one node.

---

#### Test Case 6
**Input:**
```
[1,null,2,null,3,null,4]
```
**Output:**
```
[[1],[2],[3],[4]]
```
**Explanation:** Right-skewed tree, each level has one node.

---

#### Test Case 7
**Input:**
```
[5,3,8,1,4,7,9]
```
**Output:**
```
[[5],[3,8],[1,4,7,9]]
```
**Explanation:** Complete binary tree: Level 0: [5], Level 1: [3,8], Level 2: [1,4,7,9].

---

#### Test Case 8
**Input:**
```
[1,2,3,4,null,null,5]
```
**Output:**
```
[[1],[2,3],[4,5]]
```
**Explanation:** Level 0: [1], Level 1: [2,3], Level 2: [4,5].

---

#### Test Case 9
**Input:**
```
[10,5,15,3,7,null,18]
```
**Output:**
```
[[10],[5,15],[3,7,18]]
```
**Explanation:** Three levels with varying number of nodes per level.

---

#### Test Case 10
**Input:**
```
[1,2,3,null,null,4,5,null,null,6,7]
```
**Output:**
```
[[1],[2,3],[4,5],[6,7]]
```
**Explanation:** Four-level tree: [[1],[2,3],[4,5],[6,7]].

---

## Problem 2: BST Rank Finder

**Difficulty:** Medium
**Company:** Uber, Google, Amazon

### Problem Statement

A database indexing system uses Binary Search Trees for efficient data retrieval. Given the `root` of a binary search tree and an integer `k`, return the k-th smallest value (1-indexed) of all the values of the nodes in the tree.

### Input Format
- First line: Root node of a binary search tree
- Second line: Integer `k`

### Output Format
- Return an integer representing the k-th smallest element

### Constraints
- The number of nodes in the tree is `n`
- `1 <= k <= n <= 10^4`
- `0 <= Node.val <= 10^4`

### Examples

**Example 1:**
```
Input: root = [3,1,4,null,2], k = 1
Output: 1
```

**Example 2:**
```
Input: root = [5,3,6,2,4,null,null,1], k = 3
Output: 3
```

### Test Cases

#### Test Case 1
**Input:**
```
root = [3,1,4,null,2]
k = 1
```
**Output:**
```
1
```
**Explanation:** In-order traversal: [1,2,3,4]. The 1st smallest is 1.

---

#### Test Case 2
**Input:**
```
root = [5,3,6,2,4,null,null,1]
k = 3
```
**Output:**
```
3
```
**Explanation:** In-order traversal: [1,2,3,4,5,6]. The 3rd smallest is 3.

---

#### Test Case 3
**Input:**
```
root = [1]
k = 1
```
**Output:**
```
1
```
**Explanation:** Single node, k=1 returns that node's value.

---

#### Test Case 4
**Input:**
```
root = [2,1,3]
k = 2
```
**Output:**
```
2
```
**Explanation:** In-order: [1,2,3]. The 2nd smallest is 2.

---

#### Test Case 5
**Input:**
```
root = [5,3,6,2,4,null,null,1]
k = 1
```
**Output:**
```
1
```
**Explanation:** The smallest element in the BST is 1.

---

#### Test Case 6
**Input:**
```
root = [5,3,6,2,4,null,null,1]
k = 6
```
**Output:**
```
6
```
**Explanation:** In-order: [1,2,3,4,5,6]. The 6th smallest (largest) is 6.

---

#### Test Case 7
**Input:**
```
root = [10,5,15,3,7,12,20]
k = 4
```
**Output:**
```
10
```
**Explanation:** In-order: [3,5,7,10,12,15,20]. The 4th smallest is 10.

---

#### Test Case 8
**Input:**
```
root = [4,2,6,1,3,5,7]
k = 3
```
**Output:**
```
3
```
**Explanation:** In-order: [1,2,3,4,5,6,7]. The 3rd smallest is 3.

---

#### Test Case 9
**Input:**
```
root = [8,3,10,1,6,null,14,null,null,4,7,13]
k = 5
```
**Output:**
```
7
```
**Explanation:** In-order: [1,3,4,6,7,8,10,13,14]. The 5th smallest is 7.

---

#### Test Case 10
**Input:**
```
root = [20,10,30,5,15,25,35]
k = 7
```
**Output:**
```
35
```
**Explanation:** In-order: [5,10,15,20,25,30,35]. The 7th smallest is 35.

---

## Problem 3: Left Branch Sum Calculator

**Difficulty:** Easy
**Company:** Grammarly, Facebook, Microsoft

### Problem Statement

A financial system tracks expenses in a tree structure where left branches represent specific categories. Given the `root` of a binary tree, return the sum of all left leaves.

A leaf is a node with no children. A left leaf is a leaf that is the left child of another node.

### Input Format
- The root node of a binary tree

### Output Format
- Return an integer representing the sum of all left leaves

### Constraints
- The number of nodes in the tree is in the range `[1, 1000]`
- `-1000 <= Node.val <= 1000`

### Examples

**Example 1:**
```
Input: root = [3,9,20,null,null,15,7]
Output: 24
Explanation: There are two left leaves: 9 and 15. Sum = 9 + 15 = 24.
```

**Example 2:**
```
Input: root = [1]
Output: 0
```

### Test Cases

#### Test Case 1
**Input:**
```
[3,9,20,null,null,15,7]
```
**Output:**
```
24
```
**Explanation:** Left leaves are 9 and 15. Sum = 9 + 15 = 24.

---

#### Test Case 2
**Input:**
```
[1]
```
**Output:**
```
0
```
**Explanation:** Single node with no children is not a left leaf.

---

#### Test Case 3
**Input:**
```
[1,2,3]
```
**Output:**
```
2
```
**Explanation:** Node 2 is a left leaf. Sum = 2.

---

#### Test Case 4
**Input:**
```
[1,2,3,4,5]
```
**Output:**
```
4
```
**Explanation:** Only node 4 is a left leaf (left child of 2, and has no children).

---

#### Test Case 5
**Input:**
```
[5,3,8,1,4,7,9]
```
**Output:**
```
8
```
**Explanation:** Left leaves are 1 and 7. Sum = 1 + 7 = 8.

---

#### Test Case 6
**Input:**
```
[1,2,null,3,null,4]
```
**Output:**
```
4
```
**Explanation:** Node 4 is a left leaf. Sum = 4.

---

#### Test Case 7
**Input:**
```
[10,5,15,3,7,null,18]
```
**Output:**
```
3
```
**Explanation:** Only node 3 is a left leaf. Sum = 3.

---

#### Test Case 8
**Input:**
```
[1,2,3,null,4,null,5]
```
**Output:**
```
0
```
**Explanation:** Nodes 4 and 5 are leaves but neither is a left child of its parent.

---

#### Test Case 9
**Input:**
```
[6,4,8,2,5,7,9,1,3]
```
**Output:**
```
8
```
**Explanation:** Left leaves are 1 and 7. Sum = 1 + 7 = 8.

---

#### Test Case 10
**Input:**
```
[20,10,30,5,15,25,35,null,null,12]
```
**Output:**
```
42
```
**Explanation:** Left leaves are 5, 12, and 25. Sum = 5 + 12 + 25 = 42.

---

## Problem 4: Nearest Leaf Distance Finder

**Difficulty:** Medium
**Company:** Amazon, Google, Microsoft

### Problem Statement

A network routing system needs to find the closest terminal node from any given point. Given the `root` of a binary tree where every node has a unique value and a target integer `k`, return the value of the nearest leaf node to the target `k` in the tree.

Nearest to a leaf means the least number of edges traveled on the binary tree to reach any leaf of the tree. Also, a node is called a leaf if it has no children.

### Input Format
- First line: Root node of a binary tree
- Second line: Target integer `k`

### Output Format
- Return an integer representing the value of the nearest leaf node

### Constraints
- The number of nodes in the tree is in the range `[1, 1000]`
- `1 <= Node.val <= 1000`
- All the values of the tree are unique
- There exists some node in the tree where `Node.val == k`

### Examples

**Example 1:**
```
Input: root = [1,3,2], k = 1
Output: 2
Explanation: Either 2 or 3 is the nearest leaf node to target 1.
```

**Example 2:**
```
Input: root = [1], k = 1
Output: 1
Explanation: The nearest leaf node is the root itself.
```

**Example 3:**
```
Input: root = [1,2,3,4,null,null,null,5,null,6], k = 2
Output: 3
Explanation: The leaf node with value 3 (not 6) is nearest to node 2.
```

### Test Cases

#### Test Case 1
**Input:**
```
root = [1,3,2]
k = 1
```
**Output:**
```
2
```
**Explanation:** From node 1, leaves 3 and 2 are both at distance 1. Can return either (returning 2).

---

#### Test Case 2
**Input:**
```
root = [1]
k = 1
```
**Output:**
```
1
```
**Explanation:** The root itself is a leaf and is the nearest.

---

#### Test Case 3
**Input:**
```
root = [1,2,3,4,null,null,null,5,null,6]
k = 2
```
**Output:**
```
3
```
**Explanation:** Leaf 3 is 2 edges away from node 2, while leaf 6 is 3 edges away.

---

#### Test Case 4
**Input:**
```
root = [1,2,3]
k = 2
```
**Output:**
```
2
```
**Explanation:** Node 2 itself is a leaf, distance 0.

---

#### Test Case 5
**Input:**
```
root = [1,2,3,4,5]
k = 1
```
**Output:**
```
4
```
**Explanation:** Leaves 4 and 5 are both at distance 2 from node 1. Can return either.

---

#### Test Case 6
**Input:**
```
root = [5,3,6,2,4,null,null,1]
k = 3
```
**Output:**
```
1
```
**Explanation:** From node 3, leaf 1 is at distance 2, leaves 4 and 6 are farther.

---

#### Test Case 7
**Input:**
```
root = [10,5,15,3,7,null,18]
k = 5
```
**Output:**
```
3
```
**Explanation:** From node 5, leaves 3 and 7 are both at distance 1. Can return either.

---

#### Test Case 8
**Input:**
```
root = [1,2,3,4,5,6,7]
k = 4
```
**Output:**
```
4
```
**Explanation:** Node 4 itself is a leaf.

---

#### Test Case 9
**Input:**
```
root = [8,3,10,1,6,null,14,null,null,4,7,13]
k = 6
```
**Output:**
```
4
```
**Explanation:** From node 6, leaves 4 and 7 are at distance 1. Can return either.

---

#### Test Case 10
**Input:**
```
root = [20,10,30,5,15,25,35]
k = 20
```
**Output:**
```
5
```
**Explanation:** From root 20, all four leaves (5,15,25,35) are at distance 2. Can return any.

---

**End of Coding Problems**
