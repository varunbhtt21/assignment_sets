# Major Assessment -04 - MCQ Questions
## (DP, Stack & Queue, LinkedList)

---

### Q1.

What is dynamic programming?

A. A greedy algorithm technique

B. An optimization technique that solves problems by breaking them into overlapping subproblems

C. A sorting algorithm

D. A data structure for storing data

**Answer:** B

**Explanation:** Dynamic programming is an optimization technique that solves complex problems by breaking them down into simpler overlapping subproblems, storing the results to avoid redundant calculations (memoization or tabulation).

---

### Q2.

What are the two main approaches to implement dynamic programming?

A. Recursion and Iteration

B. Top-down (Memoization) and Bottom-up (Tabulation)

C. Divide and Conquer

D. Greedy and Backtracking

**Answer:** B

**Explanation:** Dynamic programming has two main approaches: Top-down (memoization) uses recursion with caching, and Bottom-up (tabulation) builds solutions iteratively from base cases.

---

### Q3.

What is memoization in dynamic programming?

A. Memorizing the algorithm

B. Storing results of expensive function calls and returning cached result when same inputs occur

C. A type of sorting

D. A data structure

**Answer:** B

**Explanation:** Memoization is a technique where we cache the results of function calls (typically in a hash map or array) and return the cached result when the same inputs occur again, avoiding redundant calculations.

---

### Q4.

What is the time complexity of accessing an element in a stack?

A. O(1) for top element

B. O(n) for any element

C. O(log n)

D. Both A and B are correct

**Answer:** D

**Explanation:** Accessing the top element of a stack is O(1), but accessing an arbitrary element requires popping elements until you reach it, which is O(n) in the worst case.

---

### Q5.

Which data structure follows the LIFO (Last In First Out) principle?

A. Queue

B. Stack

C. Linked List

D. Array

**Answer:** B

**Explanation:** Stack follows LIFO (Last In First Out) - the last element added is the first one to be removed. Think of a stack of plates where you can only add/remove from the top.

---

### Q6.

What is the time complexity of enqueue and dequeue operations in a queue using a linked list?

A. O(1) for both

B. O(n) for both

C. O(1) for enqueue, O(n) for dequeue

D. O(n) for enqueue, O(1) for dequeue

**Answer:** A

**Explanation:** Using a linked list with both head and tail pointers, enqueue (add to tail) and dequeue (remove from head) both operate in O(1) time.

---

### Q7.

What is the main difference between a stack and a queue?

A. Stack is LIFO, Queue is FIFO

B. Stack is FIFO, Queue is LIFO

C. Both follow LIFO

D. Both follow FIFO

**Answer:** A

**Explanation:** Stack follows LIFO (Last In First Out) while Queue follows FIFO (First In First Out). In a queue, the first element added is the first to be removed.

---

### Q8.

In dynamic programming, what does "optimal substructure" mean?

A. The problem can be solved using a greedy approach

B. The optimal solution to the problem can be constructed from optimal solutions of its subproblems

C. The problem has only one solution

D. The problem requires backtracking

**Answer:** B

**Explanation:** Optimal substructure means that the optimal solution to a problem contains optimal solutions to its subproblems. This is a key property required for dynamic programming to work.

---

### Q9.

What is the space complexity of a recursive solution with memoization for a problem with n states?

A. O(1)

B. O(n)

C. O(n²)

D. O(log n)

**Answer:** B

**Explanation:** Memoization requires O(n) space to store the results of n subproblems, plus O(n) for the recursion call stack in the worst case, totaling O(n) space complexity.

---

### Q10.

Which operation is NOT typically supported by a standard stack?

A. Push

B. Pop

C. Peek/Top

D. Random access to middle elements

**Answer:** D

**Explanation:** Standard stacks support push (add to top), pop (remove from top), and peek (view top element), but do not support efficient random access to middle elements - you'd have to pop elements to reach them.

---

### Q11.

What is the time complexity of inserting a node at the beginning of a singly linked list?

A. O(1)

B. O(n)

C. O(log n)

D. O(n²)

**Answer:** A

**Explanation:** Inserting at the beginning of a linked list requires creating a new node, setting its next pointer to the current head, and updating the head pointer - all O(1) operations.

---

### Q12.

What is the advantage of a linked list over an array?

A. Faster random access

B. Dynamic size - easy insertion and deletion

C. Better cache locality

D. Less memory usage

**Answer:** B

**Explanation:** Linked lists have dynamic size and allow O(1) insertion/deletion at known positions (especially at head). Arrays have fixed size and require shifting elements for insertion/deletion in the middle.

---

### Q13.

In the context of dynamic programming, what are overlapping subproblems?

A. Subproblems that share common data

B. Subproblems that are computed multiple times in a naive recursive solution

C. Subproblems that cannot be solved independently

D. Subproblems that have the same solution

**Answer:** B

**Explanation:** Overlapping subproblems occur when the same subproblem is solved multiple times in a recursive solution. DP optimizes this by storing results of subproblems and reusing them.

---

### Q14.

What is a monotonic stack?

A. A stack that only stores increasing or decreasing elements

B. A stack with constant size

C. A stack that only allows even numbers

D. A stack implemented using an array

**Answer:** A

**Explanation:** A monotonic stack maintains elements in either strictly increasing or strictly decreasing order. It's useful for problems like finding next greater/smaller elements.

---

### Q15.

What is the time complexity of finding the middle element in a singly linked list?

A. O(1)

B. O(n)

C. O(log n)

D. O(n²)

**Answer:** B

**Explanation:** Finding the middle of a singly linked list requires traversing half the list (using slow/fast pointer technique or counting), which takes O(n) time where n is the number of nodes.

