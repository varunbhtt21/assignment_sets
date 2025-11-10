
## Problem 1: Valid Perfect Square

**Difficulty:** Easy
**Company:** Amazon, Microsoft, Google

### Problem Statement

A warehouse management system needs to verify if the total number of products can be perfectly arranged in a square grid layout for optimal storage. Given a positive integer `num` representing the total number of products, your task is to determine if they can be arranged in a perfect square formation.

Return `true` if `num` is a perfect square or `false` otherwise.

A **perfect square** is an integer that is the square of an integer. In other words, it is the product of some integer with itself.

**Important:** You must not use any built-in library function, such as `sqrt`.

### Input Format
- A single integer `num`

### Output Format
- Return `true` if `num` is a perfect square, otherwise return `false`

### Constraints
- `1 <= num <= 2^31 - 1`

### Examples

**Example 1:**
```
Input: 16
Output: true
Explanation: We return true because 4 × 4 = 16 and 4 is an integer.
```

**Example 2:**
```
Input: 14
Output: false
Explanation: We return false because 3.742 × 3.742 = 14 and 3.742 is not an integer.
```

### Test Cases

#### Test Case 1
**Input:**
```
1
```
**Output:**
```
true
```
**Explanation:** 1 is a perfect square (1 × 1 = 1).

---

#### Test Case 2
**Input:**
```
4
```
**Output:**
```
true
```
**Explanation:** 4 is a perfect square (2 × 2 = 4).

---

#### Test Case 3
**Input:**
```
16
```
**Output:**
```
true
```
**Explanation:** 16 is a perfect square (4 × 4 = 16).

---

#### Test Case 4
**Input:**
```
14
```
**Output:**
```
false
```
**Explanation:** 14 is not a perfect square as there's no integer whose square equals 14.

---

#### Test Case 5
**Input:**
```
25
```
**Output:**
```
true
```
**Explanation:** 25 is a perfect square (5 × 5 = 25).

---

#### Test Case 6
**Input:**
```
100
```
**Output:**
```
true
```
**Explanation:** 100 is a perfect square (10 × 10 = 100).

---

#### Test Case 7
**Input:**
```
808201
```
**Output:**
```
true
```
**Explanation:** 808201 is a perfect square (899 × 899 = 808201).

---

#### Test Case 8
**Input:**
```
2
```
**Output:**
```
false
```
**Explanation:** 2 is not a perfect square as there's no integer whose square equals 2.

---

#### Test Case 9
**Input:**
```
2147483647
```
**Output:**
```
false
```
**Explanation:** 2147483647 (2^31 - 1) is not a perfect square.

---

#### Test Case 10
**Input:**
```
2147395600
```
**Output:**
```
true
```
**Explanation:** 2147395600 is a perfect square (46340 × 46340 = 2147395600).

---

## Problem 2: Find the Duplicate Number

**Difficulty:** Medium
**Company:** Amazon, Microsoft, Apple, Bloomberg

### Problem Statement

A cloud infrastructure company is tracking server IDs for maintenance scheduling. Due to a logging error, exactly one server ID appears twice in the system while all other IDs appear exactly once. The system generates an array of integers `nums` containing `n + 1` integers where each integer is in the range `[1, n]` inclusive.

There is only **one repeated number** in `nums`, return this repeated number.

You must solve the problem **without** modifying the array `nums` and using only constant extra space.

### Input Format
- An array of integers `nums` of size `n + 1` where each element is in range `[1, n]`

### Output Format
- Return the duplicate number (integer)

### Constraints
- `1 <= n <= 10^5`
- `nums.length == n + 1`
- `1 <= nums[i] <= n`
- All the integers in `nums` appear only **once** except for **precisely one integer** which appears **two or more** times.

### Examples

**Example 1:**
```
Input: [1,3,4,2,2]
Output: 2
```

**Example 2:**
```
Input: [3,1,3,4,2]
Output: 3
```

**Example 3:**
```
Input: [3,3,3,3,3]
Output: 3
```

### Test Cases

#### Test Case 1
**Input:**
```
[1,3,4,2,2]
```
**Output:**
```
2
```
**Explanation:** The number 2 appears twice in the array.

---

#### Test Case 2
**Input:**
```
[3,1,3,4,2]
```
**Output:**
```
3
```
**Explanation:** The number 3 appears twice in the array.

---

#### Test Case 3
**Input:**
```
[3,3,3,3,3]
```
**Output:**
```
3
```
**Explanation:** The number 3 appears five times in the array.

---

#### Test Case 4
**Input:**
```
[1,1]
```
**Output:**
```
1
```
**Explanation:** In an array of size 2 with range [1,1], the number 1 must be duplicated.

