# Dynamic Programming - MCQ Questions

---

### Q1.

What is Dynamic Programming?

A. A technique to sort arrays efficiently

B. An optimization technique that solves problems by breaking them into overlapping subproblems

C. A way to traverse trees

D. A data structure for storing data

**Answer:** B

**Explanation:** Dynamic Programming is an algorithmic technique that solves complex problems by breaking them down into simpler overlapping subproblems and storing their solutions to avoid redundant calculations.

---

### Q2.

Which two properties must a problem have to apply Dynamic Programming?

A. Sorting and Searching

B. Optimal Substructure and Overlapping Subproblems

C. Recursion and Iteration

D. Arrays and Lists

**Answer:** B

**Explanation:** For DP to be applicable, a problem must have: (1) Optimal Substructure - optimal solution can be constructed from optimal solutions of subproblems, and (2) Overlapping Subproblems - same subproblems are solved multiple times.

---

### Q3.

What is the difference between memoization and tabulation in Dynamic Programming?

A. They are the same thing

B. Memoization is top-down (recursive), tabulation is bottom-up (iterative)

C. Memoization is faster than tabulation

D. Tabulation uses more memory

**Answer:** B

**Explanation:** Memoization uses recursion with caching (top-down approach), while tabulation uses iteration to fill a table (bottom-up approach). Both solve DP problems but with different implementation strategies.

---

### Q4.

What is the time complexity of the Fibonacci sequence using naive recursion?

A. O(n)

B. O(log n)

C. O(2^n)

D. O(n²)

**Answer:** C

**Explanation:** Naive recursive Fibonacci has exponential time complexity O(2^n) because each call branches into two more calls, creating an exponential tree of recursive calls.

---

### Q5.

What is the time complexity of Fibonacci using Dynamic Programming (memoization or tabulation)?

A. O(n)

B. O(log n)

C. O(2^n)

D. O(n²)

**Answer:** A

**Explanation:** With DP, each Fibonacci number is calculated only once and stored, reducing time complexity from O(2^n) to O(n).

---

### Q6.

What is the space complexity of the tabulation approach for Fibonacci?

A. O(1) if we only keep last two values

B. O(n) if we store all values

C. O(2^n)

D. Both A and B are correct

**Answer:** D

**Explanation:** We can optimize space to O(1) by only keeping the last two Fibonacci numbers, or use O(n) space to store all values up to n. Both approaches are valid depending on requirements.

---

### Q7.

In the 0/1 Knapsack problem, what does "0/1" signify?

A. Binary representation

B. Each item can be taken 0 or 1 times (cannot be fractionally divided)

C. There are only 0s and 1s in input

D. The answer is always 0 or 1

**Answer:** B

**Explanation:** In 0/1 Knapsack, each item can either be included (1) or excluded (0), but cannot be partially taken. This distinguishes it from fractional knapsack.

---

### Q8.

What is the time complexity of the 0/1 Knapsack problem using DP where n is number of items and W is knapsack capacity?

A. O(n)

B. O(W)

C. O(n × W)

D. O(2^n)

**Answer:** C

**Explanation:** The DP solution for 0/1 Knapsack uses a 2D table of size n × W, where we compute each cell once, resulting in O(n × W) time complexity.

---

### Q9.

What is the Longest Common Subsequence (LCS) problem?

A. Finding the longest substring common to two strings

B. Finding the longest sequence of characters that appear in the same order in both strings

C. Finding the longest palindrome

D. Finding the longest increasing sequence

**Answer:** B

**Explanation:** LCS finds the longest sequence of characters that appear in the same relative order in both strings, but the characters don't need to be contiguous.

---

### Q10.

For strings of length m and n, what is the time complexity of finding LCS using DP?

A. O(m + n)

B. O(m × n)

C. O(max(m, n))

D. O(2^(m+n))

**Answer:** B

**Explanation:** LCS uses a 2D DP table of size (m+1) × (n+1), and we fill each cell once, resulting in O(m × n) time complexity.

---

### Q11.

What is the Coin Change problem?

A. Finding the minimum number of coins to make a given amount

B. Counting total number of coins

C. Sorting coins by value

D. Finding the largest coin

**Answer:** A

**Explanation:** The classic Coin Change problem asks for the minimum number of coins needed to make a specific amount, given an array of coin denominations.

---

### Q12.

In the Edit Distance problem, which operations are typically allowed?

A. Only insertion

B. Only deletion

C. Insert, Delete, and Replace

D. Only Replace

**Answer:** C

**Explanation:** Edit Distance (Levenshtein Distance) allows three operations: insert a character, delete a character, or replace a character to transform one string into another.

---

### Q13.

What does "optimal substructure" mean in Dynamic Programming?

A. The problem can be solved using sorting

B. The optimal solution contains optimal solutions to subproblems

C. The problem has a recursive structure

D. The solution is always unique

**Answer:** B

**Explanation:** Optimal substructure means that an optimal solution to a problem contains optimal solutions to its subproblems. This property allows us to build up the solution from smaller subproblems.

---

### Q14.

What is the space complexity of the standard DP solution for Longest Increasing Subsequence (LIS)?

A. O(1)

B. O(n)

C. O(n²)

D. O(2^n)

**Answer:** B

**Explanation:** LIS using DP requires an array of size n to store the length of LIS ending at each position, resulting in O(n) space complexity.

---

### Q15.

In the Matrix Chain Multiplication problem, what are we trying to minimize?

A. Number of matrices

B. Size of matrices

C. Number of scalar multiplications

D. Memory usage

**Answer:** C

**Explanation:** Matrix Chain Multiplication aims to find the optimal parenthesization that minimizes the total number of scalar multiplications needed to compute the product.

