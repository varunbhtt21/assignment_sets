# Extra Mid Term Assessment - MCQ Questions
## (Arrays, 2D Arrays, Strings, Number Theory, 2 Pointers & Sliding Window)

---

### Q1.

What is the time complexity of accessing an element in an array by its index?

A. O(1)

B. O(n)

C. O(log n)

D. O(n²)

**Answer:** A

**Explanation:** Array elements are stored in contiguous memory locations, allowing direct access using index arithmetic. The address can be calculated as base_address + (index × element_size), which is a constant-time O(1) operation.

---

### Q2.

Which of the following operations has O(n) time complexity for an array of size n?

A. Accessing the last element

B. Finding the maximum element in an unsorted array

C. Inserting at the end when space is available

D. Checking if array is empty

**Answer:** B

**Explanation:** Finding the maximum element in an unsorted array requires traversing all n elements to compare them, resulting in O(n) time complexity. All other options are O(1) operations.

---

### Q3.

In a 2D array stored in row-major order, what is the formula to access element at position (i, j) in an array with m rows and n columns?

A. base_address + (i × n + j) × element_size

B. base_address + (j × m + i) × element_size

C. base_address + (i + j × n) × element_size

D. base_address + (i × j) × element_size

**Answer:** A

**Explanation:** In row-major order, rows are stored consecutively. To reach row i, we skip i complete rows (i × n elements), then add j to reach column j within that row. The formula is base_address + (i × n + j) × element_size.

---

### Q4.

What is the time complexity of rotating an array of size n by k positions?

A. O(1)

B. O(k)

C. O(n)

D. O(n × k)

**Answer:** C

**Explanation:** The optimal algorithm for array rotation uses the reversal technique: reverse entire array, reverse first k elements, reverse remaining elements. Each reversal takes O(n) time, and we do a constant number of reversals, so overall time complexity is O(n).

---

### Q5.

Which string matching algorithm has the best worst-case time complexity?

A. Naive pattern matching - O(m × n)

B. KMP (Knuth-Morris-Pratt) - O(m + n)

C. Boyer-Moore - O(m × n)

D. Rabin-Karp - O(m × n)

**Answer:** B

**Explanation:** KMP algorithm preprocesses the pattern to create a failure function, then uses it to avoid re-comparing characters. This gives O(m + n) time complexity in all cases, where m is pattern length and n is text length. Other algorithms have O(m × n) worst case.

---

### Q6.

What is the time complexity of checking if a string is a palindrome?

A. O(1)

B. O(n)

C. O(n log n)

D. O(n²)

**Answer:** B

**Explanation:** To check if a string is a palindrome, we compare characters from both ends moving towards the center. We need to check at most n/2 pairs of characters, which is O(n) time complexity.

---

### Q7.

The Sieve of Eratosthenes algorithm is used to find all prime numbers up to n. What is its time complexity?

A. O(n)

B. O(n log n)

C. O(n log log n)

D. O(n²)

**Answer:** C

**Explanation:** The Sieve of Eratosthenes marks multiples of each prime. The total number of operations is n/2 + n/3 + n/5 + ... (for each prime p up to √n), which mathematically evaluates to O(n log log n).

---

### Q8.

What is the GCD (Greatest Common Divisor) of 48 and 18?

A. 2

B. 6

C. 9

D. 12

**Answer:** B

**Explanation:** Using Euclidean algorithm: GCD(48, 18) = GCD(18, 48%18) = GCD(18, 12) = GCD(12, 6) = GCD(6, 0) = 6. The factors of 48 are {1,2,3,4,6,8,12,16,24,48} and 18 are {1,2,3,6,9,18}. Greatest common divisor is 6.

---

### Q9.

If GCD(a, b) = g, then LCM(a, b) can be calculated as:

A. a × b

B. a × b / g

C. a + b - g

D. (a + b) / g

**Answer:** B

**Explanation:** The relationship between GCD and LCM is: LCM(a, b) × GCD(a, b) = a × b. Therefore, LCM(a, b) = (a × b) / GCD(a, b). This formula helps avoid computing LCM from scratch.

---

### Q10.

In modular arithmetic, what is (37 × 45) mod 10?

A. 5

B. 15

C. 165

D. 1665

**Answer:** A

**Explanation:** We can use the property (a × b) mod m = ((a mod m) × (b mod m)) mod m. So (37 × 45) mod 10 = ((37 mod 10) × (45 mod 10)) mod 10 = (7 × 5) mod 10 = 35 mod 10 = 5.

---

### Q11.

What is 2^10 mod 1000 using binary exponentiation?

A. 24

B. 124

C. 224

D. 324

**Answer:** A

