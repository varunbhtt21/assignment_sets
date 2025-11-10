# Recursion and Backtracking - MCQ Questions

---

### Q1.

What is the base case in recursion?

A. The first call to the recursive function

B. The condition that stops the recursion

C. The recursive call itself

D. The return value of the function

**Answer:** B

**Explanation:** The base case is the condition that terminates the recursion, preventing infinite calls.

---

### Q2.

What will be the output of this recursive function?

```java
int factorial(int n) {
    if (n == 0) return 1;
    return n * factorial(n - 1);
}
factorial(4);
```

A. 12

B. 24

C. 120

D. Error

**Answer:** B

**Explanation:** 4! = 4 × 3 × 2 × 1 = 24.

---

### Q3.

Which data structure is used internally to manage recursive function calls?

A. Queue

B. Stack

C. Heap

D. Array

**Answer:** B

**Explanation:** The call stack is used to store return addresses and local variables for each recursive call.

---

### Q4.

What is the space complexity of a recursive function that makes n recursive calls?

A. O(1)

B. O(log n)

C. O(n)

D. O(n²)

**Answer:** C

**Explanation:** Each recursive call adds a frame to the call stack, requiring O(n) space for n calls.

---

### Q5.

What will this code print?

```java
void print(int n) {
    if (n == 0) return;
    System.out.print(n + " ");
    print(n - 1);
}
print(3);
```

A. 1 2 3

B. 3 2 1

C. 3 3 3

D. Error

**Answer:** B

**Explanation:** Prints n before recursive call, so prints 3, then 2, then 1.

---

### Q6.

What is tail recursion?

A. Recursion that calls itself at the end of the function

B. Recursion with no base case

C. Recursion that uses a loop

D. Recursion with multiple base cases

**Answer:** A

**Explanation:** Tail recursion occurs when the recursive call is the last operation in the function.

---

### Q7.

How many times will the function call itself for fib(5)?

```java
int fib(int n) {
    if (n <= 1) return n;
    return fib(n-1) + fib(n-2);
}
```

A. 5

B. 9

C. 15

D. 25

**Answer:** C

**Explanation:** fib(5) makes 15 total calls (including the initial call). The tree has exponential calls.

---

### Q8.

What is the time complexity of the recursive Fibonacci function without memoization?

A. O(n)

B. O(log n)

C. O(2^n)

D. O(n²)

**Answer:** C

**Explanation:** Each call branches into two calls, creating an exponential time complexity.

---

### Q9.

Which problem CANNOT be solved using recursion?

A. Tower of Hanoi

B. Finding factorial

C. None - all problems with iterative solutions can use recursion

D. Binary search

**Answer:** C

**Explanation:** Any problem that can be solved iteratively can also be solved recursively, and vice versa.

---

### Q10.

What will be the output?

```java
void mystery(int n) {
    if (n > 0) {
        mystery(n - 1);
        System.out.print(n + " ");
    }
}
mystery(3);
```

A. 3 2 1

B. 1 2 3

C. 0 1 2 3

D. Error

**Answer:** B

**Explanation:** Recursive call happens first, so printing happens in reverse order during unwinding: 1 2 3.

---

### Q11.

What is backtracking?

A. Going back to the previous state when a solution path fails

B. Reversing an array

C. Sorting in reverse order

D. Deleting elements from a list

**Answer:** A

**Explanation:** Backtracking is an algorithmic technique that explores all possibilities and abandons paths that don't lead to solutions.

---

### Q12.

Which of the following problems is typically solved using backtracking?

A. Finding minimum in an array

B. N-Queens problem

C. Linear search

D. Bubble sort

**Answer:** B

**Explanation:** N-Queens is a classic backtracking problem where we try placing queens and backtrack if placement is invalid.

---

### Q13.

In backtracking, when do we backtrack?

A. When we find a valid solution

B. When current path cannot lead to a solution

C. At every step

D. Only at the end

**Answer:** B

**Explanation:** We backtrack when we determine the current path violates constraints or cannot lead to a valid solution.

---

### Q14.

What is the time complexity of generating all permutations of n elements using backtracking?

A. O(n)

B. O(n²)

C. O(n!)

D. O(2^n)

**Answer:** C

**Explanation:** There are n! permutations possible, and we need to generate each one.

---

### Q15.

Which statement is TRUE about backtracking?

A. It always finds the optimal solution

B. It explores all possible solutions

C. It is faster than dynamic programming

D. It uses iteration only

**Answer:** B

