# Stack and Queue & Linkedlist - MCQ Questions

---

### Q1.

What is the LIFO principle in Stack?

A. Last In First Out

B. Least In First Out

C. Last In Forever Out

D. Linear In First Out

**Answer:** A

**Explanation:** Stack follows Last In First Out (LIFO) principle, meaning the last element added to the stack will be the first one to be removed.

---

### Q2.

What is the time complexity of push and pop operations in a stack?

A. O(n)

B. O(log n)

C. O(1)

D. O(n²)

**Answer:** C

**Explanation:** Both push and pop operations in a stack take constant time O(1) as they only involve adding or removing an element from the top.

---

### Q3.

Which data structure is used to implement recursion?

A. Queue

B. Stack

C. Array

D. Tree

**Answer:** B

**Explanation:** Recursion is implemented using the call stack. Each recursive call is pushed onto the stack, and when a function returns, it's popped from the stack.

---

### Q4.

What is the FIFO principle in Queue?

A. First In First Out

B. Fast In Fast Out

C. First In Forever Out

D. Fixed In First Out

**Answer:** A

**Explanation:** Queue follows First In First Out (FIFO) principle, meaning the first element added to the queue will be the first one to be removed.

---

### Q5.

What are the two main operations of a queue?

A. push and pop

B. insert and delete

C. enqueue and dequeue

D. add and remove

**Answer:** C

**Explanation:** The standard operations for a queue are enqueue (add element to rear) and dequeue (remove element from front).

---

### Q6.

What is the time complexity of enqueue and dequeue operations in a queue?

A. O(n)

B. O(log n)

C. O(1)

D. O(n²)

**Answer:** C

**Explanation:** Both enqueue and dequeue operations take constant time O(1) when implemented efficiently using a circular queue or linked list.

---

### Q7.

Which application uses a Stack data structure?

A. Breadth-First Search

B. Expression evaluation and syntax parsing

C. Scheduling algorithms

D. Finding shortest path

**Answer:** B

**Explanation:** Stacks are used for expression evaluation (postfix, prefix), syntax parsing, backtracking, and function call management.

---

### Q8.

What is a monotonic stack?

A. A stack that only stores increasing values

B. A stack that maintains elements in monotonically increasing or decreasing order

C. A stack with constant size

D. A stack that never changes

**Answer:** B

**Explanation:** A monotonic stack maintains elements in either strictly increasing or strictly decreasing order, useful for problems like next greater element.

---

### Q9.

What is the minimum number of stacks needed to implement a queue?

A. 1

B. 2

C. 3

D. Cannot be implemented

**Answer:** B

**Explanation:** A queue can be implemented using two stacks - one for enqueue operations and another for dequeue operations.

---

### Q10.

In the "Valid Parentheses" problem, what is the correct approach?

A. Count opening and closing brackets

B. Use a stack to match opening brackets with closing brackets

C. Use a queue

D. Sort the string

**Answer:** B

**Explanation:** Use a stack to push opening brackets and pop when encountering matching closing brackets. If stack is empty at the end, parentheses are valid.

---

### Q11.

What is a singly linked list?

A. A list where each node points to the next node

B. A list where each node points to previous and next nodes

C. A circular list

D. A list with no pointers

**Answer:** A

**Explanation:** In a singly linked list, each node contains data and a pointer to the next node in the sequence.

---

### Q12.

What is the time complexity of inserting a node at the beginning of a singly linked list?

A. O(n)

B. O(log n)

C. O(1)

D. O(n²)

**Answer:** C

**Explanation:** Inserting at the beginning requires creating a new node, pointing it to the current head, and updating head pointer - all O(1) operations.

---

### Q13.

What is the time complexity of accessing the nth element in a linked list?

A. O(1)

B. O(log n)

C. O(n)

D. O(n²)

**Answer:** C

**Explanation:** Unlike arrays, linked lists don't support random access. We must traverse from the head to reach the nth element, taking O(n) time.

---

### Q14.

What is a doubly linked list?

A. A list with two heads

B. A list where each node has pointers to both next and previous nodes

C. A list with duplicate values

D. Two separate linked lists

**Answer:** B

**Explanation:** In a doubly linked list, each node contains data, a pointer to the next node, and a pointer to the previous node, allowing bidirectional traversal.

---

### Q15.

How do you detect a cycle in a linked list?

A. Use two nested loops

B. Use Floyd's cycle detection algorithm (slow and fast pointers)

C. Sort the list

D. Count the nodes

**Answer:** B

**Explanation:** Floyd's algorithm uses two pointers moving at different speeds. If there's a cycle, the fast pointer will eventually meet the slow pointer.

---

### Q16.