**Explanation:** 2^10 = 1024. Therefore, 1024 mod 1000 = 24. Binary exponentiation computes this efficiently by repeatedly squaring: 2^1=2, 2^2=4, 2^4=16, 2^8=256, 2^10=2^8×2^2=256×4=1024, then 1024 mod 1000 = 24.

---

### Q12.

Which property of modular arithmetic is INCORRECT?

A. (a + b) mod m = ((a mod m) + (b mod m)) mod m

B. (a - b) mod m = ((a mod m) - (b mod m)) mod m

C. (a × b) mod m = ((a mod m) × (b mod m)) mod m

D. (a / b) mod m = ((a mod m) / (b mod m)) mod m

**Answer:** D

**Explanation:** Division does not distribute over modular arithmetic in the same way as addition, subtraction, and multiplication. For division in modular arithmetic, we need to use modular multiplicative inverse: (a / b) mod m = (a × b^(-1)) mod m, where b^(-1) is the modular inverse of b.

---

### Q13.

In the two-pointer technique, when is it most effective to use opposite-directional pointers?

A. Finding duplicates in an unsorted array

B. Finding a pair with a given sum in a sorted array

C. Reversing a linked list

D. Finding the middle element of an array

**Answer:** B

**Explanation:** Opposite-directional pointers (one from start, one from end) work best on sorted arrays for finding pairs. If the sum is too large, move the right pointer left; if too small, move the left pointer right. This gives O(n) time complexity.

---

### Q14.

What is the time complexity of finding the longest substring without repeating characters using sliding window?

A. O(n)

B. O(n log n)

C. O(n²)

D. O(2^n)

**Answer:** A

**Explanation:** Using sliding window with a hash set, we expand the window by moving the right pointer and contract by moving the left pointer when duplicates are found. Each character is visited at most twice (once by right pointer, once by left pointer), giving O(n) time complexity.

---

### Q15.

In a sliding window of fixed size k on an array of size n, how many total windows are there?

A. k

B. n - k

C. n - k + 1

D. n

**Answer:** C

**Explanation:** For an array of size n with window size k, the first window starts at index 0 and the last window starts at index n-k. The number of windows is (n-k) + 1 = n - k + 1. For example, array of size 5 with window size 3 has windows starting at indices 0, 1, 2, which is 3 = 5-3+1.

---

### Q16.

What is the most efficient way to find the maximum sum subarray of size k in an array?

A. Calculate sum of each window separately - O(n × k)

B. Use sliding window to update sum - O(n)

C. Sort and take k largest elements - O(n log n)

D. Use dynamic programming - O(n²)

**Answer:** B

**Explanation:** Sliding window technique is optimal: calculate the sum of first window, then for each subsequent window, subtract the leftmost element of previous window and add the new rightmost element. This gives O(n) time complexity.

---

### Q17.

Which of the following is NOT a valid application of the two-pointer technique?

A. Finding if a string is a palindrome

B. Removing duplicates from a sorted array

C. Finding the kth smallest element in an unsorted array

D. Merging two sorted arrays

**Answer:** C

**Explanation:** Finding the kth smallest element in an unsorted array typically requires sorting O(n log n), heap O(n log k), or quickselect O(n) on average. Two-pointer technique doesn't apply here as it requires some ordered structure or specific property to work with.

---

### Q18.

What is the space complexity of the Sieve of Eratosthenes algorithm to find all primes up to n?

A. O(1)

B. O(log n)

C. O(n)

D. O(n²)

**Answer:** C

**Explanation:** The Sieve of Eratosthenes requires a boolean array of size n to mark whether each number is prime or not. This requires O(n) space complexity.

---

### Q19.

In a 2D array of size m × n, what is the time complexity of finding an element if the array is sorted row-wise and column-wise?

A. O(log(m × n))

B. O(m + n)

C. O(m × n)

D. O(√(m × n))

**Answer:** B

**Explanation:** For a matrix sorted row-wise and column-wise, we can start from top-right corner (or bottom-left). Compare target with current element: if larger, move down; if smaller, move left. Maximum moves = m + n, giving O(m + n) time complexity. This is more efficient than binary search on each row.

---

### Q20.

What does the following modular arithmetic property represent: a^(p-1) ≡ 1 (mod p) where p is prime and gcd(a,p) = 1?

A. Fermat's Little Theorem

B. Wilson's Theorem

C. Euler's Theorem

D. Chinese Remainder Theorem

**Answer:** A

**Explanation:** Fermat's Little Theorem states that if p is prime and a is not divisible by p, then a^(p-1) ≡ 1 (mod p). This is useful for finding modular inverses and in cryptography. For example, to find a^(-1) mod p, we can compute a^(p-2) mod p.

