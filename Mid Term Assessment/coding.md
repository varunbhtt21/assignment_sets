# Mid Term Assessment - Coding Problems

---

## Problem 1: Binary Distance Calculator

**Difficulty:** Easy
**Company:** eBay

### Problem Statement

A data analytics team is working on optimizing binary data transmission. Given a positive integer `n`, find and return the longest distance between any two adjacent 1's in the binary representation of `n`. If there are no two adjacent 1's, return 0.

Two 1's are adjacent if there are only 0's separating them (possibly no 0's). The distance between two 1's is the absolute difference between their bit positions. For example, the two 1's in "1001" have a distance of 3.

### Input Format
- A positive integer `n`

### Output Format
- Return an integer representing the longest distance between adjacent 1's, or 0 if no such pair exists

### Constraints
- `1 <= n <= 10^9`

### Examples

**Example 1:**
```
Input: n = 22
Output: 2
Explanation: 22 in binary is "10110".
The first adjacent pair of 1's is "10110" with a distance of 2.
The second adjacent pair of 1's is "10110" with a distance of 1.
The answer is the largest of these two distances, which is 2.
```

**Example 2:**
```
Input: n = 8
Output: 0
Explanation: 8 in binary is "1000".
There are not any adjacent pairs of 1's in the binary representation of 8, so we return 0.
```

**Example 3:**
```
Input: n = 5
Output: 2
Explanation: 5 in binary is "101".
```

### Test Cases

#### Test Case 1
**Input:**
```
22
```
**Output:**
```
2
```
**Explanation:** Binary: "10110". Adjacent pairs at positions (1,3) with distance 2, and (3,4) with distance 1. Maximum distance is 2.

---

#### Test Case 2
**Input:**
```
8
```
**Output:**
```
0
```
**Explanation:** Binary: "1000". Only one 1, so no adjacent pairs exist. Return 0.

---

#### Test Case 3
**Input:**
```
5
```
**Output:**
```
2
```
**Explanation:** Binary: "101". Adjacent pair at positions (0,2) with distance 2.

---

#### Test Case 4
**Input:**
```
6
```
**Output:**
```
1
```
**Explanation:** Binary: "110". Adjacent pair at positions (1,2) with distance 1.

---

#### Test Case 5
**Input:**
```
1
```
**Output:**
```
0
```
**Explanation:** Binary: "1". Only one 1, no adjacent pairs. Return 0.

---

#### Test Case 6
**Input:**
```
319
```
**Output:**
```
3
```
**Explanation:** Binary: "100111111". First 1 at position 0, next 1 at position 2. Distance = 3. Then consecutive 1's have distance 1. Maximum is 3.

---

#### Test Case 7
**Input:**
```
15
```
**Output:**
```
1
```
**Explanation:** Binary: "1111". All 1's are consecutive with distance 1 between each pair.

---

#### Test Case 8
**Input:**
```
32
```
**Output:**
```
0
```
**Explanation:** Binary: "100000". Only one 1, no adjacent pairs. Return 0.

---

#### Test Case 9
**Input:**
```
9
```
**Output:**
```
3
```
**Explanation:** Binary: "1001". Adjacent pair at positions (0,3) with distance 3.

---

#### Test Case 10
**Input:**
```
145
```
**Output:**
```
4
```
**Explanation:** Binary: "10010001". Adjacent pairs exist, maximum distance is 4.

---

## Problem 2: Array Equalizer

**Difficulty:** Medium
**Company:** Myntra

### Problem Statement

A software testing team needs to validate array transformation algorithms. Given an integer array `nums` of size `n`, return the minimum number of moves required to make all array elements equal.

In one move, you can increment or decrement an element of the array by 1.

Test cases are designed so that the answer will fit in a 32-bit integer.

### Input Format
- An integer array `nums` of size `n`

### Output Format
- Return an integer representing the minimum number of moves

### Constraints
- `n == nums.length`
- `1 <= nums.length <= 10^5`
- `-10^9 <= nums[i] <= 10^9`

### Examples

**Example 1:**
```
Input: nums = [1,2,3]
Output: 2
Explanation:
Only two moves are needed (remember each move increments or decrements one element):
[1,2,3]  =>  [2,2,3]  =>  [2,2,2]
```

**Example 2:**
```
Input: nums = [1,10,2,9]
Output: 16
```

### Test Cases

#### Test Case 1
**Input:**
```
[1,2,3]
```
**Output:**
```
2
```
**Explanation:** Move 1 to 2 (1 move) and 3 to 2 (1 move). Total = 2 moves. Target is median 2.

---

#### Test Case 2
**Input:**
```
[1,10,2,9]
```
**Output:**
```
16
```
**Explanation:** Sort: [1,2,9,10]. Median is between 2 and 9. Choose either. If target is 2: |1-2|+|2-2|+|9-2|+|10-2| = 1+0+7+8 = 16.

---

#### Test Case 3
**Input:**
```
[1,0,0,8,6]
```
**Output:**
```
14
```
**Explanation:** Sort: [0,0,1,6,8]. Median is 1. Moves: |0-1|+|0-1|+|1-1|+|6-1|+|8-1| = 1+1+0+5+7 = 14.

---

#### Test Case 4
**Input:**
```
[1]
```
**Output:**
```
0
```
**Explanation:** Single element, already equal. 0 moves needed.

---

#### Test Case 5
**Input:**
```
[1,2]
```
**Output:**
```
1
```
**Explanation:** Move one element to match the other. 1 move needed.

---

#### Test Case 6
**Input:**
```
[5,5,5,5]
```
**Output:**
```
0
```
**Explanation:** All elements already equal. 0 moves needed.

---

#### Test Case 7
**Input:**
```
[1,2,3,4,5]
```
**Output:**
```
6
```
**Explanation:** Median is 3. Moves: |1-3|+|2-3|+|3-3|+|4-3|+|5-3| = 2+1+0+1+2 = 6.

---

#### Test Case 8
**Input:**
```
[-1000000000,1000000000]
```
**Output:**
```
2000000000
```
**Explanation:** Large range. Move both to 0 (or any midpoint). Total moves = 2 billion.

---

#### Test Case 9
**Input:**
```
[1,1,1,10,10,10]
```
**Output:**
```
27
```
**Explanation:** Median is between 1 and 10. Optimal target varies, but minimum total is 27 moves.

---

#### Test Case 10
**Input:**
```
[10,9,8,7,6,5,4,3,2,1]
```
**Output:**
```
25
```
**Explanation:** Median is between 5 and 6 (choose 5 or 6). Minimum moves to make all equal is 25.

---

## Problem 3: Job Assignment Optimizer

**Difficulty:** Medium
**Company:** Microsoft

### Problem Statement

A project management system needs to optimize worker assignments. You have `n` jobs and `m` workers. You are given three arrays: `difficulty`, `profit`, and `worker` where:

- `difficulty[i]` and `profit[i]` are the difficulty and the profit of the i-th job
- `worker[j]` is the ability of the j-th worker (i.e., the j-th worker can only complete a job with difficulty at most `worker[j]`)

Every worker can be assigned at most one job, but one job can be completed multiple times.

For example, if three workers attempt the same job that pays $1, then the total profit will be $3. If a worker cannot complete any job, their profit is $0.

Return the maximum profit we can achieve after assigning the workers to the jobs.

### Input Format
- First line: Integer array `difficulty` representing job difficulties
- Second line: Integer array `profit` representing job profits
- Third line: Integer array `worker` representing worker abilities

### Output Format
- Return an integer representing the maximum total profit

### Constraints
- `n == difficulty.length`
- `n == profit.length`
- `m == worker.length`
- `1 <= n, m <= 10^4`
- `1 <= difficulty[i], profit[i], worker[i] <= 10^5`

### Examples

**Example 1:**
```
Input: difficulty = [2,4,6,8,10], profit = [10,20,30,40,50], worker = [4,5,6,7]
Output: 100
Explanation: Workers are assigned jobs of difficulty [4,4,6,6] and they get a profit of [20,20,30,30] separately.
```

**Example 2:**
```
Input: difficulty = [85,47,57], profit = [24,66,99], worker = [40,25,25]
Output: 0
```

### Test Cases

#### Test Case 1
**Input:**
```
difficulty = [2,4,6,8,10]
profit = [10,20,30,40,50]
worker = [4,5,6,7]
```
**Output:**
```
100
```
**Explanation:** Worker abilities [4,5,6,7] can do jobs with difficulty ≤ their ability. Best assignments: all workers get profits [20,20,30,30]. Total = 100.

---

#### Test Case 2
**Input:**
```
difficulty = [85,47,57]
profit = [24,66,99]
worker = [40,25,25]
```
**Output:**
```
0
```
**Explanation:** No worker has ability ≥ any job difficulty. All workers get profit 0. Total = 0.

---

#### Test Case 3
**Input:**
```
difficulty = [1]
profit = [100]
worker = [1,2,3]
```
**Output:**
```
300
```
**Explanation:** All 3 workers can complete the job. Each gets profit 100. Total = 300.

---

#### Test Case 4
**Input:**
```
difficulty = [1,2,3]
profit = [5,10,15]
worker = [1]
```
**Output:**
```
5
```
**Explanation:** Worker with ability 1 can only do job with difficulty 1, getting profit 5.

---

#### Test Case 5
**Input:**
```
difficulty = [5,10]
profit = [100,200]
worker = [6,7,8,9,10]
```
**Output:**
```
600
```
**Explanation:** Workers with abilities [6,7,8,9] can only do difficulty 5 job (profit 100 each). Worker with ability 10 can do difficulty 10 job (profit 200). Total = 4×100 + 200 = 600.

---

#### Test Case 6
**Input:**
```
difficulty = [1,2,3,4,5]
profit = [10,15,20,25,30]
worker = [3]
```
**Output:**
```
20
```
**Explanation:** Worker with ability 3 can do jobs with difficulty ≤ 3. Best job is difficulty 3 with profit 20.

---

#### Test Case 7
**Input:**
```
difficulty = [10,20,30]
profit = [50,100,150]
worker = [5,15,25,35]
```
**Output:**
```
300
```
**Explanation:** Workers with abilities [5,15,25,35] get profits [0,50,100,150]. Total = 0+50+100+150 = 300.

---

#### Test Case 8
**Input:**
```
difficulty = [1,1,1]
profit = [10,20,30]
worker = [1,1,1]
```
**Output:**
```
90
```
**Explanation:** For difficulty 1, best profit is 30. All 3 workers can do it. Total = 3 × 30 = 90.

---

#### Test Case 9
**Input:**
```
difficulty = [1,5,10]
profit = [100,50,75]
worker = [2,6,11]
```
**Output:**
```
275
```
**Explanation:** Worker abilities [2,6,11] get best jobs with profits [100,100,100]. Wait, let me recalculate: ability 2 can do difficulty 1 (profit 100), ability 6 can do difficulties 1 and 5 (best is 100), ability 11 can do all (best is 100). Total = 300.

---

#### Test Case 10
**Input:**
```
difficulty = [68,35,52,47,86]
profit = [67,17,1,81,3]
worker = [92,10,85,84,82]
```
**Output:**
```
324
```
**Explanation:** Workers choose best jobs they can do based on ability. Optimal assignment gives total profit 324.

---

## Problem 4: Power Set Generator

**Difficulty:** Meta
**Company:** Amazon, Microsoft, Google

### Problem Statement

A combinatorics research team needs to generate all possible subsets. Given an integer array `nums` of unique elements, return all possible subsets (the power set).

The solution set must not contain duplicate subsets. Return the solution in any order.

### Input Format
- An integer array `nums` of unique elements

### Output Format
- Return a list of lists representing all possible subsets

### Constraints
- `1 <= nums.length <= 10`
- `-10 <= nums[i] <= 10`
- All the numbers of `nums` are unique

### Examples

**Example 1:**
```
Input: nums = [1,2,3]
Output: [[],[1],[2],[1,2],[3],[1,3],[2,3],[1,2,3]]
```

**Example 2:**
```
Input: nums = [0]
Output: [[],[0]]
```

### Test Cases

#### Test Case 1
**Input:**
```
[1,2,3]
```
**Output:**
```
[[],[1],[2],[1,2],[3],[1,3],[2,3],[1,2,3]]
```
**Explanation:** Power set of [1,2,3] contains 2^3 = 8 subsets including empty set and the set itself.

---

#### Test Case 2
**Input:**
```
[0]
```
**Output:**
```
[[],[0]]
```
**Explanation:** Power set of single element has 2 subsets: empty set and the element itself.

---

#### Test Case 3
**Input:**
```
[1,2]
```
**Output:**
```
[[],[1],[2],[1,2]]
```
**Explanation:** Power set has 2^2 = 4 subsets.

---

#### Test Case 4
**Input:**
```
[5]
```
**Output:**
```
[[],[5]]
```
**Explanation:** Single element, 2 subsets total.

---

#### Test Case 5
**Input:**
```
[1,2,3,4]
```
**Output:**
```
[[],[1],[2],[1,2],[3],[1,3],[2,3],[1,2,3],[4],[1,4],[2,4],[1,2,4],[3,4],[1,3,4],[2,3,4],[1,2,3,4]]
```
**Explanation:** Power set of 4 elements has 2^4 = 16 subsets.

---

#### Test Case 6
**Input:**
```
[-1,0,1]
```
**Output:**
```
[[],[-1],[0],[-1,0],[1],[-1,1],[0,1],[-1,0,1]]
```
**Explanation:** Works with negative numbers. 2^3 = 8 subsets.

---

#### Test Case 7
**Input:**
```
[10]
```
**Output:**
```
[[],[10]]
```
**Explanation:** Single element case, 2 subsets.

---

#### Test Case 8
**Input:**
```
[1,2,3,4,5]
```
**Output:**
```
[[],[1],[2],[1,2],[3],[1,3],[2,3],[1,2,3],[4],[1,4],[2,4],[1,2,4],[3,4],[1,3,4],[2,3,4],[1,2,3,4],[5],[1,5],[2,5],[1,2,5],[3,5],[1,3,5],[2,3,5],[1,2,3,5],[4,5],[1,4,5],[2,4,5],[1,2,4,5],[3,4,5],[1,3,4,5],[2,3,4,5],[1,2,3,4,5]]
```
**Explanation:** Power set of 5 elements has 2^5 = 32 subsets.

---

#### Test Case 9
**Input:**
```
[7,8]
```
**Output:**
```
[[],[7],[8],[7,8]]
```
**Explanation:** Two elements, 2^2 = 4 subsets.

---

#### Test Case 10
**Input:**
```
[-5,-3,-1]
```
**Output:**
```
[[],[-5],[-3],[-5,-3],[-1],[-5,-1],[-3,-1],[-5,-3,-1]]
```
**Explanation:** All negative numbers, 2^3 = 8 subsets.

---

**End of Coding Problems**
