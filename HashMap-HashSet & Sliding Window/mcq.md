# HashMap/HashSet & Sliding Window - MCQ Questions

---

### Q1.

What is the average time complexity for inserting an element into a HashMap?

A. O(1)

B. O(log n)

C. O(n)

D. O(n²)

**Answer:** A

**Explanation:** HashMap uses hashing to store elements, providing O(1) average time complexity for insertion, search, and deletion operations.

---

### Q2.

What is the main difference between HashMap and HashSet?

A. HashMap stores key-value pairs, HashSet stores only values

B. HashMap is faster than HashSet

C. HashSet allows duplicate values

D. HashMap uses trees internally

**Answer:** A

**Explanation:** HashMap stores key-value pairs while HashSet stores only unique values. HashSet internally uses a HashMap where values are stored as keys.

---

### Q3.

What happens when two keys produce the same hash code in a HashMap?

A. The second key overwrites the first

B. An error is thrown

C. Collision handling occurs (typically chaining or open addressing)

D. The HashMap automatically resizes

**Answer:** C

**Explanation:** When two keys produce the same hash code (collision), HashMap uses collision handling mechanisms like chaining (linked lists) or open addressing to store both entries.

---

### Q4.

Which data structure does HashSet use internally in Java?

A. Array

B. LinkedList

C. HashMap

D. TreeMap

**Answer:** C

**Explanation:** HashSet internally uses HashMap where the elements are stored as keys with a dummy constant value.

---

### Q5.

What is the worst-case time complexity for searching in a HashMap?

A. O(1)

B. O(log n)

C. O(n)

D. O(n²)

**Answer:** C

**Explanation:** In the worst case, when all keys hash to the same bucket (hash collision), searching requires traversing all elements, resulting in O(n) time complexity.

---

### Q6.

Can a HashMap contain duplicate keys?

A. Yes, multiple values can have the same key

B. No, each key must be unique; new values overwrite old ones

C. Yes, but only for null keys

D. It depends on the implementation

**Answer:** B

**Explanation:** HashMap does not allow duplicate keys. If you insert a value with an existing key, the new value overwrites the old value for that key.

---

### Q7.

What is the space complexity of a HashMap with n elements?

A. O(1)

B. O(log n)

C. O(n)

D. O(n²)

**Answer:** C

**Explanation:** HashMap requires O(n) space to store n key-value pairs, plus additional space for the internal array structure.

---

### Q8.

Which method checks if a key exists in a HashMap?

A. contains()

B. containsKey()

C. hasKey()

D. exists()

**Answer:** B

**Explanation:** The containsKey() method checks if a specific key exists in the HashMap and returns a boolean value.

---

### Q9.

What is the load factor in a HashMap?

A. The number of elements in the HashMap

B. A measure of how full the HashMap is allowed to get before resizing

C. The speed of hash function computation

D. The number of collisions

**Answer:** B

**Explanation:** Load factor is the ratio of number of elements to the capacity. When this threshold is exceeded (typically 0.75), the HashMap resizes to maintain performance.

---

### Q10.

Can a HashSet contain null values?

A. No, HashSet doesn't allow null

B. Yes, exactly one null value is allowed

C. Yes, multiple null values are allowed

D. It depends on the Java version

**Answer:** B

**Explanation:** HashSet allows at most one null element since it doesn't allow duplicates and null is considered a unique value.

---

### Q11.

What is the Sliding Window technique?

A. A method to sort arrays efficiently

B. A technique to process subarrays or sublists by maintaining a window that slides through the data

C. A way to implement hash tables

D. A tree traversal method

**Answer:** B

**Explanation:** Sliding Window is a technique where a window (subarray) of fixed or variable size slides through the data structure to solve problems efficiently, typically reducing time complexity from O(n²) to O(n).

---

### Q12.

What is the time complexity of finding the maximum sum of a subarray of size k using the sliding window technique?

A. O(n²)

B. O(n log n)

C. O(n)

D. O(k)

**Answer:** C

**Explanation:** Using sliding window, we calculate the sum of the first window in O(k), then slide the window by removing the leftmost element and adding the rightmost element, processing the entire array in O(n) time.

---

### Q13.

Which type of problems are best suited for the sliding window technique?

A. Finding shortest paths in graphs

B. Subarray/substring problems with consecutive elements

C. Sorting problems

D. Tree traversal problems

**Answer:** B

**Explanation:** Sliding window is ideal for problems involving contiguous subarrays or substrings where we need to find maximum, minimum, or specific conditions within a range.

---

### Q14.

In a fixed-size sliding window problem, how do we move the window forward?

A. Recalculate the entire window from scratch

B. Remove the leftmost element and add the next rightmost element

C. Sort the window elements

D. Use binary search

**Answer:** B

**Explanation:** To maintain O(n) complexity, we slide the window by removing the element that's leaving the window (leftmost) and adding the new element entering the window (rightmost).

---

### Q15.

What is a variable-size sliding window?

A. A window that changes size at random

B. A window whose size changes based on certain conditions while sliding

C. A window that only increases in size

D. A window that is always size 1

**Answer:** B

**Explanation:** In variable-size sliding window problems, the window expands or contracts based on problem conditions (e.g., finding longest substring with k distinct characters).

---

### Q16.

For the problem "longest substring without repeating characters", which data structure is most helpful?

A. Array only

B. HashMap or HashSet to track seen characters

C. Stack

D. Queue only

**Answer:** B

**Explanation:** HashMap/HashSet helps track which characters we've seen and their positions, allowing us to efficiently detect duplicates and adjust the window.