---

### Q21.

Which string algorithm uses a hash function to find patterns?

A. KMP Algorithm

B. Rabin-Karp Algorithm

C. Z-Algorithm

D. Aho-Corasick Algorithm

**Answer:** B

**Explanation:** Rabin-Karp algorithm uses rolling hash to compare pattern with substrings of text. It computes hash of pattern and compares with hash of each text window. If hashes match, it verifies character by character. Average time complexity is O(n + m) but worst case is O(n × m).

---

### Q22.

What is the maximum number of subarrays possible in an array of size n?

A. n

B. n²

C. n(n+1)/2

D. 2^n

**Answer:** C

**Explanation:** A subarray is a contiguous portion of an array. For each starting position i (from 0 to n-1), we can have (n-i) subarrays. Total = n + (n-1) + (n-2) + ... + 1 = n(n+1)/2. For example, array [1,2,3] has 6 subarrays: [1], [2], [3], [1,2], [2,3], [1,2,3].

---

### Q23.

In the Dutch National Flag problem (sorting an array of 0s, 1s, and 2s), what is the optimal time complexity?

A. O(n log n)

B. O(n)

C. O(n²)

D. O(3n)

**Answer:** B

**Explanation:** Using three pointers (low, mid, high), we can sort in a single pass: 0s go to low section, 2s go to high section, 1s stay in middle. Each element is visited once, giving O(n) time complexity with O(1) space. This is optimal for this problem.

---

### Q24.

What is the time complexity of computing GCD of two numbers using the Euclidean algorithm?

A. O(1)

B. O(log(min(a, b)))

C. O(min(a, b))

D. O(a + b)

**Answer:** B

**Explanation:** Euclidean algorithm: GCD(a, b) = GCD(b, a mod b). The number of recursive calls is proportional to the number of digits in the smaller number, which is O(log(min(a, b))). This is very efficient even for large numbers.

---

### Q25.

Which of the following problems can be solved efficiently using the sliding window technique?

A. Finding longest substring with at most k distinct characters

B. Finding the median of an array

C. Finding prime factors of a number

D. Checking if a graph is bipartite

**Answer:** A

**Explanation:** Finding longest substring with at most k distinct characters is a classic sliding window problem. We expand window by adding characters and contract when distinct characters exceed k, maintaining a character frequency map. This gives O(n) time complexity.

---

### Q26.

What is the result of 5^3 mod 7 using fast binary exponentiation?

A. 6

B. 5

C. 4

D. 3

**Answer:** A

**Explanation:** 5^3 = 125. Then 125 mod 7 = 125 - (17 × 7) = 125 - 119 = 6. Using binary exponentiation: 5^1=5, 5^2=(5×5)mod7=25mod7=4, 5^3=(5^2×5)mod7=(4×5)mod7=20mod7=6.

---

### Q27.

In a string, what is the maximum number of palindromic substrings possible?

A. n

B. n²

C. n(n+1)/2

D. 2^n - 1

**Answer:** C

**Explanation:** Every substring can potentially be a palindrome. The number of substrings in a string of length n is n(n+1)/2 (same as subarrays). Each character is a palindrome, and there can be multi-character palindromes. The upper bound is n(n+1)/2.

---

### Q28.

Which technique is used to find all anagrams of a pattern in a text?

A. Two pointers with sorting

B. Sliding window with character frequency map

C. Binary search

D. Divide and conquer

**Answer:** B

**Explanation:** To find all anagram occurrences, use a sliding window of size equal to pattern length, maintaining character frequency counts. Compare window's frequency with pattern's frequency at each position. This gives O(n) time complexity where n is text length.

---

### Q29.

What is the time complexity of transposing an m × n matrix?

A. O(1)

B. O(m + n)

C. O(m × n)

D. O(min(m, n))

**Answer:** C

**Explanation:** Transposing a matrix requires swapping rows and columns: result[j][i] = matrix[i][j] for all i and j. This requires visiting every element once, giving O(m × n) time complexity. If done in-place for square matrix, space is O(1), otherwise O(m × n) space needed.

---

### Q30.

In the two-pointer technique for finding triplets with sum equal to target in a sorted array, what is the overall time complexity?

A. O(n)

B. O(n²)

C. O(n³)

D. O(n log n)

**Answer:** B

**Explanation:** Fix one element and use two pointers for remaining array to find pair with required sum. For each of n elements, the two-pointer scan takes O(n) time. Total: O(n) × O(n) = O(n²). If array is unsorted, add O(n log n) for sorting, but overall remains O(n²).

---

**End of MCQ Questions**