---

#### Test Case 5
**Input:**
```
[2,5,9,6,9,3,8,9,7,1,4]
```
**Output:**
```
9
```
**Explanation:** The number 9 appears three times in the array.

---

#### Test Case 6
**Input:**
```
[1,2,3,4,5,6,7,8,9,9]
```
**Output:**
```
9
```
**Explanation:** The number 9 appears twice at the end of the array.

---

#### Test Case 7
**Input:**
```
[2,2,2,2,2]
```
**Output:**
```
2
```
**Explanation:** The number 2 appears five times in the array.

---

#### Test Case 8
**Input:**
```
[1,3,4,2,1]
```
**Output:**
```
1
```
**Explanation:** The number 1 appears twice in the array.

---

#### Test Case 9
**Input:**
```
[4,3,1,4,2]
```
**Output:**
```
4
```
**Explanation:** The number 4 appears twice in the array.

---

#### Test Case 10
**Input:**
```
[8,7,1,10,17,15,18,11,16,9,19,12,5,14,3,4,2,13,18,6]
```
**Output:**
```
18
```
**Explanation:** In this larger array with n=19, the number 18 appears twice.

---

## Problem 3: Find K Closest Elements

**Difficulty:** Medium
**Company:** Google, Facebook, Amazon, LinkedIn

### Problem Statement

A search engine needs to find the most relevant results based on a relevance score. Given a **sorted** integer array `arr`, two integers `k` and `x`, you need to return the `k` closest integers to `x` in the array. The result should also be sorted in ascending order.

An integer `a` is closer to `x` than an integer `b` if:
- `|a - x| < |b - x|`, or
- `|a - x| == |b - x|` and `a < b`

### Input Format
- First line: A sorted array `arr` of integers
- Second line: Integer `k` (number of closest elements to find)
- Third line: Integer `x` (target value)

### Output Format
- Return an array of `k` closest integers to `x`, sorted in ascending order

### Constraints
- `1 <= k <= arr.length`
- `1 <= arr.length <= 10^4`
- `arr` is sorted in **ascending** order
- `-10^4 <= arr[i], x <= 10^4`

### Examples

**Example 1:**
```
Input:
arr = [1,2,3,4,5]
k = 4
x = 3
Output: [1,2,3,4]
```

**Example 2:**
```
Input:
arr = [1,1,2,3,4,5]
k = 4
x = -1
Output: [1,1,2,3]
```

### Test Cases

#### Test Case 1
**Input:**
```
arr = [1,2,3,4,5]
k = 4
x = 3
```
**Output:**
```
[1,2,3,4]
```
**Explanation:** The distances from x=3 are [2,1,0,1,2]. The 4 closest elements are [1,2,3,4].

---

#### Test Case 2
**Input:**
```
arr = [1,1,2,3,4,5]
k = 4
x = -1
```
**Output:**
```
[1,1,2,3]
```
**Explanation:** Since x=-1 is less than all elements, we take the first 4 elements.

---

#### Test Case 3
**Input:**
```
arr = [1,2,3,4,5]
k = 1
x = 3
```
**Output:**
```
[3]
```
**Explanation:** The closest element to x=3 is 3 itself.

---

#### Test Case 4
**Input:**
```
arr = [1,2,3,4,5]
k = 3
x = 4
```
**Output:**
```
[3,4,5]
```
**Explanation:** The distances from x=4 are [3,2,1,0,1]. The 3 closest elements are [3,4,5].

---

#### Test Case 5
**Input:**
```
arr = [1,2,3,4,5,6,7,8,9,10]
k = 5
x = 6
```
**Output:**
```
[4,5,6,7,8]
```
**Explanation:** The 5 closest elements to x=6 are [4,5,6,7,8] with distances [2,1,0,1,2].

---

#### Test Case 6
**Input:**
```
arr = [0,1,2,2,2,3,6,8,8,9]
k = 5
x = 5
```
**Output:**
```
[2,2,2,3,6]
```
**Explanation:** The 5 closest elements to x=5 are [2,2,2,3,6] with distances [3,3,3,2,1].

---

#### Test Case 7
**Input:**
```
arr = [1,3,5,7,9]
k = 2
x = 4
```
**Output:**
```
[3,5]
```
**Explanation:** The distances from x=4 are [3,1,1,3,5]. Elements 3 and 5 are closest, both at distance 1.

---

#### Test Case 8
**Input:**
```
arr = [1]
k = 1
x = 1
```
**Output:**
```
[1]
```
**Explanation:** Single element array, return the only element.

---

#### Test Case 9
**Input:**
```
arr = [1,2,3,4,5]
k = 5
x = 10
```
**Output:**
```
[1,2,3,4,5]
```
**Explanation:** Since x=10 is greater than all elements, we return all k=5 elements.