---

### Q16.

Which problem is best solved using dynamic programming?

A. Finding if a number is prime

B. Fibonacci sequence

C. Binary search

D. Sorting an array

**Answer:** B

**Explanation:** Fibonacci sequence has overlapping subproblems (fib(n) = fib(n-1) + fib(n-2)) and optimal substructure, making it ideal for DP. Naive recursion is O(2^n) while DP solution is O(n).

---

### Q17.

What is a deque (double-ended queue)?

A. A queue that can only add elements

B. A queue where elements can be added or removed from both ends

C. A queue with maximum size of 2

D. A queue that stores only duplicates

**Answer:** B

**Explanation:** A deque (double-ended queue) allows insertion and deletion at both the front and rear ends, combining properties of both stack and queue.

---

### Q18.

What is the time complexity of reversing a singly linked list?

A. O(1)

B. O(n)

C. O(log n)

D. O(n²)

**Answer:** B

**Explanation:** Reversing a singly linked list requires traversing the entire list once, changing each node's next pointer. This takes O(n) time and can be done with O(1) extra space.

---

### Q19.

In dynamic programming, what is the difference between 1D and 2D DP?

A. 1D DP uses arrays, 2D DP uses linked lists

B. 1D DP has one parameter in the state, 2D DP has two parameters

C. 1D DP is faster than 2D DP

D. There is no difference

**Answer:** B

**Explanation:** The dimension of DP refers to the number of parameters needed to define a state. 1D DP uses one parameter (like dp[i]), 2D DP uses two (like dp[i][j]) for problems with two variables.

---

### Q20.

What is the space complexity of implementing a queue using two stacks?

A. O(1)

B. O(n)

C. O(log n)

D. O(n²)

**Answer:** B

**Explanation:** Implementing a queue using two stacks requires storing all n elements across the two stacks, resulting in O(n) space complexity.

---

### Q21.

What is a circular linked list?

A. A linked list where the last node points back to the first node

B. A linked list arranged in a circle shape physically

C. A linked list with circular data

D. A linked list with only one node

**Answer:** A

**Explanation:** A circular linked list is one where the last node's next pointer points back to the first node instead of null, forming a cycle. This allows continuous traversal.

---

### Q22.

Which of the following is true about the maximum product subarray problem?

A. It can be solved using Kadane's algorithm without modification

B. It requires tracking both maximum and minimum products due to negative numbers

C. It always has O(n²) time complexity

D. It cannot be solved using dynamic programming

**Answer:** B

**Explanation:** Unlike maximum sum subarray, maximum product requires tracking both max and min products because a negative number can turn a large negative product into a large positive product.

---

### Q23.

What is the purpose of a priority queue?

A. To process elements in FIFO order

B. To process elements based on priority, not insertion order

C. To store only unique elements

D. To sort elements

**Answer:** B

**Explanation:** A priority queue processes elements based on their priority (typically implemented using a heap), not their insertion order. Highest (or lowest) priority elements are dequeued first.

---

### Q24.

What is the Floyd's Cycle Detection algorithm (Tortoise and Hare) used for in linked lists?

A. To find the middle element

B. To detect if a cycle exists

C. To reverse the list

D. To sort the list

**Answer:** B

**Explanation:** Floyd's Cycle Detection uses two pointers (slow and fast) moving at different speeds. If there's a cycle, the fast pointer will eventually catch up to the slow pointer.

---

### Q25.

In the decode string problem (k[string]), which data structure is most suitable?

A. Queue

B. Stack

C. Linked List

D. Array

**Answer:** B

**Explanation:** Stack is ideal for decode string because we need to process nested brackets. When we encounter ']', we pop from stack until we find '[', then multiply the string by k.

---

### Q26.

What is the time complexity of the optimal solution for the 0/1 Knapsack problem using DP?

A. O(n)

B. O(n * W) where n is items and W is capacity

C. O(2^n)

D. O(n²)

**Answer:** B

**Explanation:** The DP solution for 0/1 Knapsack uses a 2D table of size n × W, where n is the number of items and W is the knapsack capacity, resulting in O(n * W) time complexity.

---

### Q27.

What is the advantage of a doubly linked list over a singly linked list?

A. Uses less memory

B. Allows traversal in both directions

C. Faster insertion at the beginning

D. Better cache performance

**Answer:** B

**Explanation:** Doubly linked lists have both next and previous pointers, allowing bidirectional traversal. This enables O(1) deletion of a node when you have a pointer to it, unlike singly linked lists.

---

### Q28.

What is the "next greater element" problem typically solved with?

A. Queue

B. Monotonic Stack

C. Heap

D. Hash Table

**Answer:** B

**Explanation:** The next greater element problem is efficiently solved using a monotonic stack. We maintain a decreasing stack and when we find a larger element, we pop and update the results.

---

### Q29.

In dynamic programming, what does "state" refer to?

A. The current position in the array

B. A unique configuration of subproblem parameters

C. The final answer

D. The base case

**Answer:** B

**Explanation:** A state in DP represents a unique subproblem defined by its parameters (e.g., dp[i][j] where i and j are parameters). Each state stores the solution to that specific subproblem.

---

### Q30.

What is the time complexity of implementing stack operations using a linked list?

A. O(1) for push and pop

B. O(n) for push and pop

C. O(log n) for push and pop

D. O(1) for push, O(n) for pop

**Answer:** A

**Explanation:** Using a linked list with operations at the head, both push (insert at head) and pop (remove from head) are O(1) operations as they only involve pointer manipulation.

---

**End of MCQ Questions**
