# Major Assessment -03 - MCQ Questions
## (Sorting, Hashmap and Hashset, Two Pointers and Sliding Window)

---

### Q1.

What is the time complexity of merge sort in the worst case?

A. O(n)

B. O(n log n)

C. O(n²)

D. O(log n)

**Answer:** B

**Explanation:** Merge sort divides the array into two halves (log n levels) and merges them (n operations per level), resulting in O(n log n) time complexity in all cases (best, average, and worst).

---

### Q2.

Which sorting algorithm is most efficient for nearly sorted arrays?

A. Merge Sort

B. Quick Sort

C. Insertion Sort

D. Heap Sort

**Answer:** C

**Explanation:** Insertion sort performs exceptionally well on nearly sorted arrays with time complexity close to O(n) because most elements are already in their correct positions, requiring minimal swaps.

---

### Q3.

What is a hash collision?

A. When two different keys produce the same hash value

B. When a hash table is full

C. When a key is not found in the hash table

D. When the hash function returns null

**Answer:** A

**Explanation:** A hash collision occurs when two different keys hash to the same index in the hash table. This is handled using techniques like chaining (linked lists) or open addressing (probing).

---

### Q4.

What is the average time complexity for insertion in a HashMap?

A. O(1)

B. O(log n)

C. O(n)

D. O(n log n)

**Answer:** A

**Explanation:** HashMap uses hashing to compute the index in constant time O(1) on average. In the worst case with many collisions, it can degrade to O(n), but with a good hash function, average case is O(1).

---

### Q5.

What is the main difference between HashMap and HashSet?

A. HashMap stores key-value pairs, HashSet stores only values

B. HashMap is slower than HashSet

C. HashSet allows duplicate values

D. HashMap cannot handle null values

**Answer:** A

**Explanation:** HashMap stores key-value pairs and allows retrieval by key, while HashSet stores only unique values (no duplicates) and is backed by a HashMap internally (values are stored as keys with a dummy object as value).

---

### Q6.

In the two-pointer technique, when should you use opposite-directional pointers?

A. Finding pairs in an unsorted array

B. Finding pairs with a specific sum in a sorted array

C. Finding duplicates in an array

D. Reversing a linked list

**Answer:** B

**Explanation:** Opposite-directional pointers (one from start, one from end) are effective for finding pairs in sorted arrays. If the sum is too large, move the right pointer left; if too small, move the left pointer right.

---

### Q7.

What is the time complexity of the two-pointer approach for finding a pair with a given sum in a sorted array?

A. O(n²)

B. O(n log n)

C. O(n)

D. O(1)

**Answer:** C

**Explanation:** The two-pointer approach traverses the sorted array once with pointers moving from both ends, resulting in O(n) time complexity, which is much better than the brute force O(n²) approach.

---

### Q8.

What is a sliding window?

A. A fixed-size subarray that moves through the array

B. A sorting technique

C. A type of hash table

D. A binary search variant

**Answer:** A

**Explanation:** A sliding window is a technique where a window (subarray) of fixed or variable size slides through the array. It's used to find subarrays with specific properties efficiently, avoiding redundant calculations.

---

### Q9.

What is the time complexity of finding the maximum sum subarray of size k using the sliding window technique?

A. O(n * k)

B. O(n²)

C. O(n)

D. O(k)

**Answer:** C

**Explanation:** Sliding window computes the sum of the first window in O(k) time, then slides by removing the leftmost element and adding the rightmost element for each subsequent window, taking O(1) per slide, resulting in O(n) total time.

---

### Q10.

Which data structure is typically used to check for duplicate values efficiently in a HashSet?

A. Array

B. Linked List

C. Hash Table

D. Binary Tree

**Answer:** C

**Explanation:** HashSet is internally implemented using a hash table, which provides O(1) average time complexity for checking if a value exists, making duplicate detection very efficient.

---

### Q11.

What is the space complexity of quick sort in the average case?

A. O(1)

B. O(log n)

C. O(n)

D. O(n log n)

**Answer:** B

**Explanation:** Quick sort is an in-place sorting algorithm but uses recursion. The recursion stack depth in the average case is O(log n) due to balanced partitioning, making the space complexity O(log n).

---

### Q12.

Which sorting algorithm has the best worst-case time complexity?

A. Quick Sort

B. Merge Sort

C. Bubble Sort

D. Selection Sort

**Answer:** B

**Explanation:** Merge sort has O(n log n) time complexity in all cases (best, average, worst). Quick sort's worst case is O(n²), while bubble and selection sort are O(n²) in all non-trivial cases.

---

### Q13.

What is the load factor in a HashMap?

A. The ratio of number of entries to table size

B. The maximum number of collisions allowed

C. The number of buckets in the table

D. The initial capacity of the HashMap

**Answer:** A

**Explanation:** Load factor = (number of entries) / (table size). When the load factor exceeds a threshold (typically 0.75), the HashMap is resized (rehashed) to maintain O(1) performance.

---

### Q14.

In which scenario is the sliding window technique most useful?

A. Finding all permutations of a string

B. Finding the longest substring without repeating characters

C. Sorting an array

D. Finding the median of an array

**Answer:** B

**Explanation:** Sliding window is perfect for substring/subarray problems with specific constraints. For longest substring without repeating characters, we expand the window when characters are unique and contract when duplicates appear.

---

### Q15.

What is the worst-case time complexity of quick sort?

A. O(n)

B. O(n log n)

C. O(n²)

D. O(log n)

**Answer:** C

**Explanation:** Quick sort's worst case occurs when the pivot is always the smallest or largest element, causing unbalanced partitions. This results in O(n²) comparisons, similar to selection sort.

---

### Q16.

Which of the following is true about stable sorting algorithms?

