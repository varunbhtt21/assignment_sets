# Major Assessment -02 - MCQ Questions
## (Bits Manipulation, Searching, Recursion and Backtracking)

---

### Q1.

What is the result of the bitwise AND operation: 12 & 10?

A. 8

B. 10

C. 12

D. 14

**Answer:** A

**Explanation:** 12 in binary is 1100, 10 in binary is 1010. AND operation: 1100 & 1010 = 1000 = 8 in decimal.

---

### Q2.

Which bitwise operation can be used to check if a number is even or odd?

A. Left shift

B. Right shift

C. AND with 1

D. OR with 1

**Answer:** C

**Explanation:** n & 1 returns 0 if n is even (last bit is 0) and 1 if n is odd (last bit is 1). This is the most efficient way to check parity.

---

### Q3.

What is the time complexity of binary search?

A. O(n)

B. O(log n)

C. O(n log n)

D. O(1)

**Answer:** B

**Explanation:** Binary search divides the search space in half at each step, resulting in O(log n) time complexity for sorted arrays.

---

### Q4.

What does the XOR (^) operation of a number with itself always return?

A. The number itself

B. 0

C. 1

D. -1

**Answer:** B

**Explanation:** Any number XORed with itself always returns 0 because all bits will cancel out. For example: 5 ^ 5 = 0101 ^ 0101 = 0000 = 0.

---

### Q5.

What is the result of left shifting a number by 1 position (n << 1)?

A. n / 2

B. n * 2

C. n + 1

D. n - 1

**Answer:** B

**Explanation:** Left shift by 1 position is equivalent to multiplying by 2. For example: 5 << 1 = 0101 << 1 = 1010 = 10.

---

### Q6.

Which algorithm is required for binary search to work?

A. The array must be sorted

B. The array must contain unique elements

C. The array must have even number of elements

D. The array must be of size 2^n

**Answer:** A

**Explanation:** Binary search requires the array to be sorted (either ascending or descending) to eliminate half of the search space at each step.

---

### Q7.

What is the result of 15 | 8 (bitwise OR)?

A. 7

B. 8

C. 15

D. 23

**Answer:** C

**Explanation:** 15 in binary is 1111, 8 in binary is 1000. OR operation: 1111 | 1000 = 1111 = 15 in decimal.

---

### Q8.

How do you find if a number is a power of 2 using bit manipulation?

A. n & (n - 1) == 0

B. n | (n - 1) == 0

C. n ^ (n - 1) == 0

D. n << 1 == 0

**Answer:** A

**Explanation:** Powers of 2 have only one bit set. n & (n - 1) clears the rightmost set bit. For powers of 2, this results in 0. Example: 8 & 7 = 1000 & 0111 = 0.

---

### Q9.

What is the space complexity of binary search (iterative)?

A. O(1)

B. O(log n)

C. O(n)

D. O(n log n)

**Answer:** A

**Explanation:** Iterative binary search uses only a constant amount of extra space for variables (low, high, mid), making it O(1) space complexity.

---

### Q10.

What does right shifting by 1 position (n >> 1) accomplish?

A. Multiplies n by 2

B. Divides n by 2 (integer division)

C. Adds 1 to n

D. Subtracts 1 from n

**Answer:** B

**Explanation:** Right shift by 1 is equivalent to integer division by 2. For example: 10 >> 1 = 1010 >> 1 = 0101 = 5.

---

### Q11.

What is recursion in programming?

A. A loop that runs indefinitely

B. A function that calls itself

C. A sorting algorithm

D. A data structure

**Answer:** B

**Explanation:** Recursion is a programming technique where a function calls itself directly or indirectly to solve a problem by breaking it into smaller subproblems.

---

### Q12.

What is the base case in recursion?

A. The first recursive call

B. The condition that stops recursion

C. The last recursive call

D. The middle of the recursion

**Answer:** B

**Explanation:** The base case is the terminating condition that stops recursion. Without it, recursion would continue infinitely, causing stack overflow.

---

### Q13.

What is the time complexity of calculating the nth Fibonacci number using naive recursion?

A. O(n)

B. O(log n)

C. O(2^n)

D. O(n²)

**Answer:** C

**Explanation:** Naive recursive Fibonacci has exponential time complexity O(2^n) because it recalculates the same values multiple times without memoization.

---

### Q14.

What is tail recursion?

A. Recursion that happens at the end of a program

B. Recursion where the recursive call is the last operation in the function

C. Recursion with no base case

D. Recursion that uses a tail data structure

**Answer:** B

**Explanation:** Tail recursion occurs when the recursive call is the last statement in the function. Many compilers can optimize tail recursion to avoid stack overflow.

---

### Q15.

What is the maximum recursion depth problem?

A. Recursion can only go 10 levels deep

B. Stack overflow due to too many recursive calls

C. Recursion cannot solve complex problems

D. Base case is never reached

**Answer:** B

**Explanation:** Each recursive call uses stack space. Too many recursive calls can exceed the stack size limit, causing a stack overflow error.

---

### Q16.

What is memoization in recursion?

A. Memorizing the recursive algorithm

B. Storing results of expensive function calls to avoid redundant calculations