**Explanation:** Backtracking explores all possible solutions and prunes paths that don't satisfy constraints.

---

### Q16.

In the subset sum problem solved with backtracking, how many recursive calls are made in the worst case for n elements?

A. O(n)

B. O(n log n)

C. O(2^n)

D. O(n²)

**Answer:** C

**Explanation:** Each element has two choices (include or exclude), leading to 2^n possible subsets.

---

### Q17.

What is pruning in backtracking?

A. Removing elements from an array

B. Stopping exploration of paths that cannot lead to a solution

C. Deleting nodes from a tree

D. Sorting the input

**Answer:** B

**Explanation:** Pruning eliminates branches of the search tree that cannot possibly lead to a valid solution.

---

### Q18.

Which data structure is most commonly used to implement backtracking?

A. Queue

B. Stack (implicitly through recursion)

C. Linked List

D. Hash Table

**Answer:** B

**Explanation:** Backtracking naturally uses the call stack through recursion, though explicit stacks can also be used.

---

### Q19.

In the Sudoku solver using backtracking, what do we do when we find that no number can be placed in a cell?

A. Place a random number

B. Skip that cell

C. Backtrack to the previous cell

D. Start over from the beginning

**Answer:** C

**Explanation:** When no valid number can be placed, we backtrack to reconsider previous placements.

---

### Q20.

What is the difference between recursion and backtracking?

A. They are the same thing

B. Backtracking is a technique that uses recursion to explore solutions

C. Recursion is slower than backtracking

D. Backtracking doesn't use base cases

**Answer:** B

**Explanation:** Backtracking is an algorithmic technique that often uses recursion to explore and abandon solution paths.

---

### Q21.

What is memoization in recursion?

A. Storing results of expensive function calls and reusing them

B. Using more memory

C. Converting recursion to iteration

D. Adding comments to code

**Answer:** A

**Explanation:** Memoization caches results of function calls to avoid redundant computations.

---

### Q22.

How does memoization improve the Fibonacci recursive function?

A. Changes complexity from O(2^n) to O(n)

B. Reduces space complexity to O(1)

C. Makes it iterative

D. Removes the need for base cases

**Answer:** A

**Explanation:** Memoization stores computed values, reducing redundant calculations from exponential to linear time.

---

### Q23.

What is the space complexity of a memoized recursive function with n unique subproblems?

A. O(1)

B. O(log n)

C. O(n)

D. O(n²)

**Answer:** C

**Explanation:** We need O(n) space to store results of n subproblems, plus O(n) for the recursion stack.

---

### Q24.

Which technique converts tail recursion to iteration automatically?

A. Memoization

B. Dynamic Programming

C. Tail Call Optimization (TCO)

D. Backtracking

**Answer:** C

**Explanation:** Tail Call Optimization reuses the current stack frame for tail recursive calls, effectively converting to iteration.

---

### Q25.

In a recursive tree with branching factor b and depth d, how many nodes are there?

A. b × d

B. b + d

C. (b^(d+1) - 1) / (b - 1)

D. b^d

**Answer:** C

**Explanation:** This is the formula for the total number of nodes in a complete tree with branching factor b and depth d.

---

### Q26.

What will be the output?

```java
int sum(int n) {
    if (n == 1) return 1;
    return n + sum(n - 1);
}
sum(5);
```

A. 5

B. 10

C. 15

D. 120

**Answer:** C

**Explanation:** Sum of 1+2+3+4+5 = 15.

---

### Q27.

Which recursion type is easier to convert to iteration?

A. Head recursion

B. Tail recursion

C. Tree recursion

D. All are equally difficult

**Answer:** B

**Explanation:** Tail recursion can be easily converted to iteration as no computation happens after the recursive call.

---

### Q28.

What is indirect recursion?

A. Function A calls function B, and B calls A

B. Function calls itself multiple times

C. Function has no base case

D. Function uses a helper function

**Answer:** A

**Explanation:** Indirect recursion occurs when functions call each other in a cycle (A ’ B ’ A).

---

### Q29.

In the recursive solution for the Tower of Hanoi with n disks, how many moves are needed?

A. n

B. 2n

C. 2^n - 1

D. n²

**Answer:** C

**Explanation:** The minimum number of moves for n disks is 2^n - 1.

---

### Q30.

What is the base case for most binary search recursive implementations?

A. left > right

B. left == right

C. left < right

D. array is empty

**Answer:** A

**Explanation:** When left > right, the search space is exhausted, indicating the element is not found.

---

**End of MCQ Questions**