A. They preserve the relative order of equal elements

B. They always have O(n log n) complexity

C. They require extra space

D. They are faster than unstable algorithms

**Answer:** A

**Explanation:** A stable sort maintains the relative order of elements with equal keys. For example, merge sort and insertion sort are stable, while quick sort and heap sort are typically unstable.

---

### Q17.

What is the advantage of using a HashSet over an array for checking duplicates?

A. HashSet uses less memory

B. HashSet provides O(1) lookup time on average

C. HashSet maintains insertion order

D. HashSet can store any data type

**Answer:** B

**Explanation:** HashSet provides O(1) average-case lookup time using hashing, while checking duplicates in an array requires O(n) time for each lookup, resulting in O(n²) for checking all elements.

---

### Q18.

In the two-pointer technique for removing duplicates from a sorted array, what do the two pointers represent?

A. Start and end of the array

B. Current position and next unique element position

C. First and last duplicate

D. Minimum and maximum values

**Answer:** B

**Explanation:** One pointer tracks the position for the next unique element (slow pointer), while the other pointer scans through the array (fast pointer). When a unique element is found, it's placed at the slow pointer's position.

---

### Q19.

What is the time complexity of finding if two strings are isomorphic using a HashMap?

A. O(1)

B. O(n)

C. O(n²)

D. O(n log n)

**Answer:** B

**Explanation:** Checking isomorphic strings requires one pass through both strings (O(n)) to build and verify the character mappings using two HashMaps, ensuring bijective (one-to-one) mapping.

---

### Q20.

Which technique is best suited for finding the maximum sum of any contiguous subarray?

A. Two Pointers

B. Sliding Window

C. Kadane's Algorithm

D. Binary Search

**Answer:** C

**Explanation:** Kadane's Algorithm is specifically designed for the maximum subarray sum problem and works in O(n) time. While it conceptually uses a sliding window, it's a specialized algorithm with specific rules for expanding/contracting.

---

### Q21.

What is chaining in hash tables?

A. Linking multiple hash tables together

B. Using linked lists to handle collisions at the same index

C. Connecting keys to values

D. Sorting elements by hash value

**Answer:** B

**Explanation:** Chaining resolves hash collisions by maintaining a linked list at each bucket. When multiple keys hash to the same index, they're stored in a linked list at that bucket.

---

### Q22.

What is the time complexity of heap sort?

A. O(n)

B. O(n log n)

C. O(n²)

D. O(log n)

**Answer:** B

**Explanation:** Heap sort builds a heap in O(n) time, then extracts the maximum n times, each taking O(log n) time for heapify operation, resulting in O(n log n) total time complexity.

---

### Q23.

In a variable-size sliding window, when do you typically expand the window?

A. When the window violates a constraint

B. When the window satisfies a constraint

C. At fixed intervals

D. Randomly

**Answer:** B

**Explanation:** In variable sliding windows, you expand (move right pointer) when the current window satisfies the constraint, and contract (move left pointer) when it violates the constraint, optimizing for the desired property.

---

### Q24.

What is open addressing in hash tables?

A. Making the hash table publicly accessible

B. Finding another slot when a collision occurs

C. Using multiple hash functions

D. Resizing the table automatically

**Answer:** B

**Explanation:** Open addressing resolves collisions by probing for the next available slot. Common probing techniques include linear probing (next slot), quadratic probing (i² slots away), and double hashing.

---

### Q25.

Which sorting algorithm is most suitable when stability is required and space is not a constraint?

A. Quick Sort

B. Heap Sort

C. Merge Sort

D. Selection Sort

**Answer:** C

**Explanation:** Merge sort is stable and guarantees O(n log n) time complexity but requires O(n) extra space. Quick sort is faster in practice but unstable, while heap sort is in-place but also unstable.

---

### Q26.

What is the purpose of the "contains" method in a HashSet?

A. To check if an element exists in the set

B. To add an element to the set

C. To remove an element from the set

D. To get the size of the set

**Answer:** A

**Explanation:** The contains() method checks if a specific element exists in the HashSet, returning true if present and false otherwise, with O(1) average time complexity using hashing.

---

### Q27.

In the context of sorting, what is a pivot?

A. The middle element of the array

B. An element used to partition the array in quick sort

C. The largest element in the array

D. A temporary variable for swapping

**Answer:** B

**Explanation:** In quick sort, the pivot is an element chosen to partition the array such that elements smaller than the pivot go to its left and larger elements go to its right. Pivot selection strategies affect performance.

---

### Q28.

What is the time complexity of checking if a substring of length k exists in a string using a sliding window with a HashSet?

A. O(n * k)

B. O(n)

C. O(k)

D. O(n²)

**Answer:** B

**Explanation:** Using a sliding window, we maintain a HashSet of the current window. For each slide, we remove one character and add one character (both O(1)), checking the set for the property. Total time is O(n).

---

### Q29.

Which statement is true about counting sort?

A. It is a comparison-based sorting algorithm

B. It works efficiently when the range of input values is small

C. It has O(n log n) time complexity

D. It is an in-place sorting algorithm

**Answer:** B

**Explanation:** Counting sort is a non-comparison based algorithm that counts occurrences of each value. It's efficient when the range k of values is small, with time complexity O(n + k), but requires O(k) extra space.

---

### Q30.

What is the main advantage of using two pointers over nested loops for array problems?

A. It uses less memory

B. It reduces time complexity from O(n²) to O(n)

C. It makes the code shorter

D. It handles negative numbers better

**Answer:** B

**Explanation:** Two pointers can solve many problems that would require nested loops (O(n²)) in just one pass (O(n)) by intelligently moving pointers based on conditions, especially effective on sorted arrays.

---

**End of MCQ Questions**