What is the advantage of a linked list over an array?

A. Random access is faster

B. Dynamic size and efficient insertion/deletion

C. Less memory usage

D. Better cache performance

**Answer:** B

**Explanation:** Linked lists can grow/shrink dynamically and allow O(1) insertion/deletion at known positions, unlike arrays which require shifting elements.

---

### Q17.

What is the space complexity of a recursive solution to reverse a linked list?

A. O(1)

B. O(log n)

C. O(n)

D. O(n²)

**Answer:** C

**Explanation:** Recursive reversal uses the call stack, which can go as deep as the number of nodes in the list, requiring O(n) space.

---

### Q18.

In a circular linked list, what does the last node point to?

A. NULL

B. The first node (head)

C. Itself

D. The second node

**Answer:** B

**Explanation:** In a circular linked list, the last node's next pointer points back to the first node, forming a circle.

---

### Q19.

What is the "runner technique" (fast and slow pointers) used for in linked lists?

A. Sorting the list

B. Finding middle element, detecting cycles, finding nth node from end

C. Reversing the list

D. Deleting nodes

**Answer:** B

**Explanation:** The runner technique uses two pointers at different speeds to solve problems like finding the middle, cycle detection, and finding nth from end.

---

### Q20.

How do you find the middle element of a linked list in one pass?

A. Count nodes first, then traverse to middle

B. Use slow and fast pointers

C. Use recursion

D. Cannot be done in one pass

**Answer:** B

**Explanation:** Use two pointers: slow moves one step, fast moves two steps. When fast reaches the end, slow is at the middle.

---

### Q21.

What is a deque (double-ended queue)?

A. A queue with two fronts

B. A queue where insertion and deletion can happen at both ends

C. Two separate queues

D. A circular queue

**Answer:** B

**Explanation:** A deque allows insertion and deletion operations at both front and rear, combining features of both stack and queue.

---

### Q22.

What is the "next greater element" problem typically solved with?

A. Queue

B. Array

C. Monotonic Stack

D. Hash Table

**Answer:** C

**Explanation:** A monotonic decreasing stack efficiently finds the next greater element by maintaining elements in decreasing order.

---

### Q23.

In the "sliding window maximum" problem, which data structure is most efficient?

A. Stack

B. Deque

C. Array

D. Linked List

**Answer:** B

**Explanation:** A deque maintains indices of useful elements in decreasing order of their values, giving O(n) solution for sliding window maximum.

---

### Q24.

What is the dummy node technique in linked list problems?

A. Adding a fake node before the head to simplify edge cases

B. Duplicating all nodes

C. Creating an empty list

D. Marking deleted nodes

**Answer:** A

**Explanation:** A dummy/sentinel node before the head simplifies operations by eliminating special cases for head node operations.

---

### Q25.

How do you merge two sorted linked lists?

A. Concatenate and sort

B. Use two pointers to compare and link nodes

C. Use recursion only

D. Convert to arrays first

**Answer:** B

**Explanation:** Compare nodes from both lists using two pointers, linking the smaller node to the result list. This can be done iteratively or recursively.

---

### Q26.

What is the time complexity of reversing a linked list?

A. O(1)

B. O(log n)

C. O(n)

D. O(n²)

**Answer:** C

**Explanation:** Reversing requires visiting each node once to change its next pointer, resulting in O(n) time complexity.

---

### Q27.

In a priority queue implemented with a heap, what is the time complexity of inserting an element?

A. O(1)

B. O(log n)

C. O(n)

D. O(n log n)

**Answer:** B

**Explanation:** Inserting into a heap requires adding the element at the end and bubbling up, which takes O(log n) time where n is the number of elements.

---

### Q28.

What is the stack overflow error?

A. Too many elements in stack

B. Stack has no elements

C. Call stack exceeds its size limit (often from infinite recursion)

D. Stack memory is freed

**Answer:** C

**Explanation:** Stack overflow occurs when the call stack exceeds its maximum size, typically from infinite or very deep recursion.

---

### Q29.

How do you implement a min stack that supports getMin() in O(1) time?

A. Sort the stack

B. Use an auxiliary stack to track minimum values

C. Scan all elements each time

D. Use a linked list

**Answer:** B

**Explanation:** Maintain an auxiliary stack that stores the minimum value at each level, allowing O(1) getMin() operation.

---

### Q30.

What is the time complexity of checking if a linked list is a palindrome?

A. O(1)

B. O(log n)

C. O(n)

D. O(n²)

**Answer:** C

**Explanation:** Find the middle (O(n)), reverse the second half (O(n)), compare both halves (O(n)). Overall time complexity is O(n).

---

**End of MCQ Questions**