---

### Q16.

What is the time complexity of the Matrix Chain Multiplication DP solution for n matrices?

A. O(n)

B. O(n²)

C. O(n³)

D. O(n!)

**Answer:** C

**Explanation:** The DP solution uses a 2D table and for each cell, we try all possible split points, resulting in O(n³) time complexity.

---

### Q17.

What is the "rod cutting" problem in DP?

A. Cutting a rod into equal pieces

B. Finding the maximum profit by cutting a rod into pieces of different lengths with given prices

C. Minimizing waste when cutting

D. Counting number of ways to cut

**Answer:** B

**Explanation:** Rod Cutting problem involves determining how to cut a rod into pieces to maximize profit, given that different lengths have different prices per unit.

---

### Q18.

Which problem is NOT typically solved using Dynamic Programming?

A. Shortest Path in a graph

B. Longest Palindromic Subsequence

C. Binary Search

D. Subset Sum

**Answer:** C

**Explanation:** Binary Search is a divide-and-conquer algorithm without overlapping subproblems. It doesn't benefit from DP. The other problems have overlapping subproblems and optimal substructure.

---

### Q19.

What is the "House Robber" problem asking for?

A. Finding the fastest escape route

B. Maximum money that can be robbed without robbing adjacent houses

C. Total number of houses

D. Minimum security needed

**Answer:** B

**Explanation:** House Robber problem asks for the maximum amount that can be stolen from houses arranged in a line, with the constraint that adjacent houses cannot be robbed (they have alarms).

---

### Q20.

In the "Climbing Stairs" problem, if you can climb 1 or 2 steps at a time, what pattern does the solution follow?

A. Factorial sequence

B. Fibonacci sequence

C. Arithmetic sequence

D. Geometric sequence

**Answer:** B

**Explanation:** Ways to reach step n = ways to reach (n-1) + ways to reach (n-2), which is exactly the Fibonacci recurrence relation.

---

### Q21.

What is state in Dynamic Programming?

A. The current value of a variable

B. A set of parameters that uniquely identify a subproblem

C. The final answer

D. The input array

**Answer:** B

**Explanation:** A state in DP is defined by parameters that uniquely identify a subproblem. The DP solution stores and reuses results for each state.

---

### Q22.

What is the "Partition Equal Subset Sum" problem?

A. Dividing array into two parts with equal elements

B. Dividing array into two subsets with equal sum

C. Finding pairs with equal sum

D. Sorting array into two parts

**Answer:** B

**Explanation:** This problem asks if an array can be partitioned into two subsets such that the sum of elements in both subsets is equal.

---

### Q23.

What is the time complexity of solving the Longest Palindromic Substring using DP?

A. O(n)

B. O(n log n)

C. O(n²)

D. O(n³)

**Answer:** C

**Explanation:** Using DP with a 2D table where dp[i][j] represents if substring from i to j is a palindrome requires O(n²) time to fill the table.

---

### Q24.

In the "Unique Paths" problem (grid traversal), what is the DP recurrence relation?

A. dp[i][j] = dp[i-1][j] + dp[i][j-1]

B. dp[i][j] = dp[i-1][j] × dp[i][j-1]

C. dp[i][j] = max(dp[i-1][j], dp[i][j-1])

D. dp[i][j] = min(dp[i-1][j], dp[i][j-1])

**Answer:** A

**Explanation:** Number of ways to reach cell (i,j) equals the sum of ways to reach from above (i-1,j) and from left (i,j-1).

---

### Q25.

What is "state compression" in Dynamic Programming?

A. Compressing the input data

B. Reducing the number of states or dimensions in DP solution

C. Using bitwise operations

D. Sorting the states

**Answer:** B

**Explanation:** State compression involves reducing the number of dimensions or states in a DP solution to optimize space complexity, such as using O(n) instead of O(n²).

---

### Q26.

In the "Palindrome Partitioning" problem, what are we trying to minimize?

A. Length of palindromes

B. Number of partitions (cuts) needed to make all parts palindromes

C. Number of characters

D. Total partitions possible

**Answer:** B

**Explanation:** The problem asks for the minimum number of cuts needed to partition a string such that every substring is a palindrome.

---

### Q27.

What is bitmask DP used for?

A. Bitwise operations only

B. Problems where state can be represented using bits (subset problems)

C. Binary search

D. Array manipulation

**Answer:** B

**Explanation:** Bitmask DP is used when the state involves subsets, where each bit represents whether an element is included or not. Common in problems like Traveling Salesman Problem.

---

### Q28.

What is the time complexity of the DP solution for the "Word Break" problem with string length n and dictionary size m?

A. O(n)

B. O(n²)

C. O(n × m)

D. O(n² × m)

**Answer:** B

**Explanation:** For each position i, we check all previous positions j, and checking if substring s[j:i] is in dictionary is O(1) with hash set, giving O(n²) overall complexity.

---

### Q29.

What is the difference between "minimum path sum" and "maximum path sum" problems?

A. They use different algorithms

B. They are the same problem

C. Only the comparison operator changes (min vs max) in DP recurrence

D. Minimum is always faster

**Answer:** C

**Explanation:** These problems have the same structure and DP approach; only the recurrence relation changes from min to max. The algorithmic approach remains identical.

---

### Q30.

Which technique is most similar to Dynamic Programming?

A. Greedy Algorithm

B. Divide and Conquer with overlapping subproblems

C. Binary Search

D. Hashing

**Answer:** B

**Explanation:** DP is essentially Divide and Conquer with memoization for overlapping subproblems. The key difference is that D&C solves independent subproblems while DP handles overlapping ones.

---

**End of MCQ Questions**
