# Trees - MCQ Questions

---

### Q1.

What is a binary tree?

A. A tree where each node has exactly two children

B. A tree where each node has at most two children

C. A tree with only two nodes

D. A tree with two root nodes

**Answer:** B

**Explanation:** A binary tree is a tree data structure where each node has at most two children, referred to as the left child and the right child. Some nodes may have zero, one, or two children.

---

### Q2.

What is the time complexity of searching for an element in a balanced Binary Search Tree (BST)?

A. O(n)

B. O(log n)

C. O(1)

D. O(n²)

**Answer:** B

**Explanation:** In a balanced BST, the height is O(log n), so searching takes O(log n) time as we eliminate half of the remaining nodes at each level by comparing with the current node.

---

### Q3.

What is the in-order traversal sequence of a Binary Search Tree?

A. Random order

B. Descending order

C. Ascending order

D. Level order

**Answer:** C

**Explanation:** In-order traversal (left-root-right) of a BST always produces elements in ascending (sorted) order because of the BST property where left subtree < root < right subtree.

---

### Q4.

What is a leaf node in a tree?

A. The root node

B. A node with exactly one child

C. A node with no children

D. The deepest node

**Answer:** C

**Explanation:** A leaf node is a node that has no children (both left and right pointers are null). It represents the terminal nodes of the tree.

---

### Q5.

What is the maximum number of nodes in a complete binary tree of height h?

A. 2^h

B. 2^h - 1

C. 2^(h+1) - 1

D. h²

**Answer:** C

**Explanation:** A complete binary tree of height h has maximum 2^(h+1) - 1 nodes. For example, height 2 has max 2^3 - 1 = 7 nodes (1 + 2 + 4).

---

### Q6.

Which traversal technique uses a queue data structure?

A. Pre-order traversal

B. In-order traversal

C. Post-order traversal

D. Level-order traversal

**Answer:** D

**Explanation:** Level-order traversal (BFS) uses a queue to visit nodes level by level from left to right. DFS traversals (pre-order, in-order, post-order) use recursion or a stack.

---

### Q7.

What is the height of a tree with a single node?

A. -1

B. 0

C. 1

D. Undefined

**Answer:** B

**Explanation:** By convention, the height of a tree with a single node (just the root) is 0. Height is defined as the number of edges in the longest path from root to a leaf.

---

### Q8.

In a Binary Search Tree, where would you find the minimum value?

A. At the root

B. In the rightmost node

C. In the leftmost node

D. At any leaf node

**Answer:** C

**Explanation:** Due to the BST property (left < root < right), the minimum value is always found by following left pointers until reaching the leftmost node.

---

### Q9.

What is the space complexity of recursive in-order traversal?

A. O(1)

B. O(log n) for balanced trees

C. O(n) in worst case

D. Both B and C

**Answer:** D

**Explanation:** Recursive traversal uses the call stack. For balanced trees, the maximum depth is O(log n). For skewed trees (worst case), it's O(n). So both are correct depending on tree structure.

---

### Q10.

What traversal order is used to evaluate a postfix expression tree?

A. Pre-order

B. In-order

C. Post-order

D. Level-order

**Answer:** C

**Explanation:** Post-order traversal (left-right-root) processes children before the parent, which matches the evaluation order needed for postfix expressions.

---

### Q11.

What defines a valid Binary Search Tree?

A. Left subtree values < root, right subtree values > root

B. All left descendants < root < all right descendants

C. Nodes are in sorted order

D. Height is balanced

**Answer:** B

**Explanation:** A valid BST requires ALL nodes in the left subtree to be less than the root, and ALL nodes in the right subtree to be greater than the root, not just immediate children.

---

### Q12.

What is the time complexity of inserting a node in an unbalanced BST in the worst case?

A. O(1)

B. O(log n)

C. O(n)

D. O(n log n)

**Answer:** C

**Explanation:** In the worst case (completely skewed tree), insertion requires traversing all n nodes to reach the correct position, resulting in O(n) time complexity.

---

### Q13.

Which tree traversal would give you a copy of the tree when combined with the tree structure?

A. Pre-order only

B. In-order only

C. Post-order only

D. Pre-order or Post-order

**Answer:** D

**Explanation:** Pre-order (root-left-right) or post-order (left-right-root) combined with null markers can uniquely reconstruct a tree. In-order alone cannot uniquely determine tree structure.

---

### Q14.

What is a complete binary tree?

A. All levels are completely filled

B. All levels are filled except possibly the last, which is filled from left to right

C. All nodes have two children

D. A balanced binary tree

**Answer:** B

**Explanation:** A complete binary tree has all levels fully filled except possibly the last level, which is filled from left to right without gaps.

---

### Q15.

What is the minimum number of nodes in a binary tree of height h?

A. h

B. h + 1

C. 2^h

D. 2^(h+1) - 1

**Answer:** B

**Explanation:** A skewed tree (like a linked list) with height h has minimum h + 1 nodes (one node per level from 0 to h).

---

### Q16.

How do you check if a binary tree is a valid BST?

A. Check if in-order traversal is sorted

B. Check each node's value against its children only

C. Check if tree is balanced

