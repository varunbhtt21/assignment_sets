# Searching (Linear Search and Binary Search) & Bits Manipulation - MCQ Questions

---

### Q1.

What is the time complexity of Linear Search in the worst case?

A. O(1)

B. O(log n)

C. O(n)

D. O(n²)

**Answer:** C

**Explanation:** Linear search checks each element sequentially, so in the worst case it needs to check all n elements.

---

### Q2.

Which searching algorithm is best suited for an **unsorted** array?

A. Binary Search

B. Linear Search

C. Jump Search

D. Interpolation Search

**Answer:** B

**Explanation:** Linear search works on both sorted and unsorted arrays, while binary search requires a sorted array.

---

### Q3.

What will be the output of linear search for the target 5 in array [3, 7, 1, 5, 9]?

A. -1

B. 0

C. 3

D. 5

**Answer:** C

**Explanation:** Linear search returns the index where element is found. Element 5 is at index 3 (0-indexed).

---

### Q4.

In the best case, what is the time complexity of Linear Search?

A. O(1)

B. O(log n)

C. O(n)

D. O(n log n)

**Answer:** A

**Explanation:** Best case occurs when the target element is at the first position, requiring only one comparison.

---

### Q5.

What is the space complexity of Linear Search?

A. O(1)

B. O(log n)

C. O(n)

D. O(n²)

**Answer:** A

**Explanation:** Linear search uses only a constant amount of extra space regardless of input size.

---

### Q6.

Which statement is **true** about Linear Search?

A. It only works on sorted arrays

B. It requires extra space proportional to input size

C. It can find multiple occurrences by continuing the search

D. It has O(log n) average time complexity

**Answer:** C

**Explanation:** Linear search can be modified to find all occurrences by not stopping after finding the first match.

---

### Q7.

How many comparisons are needed in the worst case to find an element in an array of size 100 using linear search?

A. 1

B. 10

C. 50

D. 100

**Answer:** D

**Explanation:** In the worst case (element not present or at the last position), all 100 elements must be checked.

---

### Q8.

What is returned when linear search doesn't find the target element?

A. 0

B. -1

C. null

D. Length of array

**Answer:** B

**Explanation:** By convention, -1 is returned to indicate the element was not found (since -1 is not a valid array index).

---

### Q9.

Which of the following is an advantage of Linear Search over Binary Search?

A. Faster for large datasets

B. Works on unsorted arrays

C. Uses less memory

D. Has better worst-case complexity

**Answer:** B

**Explanation:** Linear search doesn't require the array to be sorted, while binary search does.

---

### Q10.

What is the average case time complexity of Linear Search?

A. O(1)

B. O(n/2)

C. O(n)

D. O(log n)

**Answer:** C

**Explanation:** On average, we check n/2 elements, but in Big-O notation, we drop constants, so it's O(n).

---

### Q11.

What is the **prerequisite** for applying Binary Search?

A. Array must be sorted

B. Array must have unique elements

C. Array size must be power of 2

D. Array must be of integer type

**Answer:** A

**Explanation:** Binary search only works correctly on sorted arrays.

---

### Q12.

What is the time complexity of Binary Search?

A. O(n)

B. O(log n)

C. O(n log n)

D. O(1)

**Answer:** B

**Explanation:** Binary search divides the search space in half with each comparison, leading to logarithmic time complexity.

---

### Q13.

In a sorted array of 1024 elements, what is the maximum number of comparisons needed in binary search?

A. 10

B. 512

C. 1024

D. 11

**Answer:** A

**Explanation:** log‚(1024) = 10, so at most 10 comparisons are needed.

---

### Q14.

What will binary search return when searching for 15 in the sorted array [2, 5, 8, 12, 16, 23, 38]?

A. 3

B. 4

C. -1

D. 15

**Answer:** C

**Explanation:** 15 is not present in the array, so binary search returns -1.

---

### Q15.

Which statement about Binary Search is **false**?

A. It works on sorted arrays

B. Time complexity is O(log n)

C. It uses divide and conquer approach

D. It always finds the first occurrence of a duplicate element

**Answer:** D

**Explanation:** Standard binary search may find any occurrence of a duplicate element, not necessarily the first one.

---

### Q16.

What is the space complexity of iterative binary search?

A. O(1)

B. O(log n)

C. O(n)

D. O(n log n)

**Answer:** A