---

### Q17.

What is the space complexity of the sliding window technique?

A. Always O(1)

B. Always O(n)

C. O(1) for fixed window, can be O(k) or O(n) for variable window with additional data structures

D. O(n²)

**Answer:** C

**Explanation:** Fixed-size windows with simple operations use O(1) space. Variable windows may need O(k) space for tracking window contents or O(n) if storing all elements.

---

### Q18.

In the problem "find all anagrams in a string", which approach is most efficient?

A. Generate all permutations - O(n!)

B. Sliding window with character frequency map - O(n)

C. Sort each substring - O(n² log n)

D. Brute force comparison - O(n²)

**Answer:** B

**Explanation:** Using a fixed-size sliding window equal to the pattern length, combined with a character frequency map, we can find anagrams in O(n) time.

---

### Q19.

What is the two-pointer technique in relation to sliding window?

A. They are unrelated concepts

B. Two pointers often implement sliding window (left and right boundaries)

C. Two pointers is slower than sliding window

D. Two pointers only works on sorted arrays

**Answer:** B

**Explanation:** Sliding window is often implemented using two pointers (left and right) that define the window boundaries. Two pointers is a broader technique that includes sliding window as a special case.

---

### Q20.

For the problem "maximum sum subarray of size k", after calculating the first window sum, what's the next step?

A. Calculate sum of next k elements from scratch

B. Subtract the leftmost element of previous window and add the next element

C. Use binary search

D. Sort the array

**Answer:** B

**Explanation:** This is the essence of sliding window optimization: sum_new = sum_old - arr[left] + arr[right+1], maintaining O(1) per slide operation.

---

### Q21.

What is the time complexity of checking if an element exists in a HashSet?

A. O(n)

B. O(log n)

C. O(1) average case

D. O(n²)

**Answer:** C

**Explanation:** HashSet provides O(1) average-case time complexity for search operations due to hashing, though worst case is O(n) with many collisions.

---

### Q22.

In the "two sum" problem, why is HashMap preferred over a nested loop?

A. HashMap uses less memory

B. HashMap reduces time complexity from O(n²) to O(n)

C. HashMap guarantees finding a solution

D. HashMap sorts the data automatically

**Answer:** B

**Explanation:** HashMap allows us to check if the complement (target - current) exists in O(1) time, reducing overall complexity from O(n²) (nested loops) to O(n) (single pass with HashMap lookups).

---

### Q23.

What happens when a HashMap's load factor threshold is exceeded?

A. It throws an exception

B. It stops accepting new elements

C. It rehashes and increases capacity (typically doubles)

D. It converts to a TreeMap

**Answer:** C

**Explanation:** When load factor exceeds the threshold (default 0.75), HashMap rehashes all entries into a larger array (typically double the size) to maintain performance.

---

### Q24.

For finding the "longest substring with at most k distinct characters", what type of sliding window is used?

A. Fixed-size window

B. Variable-size expanding window

C. No window needed

D. Multiple fixed windows

**Answer:** B

**Explanation:** This requires a variable-size window that expands when conditions are met (distinct chars ≤ k) and contracts when exceeded, along with a HashMap to track character frequencies.

---

### Q25.

What is the advantage of using HashMap over sorting for the "group anagrams" problem?

A. HashMap uses less space

B. HashMap approach is O(n*k) vs sorting approach O(n*k*log k) where k is string length

C. HashMap guarantees correct results

D. Sorting doesn't work for this problem

**Answer:** B

**Explanation:** Using sorted string as key in HashMap gives O(n*k*log k) complexity. Using character frequency as key (or count array) gives O(n*k) complexity, which is better.

---

### Q26.

In sliding window problems, when do we expand the window vs contract it?

A. Randomly

B. Expand when condition is met/valid, contract when condition is violated

C. Always expand first, then contract

D. Only expand, never contract

**Answer:** B

**Explanation:** Variable sliding window expands (right pointer moves) when the window satisfies the condition and contracts (left pointer moves) when the condition is violated.

---

### Q27.

What is the purpose of using a HashMap in the "minimum window substring" problem?

A. To store the window elements

B. To track required character frequencies and current window frequencies

C. To sort the characters

D. To find the length

**Answer:** B

**Explanation:** HashMap tracks required character frequencies from the pattern and current window frequencies, helping us determine when we have a valid window containing all required characters.

---

### Q28.

Which statement about HashMap iteration order is TRUE?

A. HashMap maintains insertion order

B. HashMap maintains sorted order

C. HashMap has no guaranteed order

D. HashMap maintains reverse insertion order

**Answer:** C

**Explanation:** HashMap does not guarantee any specific iteration order. LinkedHashMap maintains insertion order, and TreeMap maintains sorted order.

---

### Q29.

For the problem "find first non-repeating character", which approach is most efficient?

A. Nested loops - O(n²)

B. Sorting - O(n log n)

C. HashMap to count frequencies, then find first with count 1 - O(n)

D. Binary search - O(log n)

**Answer:** C

**Explanation:** Using HashMap, we can count character frequencies in O(n), then iterate through the string again in O(n) to find the first character with frequency 1, giving overall O(n) complexity.

---

### Q30.

What is the maximum number of times the right pointer moves in a sliding window algorithm for an array of size n?

A. n²

B. 2n

C. n

D. n-1

**Answer:** D

**Explanation:** The right pointer starts at 0 and can move at most to index n-1, making at most n-1 moves. Combined with left pointer movements, total operations remain O(n).

---

**End of MCQ Questions**
