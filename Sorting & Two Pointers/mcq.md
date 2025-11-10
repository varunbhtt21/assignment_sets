# Sorting & Two Pointers - MCQ Questions

---

### Q1.

What is the time complexity of Bubble Sort in the worst case?

A. O(n)

B. O(n log n)

C. O(n²)

D. O(n³)

**Answer:** C

**Explanation:** Bubble Sort has a worst-case time complexity of O(n²) because it uses nested loops to compare and swap adjacent elements.

---

### Q2.

Which sorting algorithm is considered stable?

A. Quick Sort

B. Heap Sort

C. Merge Sort

D. Selection Sort

**Answer:** C

**Explanation:** Merge Sort is stable because it maintains the relative order of equal elements. Quick Sort and Heap Sort are not stable by default, and Selection Sort is also unstable.

---

### Q3.

What is the space complexity of Merge Sort?

A. O(1)

B. O(log n)

C. O(n)

D. O(n²)

**Answer:** C

**Explanation:** Merge Sort requires O(n) additional space for the temporary arrays used during the merge process.

---

### Q4.

Which sorting algorithm has the best average-case time complexity?

A. Bubble Sort - O(n²)

B. Insertion Sort - O(n²)

C. Quick Sort - O(n log n)

D. Selection Sort - O(n²)

**Answer:** C

**Explanation:** Quick Sort has an average-case time complexity of O(n log n), which is better than the O(n²) complexity of Bubble, Insertion, and Selection Sort.

---

### Q5.

What is a stable sorting algorithm?

A. An algorithm that always runs in O(n log n) time

B. An algorithm that maintains the relative order of equal elements

C. An algorithm that uses constant space

D. An algorithm that never fails

**Answer:** B

**Explanation:** A stable sorting algorithm preserves the relative order of records with equal keys (values).

---

### Q6.

Which sorting algorithm is best for nearly sorted data?

A. Quick Sort

B. Heap Sort

C. Insertion Sort

D. Merge Sort

**Answer:** C

**Explanation:** Insertion Sort has O(n) time complexity for nearly sorted data, making it very efficient for such cases.

---

### Q7.

What is the pivot element in Quick Sort?

A. Always the first element

B. Always the middle element

C. An element chosen to partition the array

D. The smallest element

**Answer:** C

**Explanation:** The pivot is an element chosen to partition the array into two sub-arrays. The choice of pivot can vary (first, last, middle, random, or median).

---

### Q8.

Which of the following is NOT a comparison-based sorting algorithm?

A. Merge Sort

B. Quick Sort

C. Counting Sort

D. Heap Sort

**Answer:** C

**Explanation:** Counting Sort is a non-comparison-based sorting algorithm that counts occurrences of each value. The others use comparisons.

---

### Q9.

What is the time complexity of Heap Sort in all cases?

A. O(n)

B. O(n log n)

C. O(n²)

D. O(log n)

**Answer:** B

**Explanation:** Heap Sort consistently runs in O(n log n) time for best, average, and worst cases.

---

### Q10.

In the Dutch National Flag problem with three colors (0, 1, 2), what is the optimal time complexity?

A. O(n²)

B. O(n log n)

C. O(n)

D. O(1)

**Answer:** C

**Explanation:** The Dutch National Flag problem can be solved in O(n) time using three pointers (low, mid, high) with a single pass through the array.

---

### Q11.

What is the Two Pointers technique?

A. Using two variables to store data

B. Using two indices to traverse an array from different positions

C. Using two arrays for comparison

D. Using two nested loops

**Answer:** B

**Explanation:** Two Pointers is a technique where two indices traverse an array, often from opposite ends or at different speeds, to solve problems efficiently.

---

### Q12.

When is the Two Pointers technique most useful?

A. For unsorted arrays only

B. For sorted arrays or when finding pairs/triplets

C. For tree traversals

D. For graph algorithms

**Answer:** B

**Explanation:** Two Pointers is particularly effective on sorted arrays and for finding pairs, triplets, or subarrays that satisfy certain conditions.

---

### Q13.

What is the time complexity of finding a pair with a given sum in a sorted array using Two Pointers?

A. O(n²)

B. O(n log n)

C. O(n)

D. O(1)

**Answer:** C

**Explanation:** Using two pointers (one at start, one at end) on a sorted array, we can find a pair with given sum in O(n) time with a single pass.

---

### Q14.

In the Two Pointers approach for container with most water, when do we move the left pointer?

A. Always

B. When left height is less than right height

C. When left height is greater than right height

D. Randomly

**Answer:** B

**Explanation:** We move the pointer with the smaller height because moving the larger height cannot increase the area (width decreases and height is limited by the smaller side).

---

### Q15.

What is the space complexity of the Two Pointers technique?

A. O(n)

B. O(log n)

C. O(n²)

D. O(1)

**Answer:** D

**Explanation:** Two Pointers technique typically uses only constant extra space O(1) as it only requires a few pointer variables.

---

### Q16.

Which problem can be efficiently solved using the Two Pointers technique?

A. Finding the shortest path in a graph