**Explanation:** Iterative binary search uses only a constant amount of extra space for variables like left, right, and mid.

---

### Q17.

What is the space complexity of recursive binary search?

A. O(1)

B. O(log n)

C. O(n)

D. O(n²)

**Answer:** B

**Explanation:** Recursive binary search uses call stack space proportional to the recursion depth, which is O(log n).

---

### Q18.

In binary search, if the array has 16 elements, how many times will the search space be divided?

A. 2

B. 4

C. 8

D. 16

**Answer:** B

**Explanation:** 16 ’ 8 ’ 4 ’ 2 ’ 1, which is 4 divisions (log‚(16) = 4).

---

### Q19.

What happens if binary search is applied to an **unsorted** array?

A. It will work correctly but slower

B. It will give incorrect results

C. It will throw an exception

D. It will automatically sort the array first

**Answer:** B

**Explanation:** Binary search assumes the array is sorted. On an unsorted array, it may miss elements or return incorrect results.

---

### Q20.

Which searching algorithm is more efficient for a sorted array of 1 million elements?

A. Linear Search

B. Binary Search

C. Both are equally efficient

D. Depends on the target element

**Answer:** B

**Explanation:** Binary search requires at most log‚(1,000,000) H 20 comparisons, while linear search may need up to 1 million.

---

### Q21.

What is the correct formula to calculate mid index in binary search to avoid integer overflow?

A. `mid = (left + right) / 2`

B. `mid = left + (right - left) / 2`

C. `mid = (left * right) / 2`

D. `mid = right - (right - left) / 2`

**Answer:** B

**Explanation:** Using `left + (right - left) / 2` prevents integer overflow that can occur with `(left + right) / 2`.

---

### Q22.

How would you modify binary search to find the **first occurrence** of a duplicate element?

A. Continue searching in the right half after finding the element

B. Continue searching in the left half after finding the element

C. Stop immediately when element is found

D. Cannot be done with binary search

**Answer:** B

**Explanation:** To find the first occurrence, continue searching in the left half even after finding the element to check for earlier occurrences.

---

### Q23.

What is the correct condition to find the **last occurrence** in binary search?

A. Continue searching right after finding the element

B. Continue searching left after finding the element

C. Return immediately after finding

D. Use linear search instead

**Answer:** A

**Explanation:** To find the last occurrence, continue searching in the right half to check for later occurrences.

---

### Q24.

In rotated sorted array [4, 5, 6, 7, 0, 1, 2], where is the pivot point?

A. Index 3

B. Index 4

C. Index 5

D. Index 0

**Answer:** A

**Explanation:** The pivot is at index 3 (element 7), after which the array rotates. Alternatively, some consider index 4 (smallest element) as the rotation point.

---

### Q25.

What approach is used to search in a rotated sorted array?

A. Linear search only

B. Modified binary search

C. Two binary searches

D. Sorting first, then binary search

**Answer:** B

**Explanation:** Modified binary search can find elements in O(log n) time by identifying which half is sorted.

---

### Q26.

What is the time complexity to find the square root of a number using binary search?

A. O(1)

B. O(log n)

C. O(n)

D. O(n²)

**Answer:** B

**Explanation:** Binary search on the range [0, n] to find square root takes O(log n) time.

---

### Q27.

In binary search on answer (search space technique), what do we search for?

A. Index of element

B. The answer value itself within a range

C. Number of elements

D. Median of array

**Answer:** B

**Explanation:** Binary search on answer searches for the optimal answer value within a possible range, not an array index.

---

### Q28.

Which problem can be solved using binary search?

A. Finding peak element in an array

B. Sorting an array

C. Reversing an array

D. Removing duplicates

**Answer:** A

**Explanation:** Peak element can be found using binary search in O(log n) time by comparing middle element with neighbors.

---

### Q29.

What is the time complexity of searching in a 2D matrix where each row and column is sorted?

A. O(n²)

B. O(n + m) where n=rows, m=columns

C. O(log n + log m)

D. O(n × m)

**Answer:** B

**Explanation:** Starting from top-right or bottom-left corner, we can search in O(n + m) time by eliminating either a row or column in each step.

---

### Q30.

In binary search, what is the condition to terminate the loop?

A. `left < right`

B. `left <= right`

C. `left > right`

D. `left == right`

**Answer:** B

**Explanation:** The loop continues while `left <= right`. When `left > right`, it means the search space is exhausted.

---

**End of MCQ Questions**