---

#### Test Case 10
**Input:**
```
arr = [-5,-3,-2,0,1,3,5,7,9,11]
k = 6
x = 2
```
**Output:**
```
[-3,-2,0,1,3,5]
```
**Explanation:** The 6 closest elements to x=2 are [-3,-2,0,1,3,5] with distances [5,4,2,1,1,3].

---

## Problem 4: Most Profit Assigning Work

**Difficulty:** Medium
**Company:** Amazon, Microsoft, Google

### Problem Statement

A logistics company's fulfillment center is optimizing task assignments to maximize profit. You have `n` jobs and `m` workers. You are given three arrays: `difficulty`, `profit`, and `worker` where:

- `difficulty[i]` and `profit[i]` are the difficulty and the profit of the `i-th` job, and
- `worker[j]` is the ability of the `j-th` worker (i.e., the `j-th` worker can only complete a job with difficulty at most `worker[j]`).

Every worker can be assigned **at most one job**, but one job can be **completed multiple times**.

- For example, if three workers attempt the same job that pays `$1`, then the total profit will be `$3`. If a worker cannot complete any job, their profit is `$0`.

Return the maximum profit we can achieve after assigning the workers to the jobs.

### Input Format
- First line: Array `difficulty` of size `n`
- Second line: Array `profit` of size `n`
- Third line: Array `worker` of size `m`

### Output Format
- Return a single integer representing the maximum total profit

### Constraints
- `n == difficulty.length`
- `n == profit.length`
- `m == worker.length`
- `1 <= n, m <= 10^4`
- `1 <= difficulty[i], profit[i], worker[i] <= 10^5`

### Examples

**Example 1:**
```
Input:
difficulty = [2,4,6,8,10]
profit = [10,20,30,40,50]
worker = [4,5,6,7]
Output: 100
Explanation: Workers are assigned jobs of difficulty [4,4,6,6] and they get a profit of [20,20,30,30] separately.
```

**Example 2:**
```
Input:
difficulty = [85,47,57]
profit = [24,66,99]
worker = [40,25,25]
Output: 0
Explanation: No worker can complete any job, so the total profit is 0.
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
**Explanation:** Workers with abilities [4,5,6,7] can do jobs with difficulties [4,4,6,6] earning profits [20,20,30,30] = 100.

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
**Explanation:** All jobs are too difficult for all workers, so total profit is 0.

---

#### Test Case 3
**Input:**
```
difficulty = [1,2,3]
profit = [5,10,15]
worker = [1,1,1]
```
**Output:**
```
15
```
**Explanation:** All three workers can only do job with difficulty 1, earning 5 each = 15.

---

#### Test Case 4
**Input:**
```
difficulty = [5,10,15]
profit = [20,30,40]
worker = [20,20,20]
```
**Output:**
```
120
```
**Explanation:** All three workers can do the hardest job with difficulty 15, earning 40 each = 120.

---

#### Test Case 5
**Input:**
```
difficulty = [1]
profit = [100]
worker = [10,5,3,1,8]
```
**Output:**
```
500
```
**Explanation:** All 5 workers can do the only job with difficulty 1, earning 100 each = 500.

---

#### Test Case 6
**Input:**
```
difficulty = [10,20,30]
profit = [100,200,300]
worker = [15]
```
**Output:**
```
100
```
**Explanation:** Worker with ability 15 can do job with difficulty 10, earning 100.

---

#### Test Case 7
**Input:**
```
difficulty = [3,7,9,12]
profit = [50,80,100,120]
worker = [8,9,10,11]
```
**Output:**
```
380
```
**Explanation:** Workers can do jobs with difficulties [7,9,9,9] earning [80,100,100,100] = 380.

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
**Explanation:** All workers can do all jobs with difficulty 1, but they choose the highest profit job (30 each) = 90.

---

#### Test Case 9
**Input:**
```
difficulty = [5,5,5]
profit = [1,2,3]
worker = [10]
```
**Output:**
```
3
```
**Explanation:** Single worker with ability 10 can do all jobs but chooses the highest profit = 3.

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
**Explanation:** Workers with abilities [92,10,85,84,82] can do best available jobs within their capability.
- Worker 92: can do all jobs, best is difficulty 47 with profit 81
- Worker 10: cannot do any job, profit 0
- Worker 85: can do jobs ≤85, best is difficulty 47 with profit 81
- Worker 84: can do jobs ≤84, best is difficulty 47 with profit 81
- Worker 82: can do jobs ≤82, best is difficulty 47 with profit 81
Total: 81+0+81+81+81 = 324

---

**End of Coding Problems**