D. Count the nodes

**Answer:** A

**Explanation:** The most reliable way is to perform in-order traversal and verify the result is in strictly ascending order. Just checking immediate children is insufficient.

---

### Q17.

What is the diameter of a binary tree?

A. The height of the tree

B. The number of nodes in the tree

C. The longest path between any two nodes

D. The number of leaf nodes

**Answer:** C

**Explanation:** The diameter (or width) of a binary tree is the length of the longest path between any two nodes in the tree. This path may or may not pass through the root.

---

### Q18.

What is the time complexity of finding the kth smallest element in a BST using in-order traversal?

A. O(1)

B. O(k)

C. O(n)

D. O(log n)

**Answer:** B

**Explanation:** Using in-order traversal, we can stop after visiting k nodes. In the best case, if k is small, we only visit k nodes, giving O(k) time complexity.

---

### Q19.

Which data structure is used for iterative pre-order traversal?

A. Queue

B. Stack

C. Array

D. Hash Table

**Answer:** B

**Explanation:** Iterative pre-order traversal uses a stack to simulate the recursive call stack. We push right child first, then left child, to ensure left is processed first.

---

### Q20.

What is the lowest common ancestor (LCA) of two nodes in a binary tree?

A. The root node

B. The deepest node that has both nodes as descendants

C. The parent of the first node

D. Any ancestor common to both nodes

**Answer:** B

**Explanation:** The LCA is the lowest (deepest) node in the tree that has both given nodes as descendants. It could be one of the nodes itself if one is an ancestor of the other.

---

### Q21.

How do you find if two binary trees are identical?

A. Check if they have the same number of nodes

B. Check if in-order traversals are the same

C. Recursively check if roots and both subtrees are identical

D. Check if heights are equal

**Answer:** C

**Explanation:** Two trees are identical if: (1) both are null, OR (2) both roots have the same value AND left subtrees are identical AND right subtrees are identical.

---

### Q22.

What is the time complexity of finding the height of a binary tree?

A. O(1)

B. O(log n)

C. O(n)

D. O(n²)

**Answer:** C

**Explanation:** Finding height requires visiting all nodes to determine the maximum depth, resulting in O(n) time complexity where n is the number of nodes.

---

### Q23.

In a binary tree, what is the relationship between number of leaf nodes (L) and number of nodes with 2 children (T) in a full binary tree?

A. L = T

B. L = T + 1

C. L = 2T

D. L = T - 1

**Answer:** B

**Explanation:** In a full binary tree, the number of leaf nodes is always one more than the number of internal nodes with two children: L = T + 1.

---

### Q24.

What is Morris Traversal used for?

A. Faster tree traversal

B. In-order traversal with O(1) space

C. Level-order traversal

D. Balanced tree creation

**Answer:** B

**Explanation:** Morris Traversal is a technique to perform in-order tree traversal without using recursion or a stack, achieving O(1) space complexity by temporarily modifying tree pointers.

---

### Q25.

How do you serialize a binary tree?

A. Store only the leaf values

B. Store level-order traversal with null markers

C. Store only in-order traversal

D. Store the height of the tree

**Answer:** B

**Explanation:** Serialization can be done using level-order (BFS) or pre-order traversal with null markers to represent missing children, allowing complete reconstruction of the tree structure.

---

### Q26.

What is a balanced binary tree?

A. All leaves are at the same level

B. Height difference between left and right subtrees of every node is at most 1

C. Number of left and right children are equal

D. All nodes have two children

**Answer:** B

**Explanation:** A balanced binary tree (like AVL tree) has the property that for every node, the height difference between left and right subtrees is at most 1, ensuring O(log n) operations.

---

### Q27.

What is the sum of all nodes at depth d in a complete binary tree?

A. Can be calculated in O(d) time

B. Can be calculated in O(2^d) time

C. Requires traversing entire tree

D. Cannot be determined

**Answer:** B

**Explanation:** At depth d, there are at most 2^d nodes. To sum them, we need to visit all nodes at that level, which takes O(2^d) time using BFS.

---

### Q28.

How do you find the vertical order traversal of a binary tree?

A. Use in-order traversal

B. Use BFS with horizontal distance tracking

C. Use pre-order traversal

D. Use post-order traversal

**Answer:** B

**Explanation:** Vertical order traversal uses BFS or DFS while maintaining horizontal distance from root (left child: hd-1, right child: hd+1) and grouping nodes by this distance.

---

### Q29.

What is the maximum width of a binary tree?

A. The height of the tree

B. The maximum number of nodes at any level

C. The number of leaf nodes

D. The diameter of the tree

**Answer:** B

**Explanation:** The width of a binary tree is defined as the maximum number of nodes present at any level of the tree. This can be found using level-order traversal.

---

### Q30.

What is the space complexity of level-order traversal using a queue?

A. O(1)

B. O(log n)

C. O(w) where w is maximum width

D. O(h) where h is height

**Answer:** C

**Explanation:** Level-order traversal stores one complete level in the queue at a time. The maximum width (w) of the tree determines the space used, which can be up to O(n) for a complete tree.

---

**End of MCQ Questions**