B. Reversing a string in-place

C. Building a binary tree

D. Implementing a hash table

**Answer:** B

**Explanation:** Reversing a string/array in-place is a classic Two Pointers problem where pointers start at both ends and swap elements moving toward the center.

---

### Q17.

What is the key idea behind partitioning in Quick Sort?

A. Divide array into equal halves

B. Place pivot in correct position with smaller elements left, larger right

C. Merge two sorted arrays

D. Build a heap structure

**Answer:** B

**Explanation:** Partitioning places the pivot element in its final sorted position, with all smaller elements to the left and larger elements to the right.

---

### Q18.

In a sorted rotated array [4,5,6,7,0,1,2], which approach helps find an element efficiently?

A. Linear search only

B. Modified binary search

C. Two Pointers from both ends

D. Hash table lookup

**Answer:** B

**Explanation:** Modified binary search can find elements in O(log n) time by determining which half is sorted and deciding which side to search.

---

### Q19.

What is the optimal approach to remove duplicates from a sorted array in-place?

A. Using a hash set

B. Using two nested loops

C. Using Two Pointers technique

D. Creating a new array

**Answer:** C

**Explanation:** Two Pointers (slow and fast) can remove duplicates in-place in O(n) time: slow pointer tracks unique elements, fast pointer scans the array.

---

### Q20.

For the problem "Move all zeros to end while maintaining order", what technique is most efficient?

A. Bubble Sort

B. Two Pointers technique

C. Quick Sort

D. Merge Sort

**Answer:** B

**Explanation:** Two Pointers approach (one for non-zero position, one for scanning) solves this in O(n) time with O(1) space while maintaining order.

---

### Q21.

What is the lower bound for comparison-based sorting algorithms?

A. O(n)

B. O(n log n)

C. O(n²)

D. O(log n)

**Answer:** B

**Explanation:** The theoretical lower bound for comparison-based sorting is O(n log n) in the worst case, proven by decision tree analysis.

---

### Q22.

Which sorting algorithm uses the divide-and-conquer approach?

A. Bubble Sort

B. Insertion Sort

C. Merge Sort

D. Selection Sort

**Answer:** C

**Explanation:** Merge Sort divides the array into halves (divide), recursively sorts them (conquer), and merges the sorted halves (combine).

---

### Q23.

What is the time complexity of Counting Sort when the range of input is k?

A. O(n + k)

B. O(n log n)

C. O(n²)

D. O(k log k)

**Answer:** A

**Explanation:** Counting Sort has O(n + k) time complexity, where n is the number of elements and k is the range of input values.

---

### Q24.

In the median of medians algorithm for finding the kth smallest element, what is the worst-case time complexity?

A. O(n²)

B. O(n log n)

C. O(n)

D. O(k log k)

**Answer:** C

**Explanation:** Median of medians guarantees O(n) worst-case time complexity for finding the kth smallest element, unlike quickselect's O(n²) worst case.

---

### Q25.

What is an in-place sorting algorithm?

A. One that uses recursion

B. One that requires O(1) or O(log n) extra space

C. One that runs in linear time

D. One that is stable

**Answer:** B

**Explanation:** An in-place algorithm uses only a constant amount O(1) or logarithmic O(log n) extra space beyond the input array.

---

### Q26.

For finding three numbers in an array that sum to a target, what is the optimal approach?

A. Three nested loops - O(n³)

B. Sort + Two Pointers for each element - O(n²)

C. Hash table with three passes - O(n³)

D. Binary search for each pair - O(n² log n)

**Answer:** B

**Explanation:** Sorting the array O(n log n) then using Two Pointers O(n) for each element gives overall O(n²) time complexity.

---

### Q27.

What happens in the "combine" step of Merge Sort?

A. The array is divided into halves

B. Two sorted subarrays are merged into one sorted array

C. A pivot element is selected

D. Elements are swapped randomly

**Answer:** B

**Explanation:** The combine/merge step takes two sorted subarrays and merges them into a single sorted array in O(n) time.

---

### Q28.

Which statement is TRUE about Quick Sort?

A. It always uses O(n) extra space

B. It is a stable sorting algorithm

C. Its worst case is O(n²) but average case is O(n log n)

D. It cannot be implemented recursively

**Answer:** C

**Explanation:** Quick Sort has O(n²) worst-case time (poor pivot choices) but O(n log n) average-case time, making it very efficient in practice.

---

### Q29.

What is the sliding window technique?

A. A variant of Two Pointers where the window size changes dynamically

B. A way to sort arrays

C. A graph traversal method

D. A tree balancing technique

**Answer:** A

**Explanation:** Sliding window is a Two Pointers variant where two pointers define a window that slides/expands/contracts through the array to solve subarray problems efficiently.

---

### Q30.

For the problem "find minimum in rotated sorted array", what is the optimal time complexity?

A. O(n)

B. O(n log n)

C. O(log n)

D. O(1)

**Answer:** C

**Explanation:** Modified binary search can find the minimum element in a rotated sorted array in O(log n) time by comparing middle element with the boundaries.

---

**End of MCQ Questions**