C. A type of recursion

D. A base case optimization

**Answer:** B

**Explanation:** Memoization is an optimization technique that stores the results of function calls and returns cached results when the same inputs occur again.

---

### Q17.

What is the space complexity of recursive Fibonacci with memoization?

A. O(1)

B. O(log n)

C. O(n)

D. O(2^n)

**Answer:** C

**Explanation:** Memoization requires O(n) space to store results for each value from 0 to n. The recursion stack also uses O(n) space, so overall it's O(n).

---

### Q18.

Which of the following problems is best solved using recursion?

A. Finding the sum of array elements

B. Printing numbers from 1 to n

C. Tower of Hanoi

D. Checking if a number is even

**Answer:** C

**Explanation:** Tower of Hanoi naturally follows a recursive pattern where solving for n disks depends on solving for n-1 disks. While other problems can use recursion, they don't require it.

---

### Q19.

What is the time complexity of binary search using recursion?

A. O(1)

B. O(log n)

C. O(n)

D. O(n log n)

**Answer:** B

**Explanation:** Recursive binary search has the same time complexity as iterative: O(log n). Each call eliminates half of the remaining elements.

---

### Q20.

What happens if a recursive function has no base case?

A. It runs very fast

B. It causes infinite recursion and stack overflow

C. It returns 0

D. It automatically stops after 100 calls

**Answer:** B

**Explanation:** Without a base case, the function keeps calling itself infinitely until the call stack is exhausted, resulting in a stack overflow error.

---

### Q21.

What is backtracking?

A. A sorting algorithm

B. An algorithmic technique that tries all possibilities and backtracks when a solution path fails

C. Going back in code execution

D. A type of loop

**Answer:** B

**Explanation:** Backtracking is an algorithmic technique that builds solutions incrementally and abandons (backtracks from) paths that fail to satisfy constraints.

---

### Q22.

Which problem is a classic example of backtracking?

A. Finding the sum of an array

B. N-Queens problem

C. Binary search

D. Bubble sort

**Answer:** B

**Explanation:** The N-Queens problem (placing N queens on an N×N chessboard so no two attack each other) is a classic backtracking problem where we try placements and backtrack on conflicts.

---

### Q23.

What is the typical structure of a backtracking algorithm?

A. Choose → Explore → Unchoose

B. Sort → Search → Return

C. Loop → Break → Continue

D. Push → Pop → Peek

**Answer:** A

**Explanation:** Backtracking follows the pattern: make a choice, recursively explore that choice, and unchoose (backtrack) if it doesn't lead to a solution.

---

### Q24.

What is pruning in backtracking?

A. Deleting elements from an array

B. Early termination of paths that cannot lead to valid solutions

C. Removing duplicates

D. Sorting the search space

**Answer:** B

**Explanation:** Pruning is an optimization where we stop exploring a path early if we determine it cannot possibly lead to a valid solution, saving computation time.

---

### Q25.

What is the time complexity of the N-Queens problem using backtracking?

A. O(n!)

B. O(n²)

C. O(2^n)

D. O(n^n)

**Answer:** A

**Explanation:** N-Queens has approximately O(n!) time complexity because we try placing queens in different columns and rows, with many permutations to explore.

---

### Q26.

In the subset sum problem, what technique is most commonly used?

A. Greedy algorithm

B. Backtracking or Dynamic Programming

C. Sorting

D. Binary search

**Answer:** B

**Explanation:** Subset sum is typically solved using backtracking (trying all subsets) or dynamic programming (building solutions bottom-up). Greedy doesn't guarantee correctness.

---

### Q27.

What is the difference between recursion and backtracking?

A. Recursion is faster

B. Backtracking is a specific use of recursion that explores all possibilities and backtracks on failure

C. Recursion uses more memory

D. They are the same thing

**Answer:** B

**Explanation:** Recursion is a general technique where a function calls itself. Backtracking is a specific algorithmic approach that uses recursion to explore solution spaces.

---

### Q28.

How do you count the number of set bits (1s) in a binary number efficiently?

A. Convert to string and count

B. Use a loop and check each bit with (n & 1), then right shift

C. Use division by 2

D. Use modulo operation

**Answer:** B

**Explanation:** The efficient approach is to repeatedly check the least significant bit using (n & 1), count if it's 1, then right shift (n >>= 1) until n becomes 0.

---

### Q29.

What is the "power set" problem and how is it solved?

A. Finding powers of a number, solved by multiplication

B. Finding all subsets of a set, solved using backtracking or bit manipulation

C. Finding the most powerful element, solved by sorting

D. Finding prime numbers, solved using sieve

**Answer:** B

**Explanation:** The power set is the set of all subsets (including empty set and the set itself). It can be solved using backtracking or bit manipulation. For n elements, there are 2^n subsets.

---

### Q30.

What is the advantage of using bit manipulation over regular arithmetic operations?

A. Easier to understand

B. Faster execution at the hardware level

C. Uses less memory

D. Works with larger numbers

**Answer:** B

**Explanation:** Bit manipulation operations are executed directly by the CPU and are extremely fast compared to arithmetic operations like multiplication and division, making them ideal for optimization.

---

**End of MCQ Questions**
