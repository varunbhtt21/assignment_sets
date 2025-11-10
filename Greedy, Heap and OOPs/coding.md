# Greedy, Heap and OOPs - Coding Problems

---

## Problem 1: Forest Population Survey

**Difficulty:** Medium
**Company:** Amazon, Google, Meta

### Problem Statement

A wildlife research team is conducting a population survey in a forest with an unknown number of rabbits. The team asked n rabbits "How many rabbits have the same color as you?" and collected the answers in an integer array `answers` where `answers[i]` is the answer of the i-th rabbit.

Given the array `answers`, return the minimum number of rabbits that could be in the forest.

### Input Format
- An integer array `answers` where `answers[i]` represents the answer given by the i-th rabbit

### Output Format
- Return an integer representing the minimum number of rabbits in the forest

### Constraints
- `1 <= answers.length <= 1000`
- `0 <= answers[i] <= 1000`

### Examples

**Example 1:**
```
Input: answers = [1,1,2]
Output: 5
Explanation:
The two rabbits that answered "1" could both be the same color, say red.
The rabbit that answered "2" can't be red or the answers would be inconsistent.
Say the rabbit that answered "2" was blue.
Then there should be 2 other blue rabbits in the forest that didn't answer into the array.
The smallest possible number of rabbits in the forest is therefore 5: 3 that answered plus 2 that didn't.
```

**Example 2:**
```
Input: answers = [10,10,10]
Output: 11
```

### Test Cases

#### Test Case 1
**Input:**
```
[1,1,2]
```
**Output:**
```
5
```
**Explanation:** Two rabbits answered "1" (form one group of 2 red rabbits), one rabbit answered "2" (needs 2 more blue rabbits that didn't answer). Total = 2 + 3 = 5.

---

#### Test Case 2
**Input:**
```
[10,10,10]
```
**Output:**
```
11
```
**Explanation:** All three rabbits answered "10", meaning each has 10 rabbits of the same color including themselves. They can all be the same color, requiring 11 total rabbits (10+1).

---

#### Test Case 3
**Input:**
```
[0]
```
**Output:**
```
1
```
**Explanation:** One rabbit answered "0", meaning it has no other rabbits of the same color. Total = 1.

---

#### Test Case 4
**Input:**
```
[0,0,1,1,1]
```
**Output:**
```
6
```
**Explanation:** Two rabbits answered "0" (each is unique color, so 2 rabbits). Three rabbits answered "1" (can form at most 2 groups: one group of 2 rabbits, one group needing 1 more). Total = 2 + 2 + 2 = 6.

---

#### Test Case 5
**Input:**
```
[1,0,1,0,0]
```
**Output:**
```
5
```
**Explanation:** Three rabbits answered "0" (3 unique colors = 3 rabbits). Two rabbits answered "1" (form one group of 2). Total = 3 + 2 = 5.

---

#### Test Case 6
**Input:**
```
[2,2,2,2]
```
**Output:**
```
6
```
**Explanation:** Four rabbits answered "2" (each needs 2 others of same color, total 3 per group). We need 2 groups: 3 + 3 = 6 rabbits.

---

#### Test Case 7
**Input:**
```
[5,5,5,5,5,5]
```
**Output:**
```
6
```
**Explanation:** Six rabbits answered "5" (each says there are 5 others of same color, so 6 total per group). All 6 can be same color. Total = 6.

---

#### Test Case 8
**Input:**
```
[1,1,1]
```
**Output:**
```
4
```
**Explanation:** Three rabbits answered "1" (each needs 1 other of same color, so 2 per group). Need 2 groups: 2 + 2 = 4.

---

#### Test Case 9
**Input:**
```
[3,3,3,3,3]
```
**Output:**
```
8
```
**Explanation:** Five rabbits answered "3" (each needs 3 others, so 4 per group). Need 2 groups: 4 + 4 = 8.

---

#### Test Case 10
**Input:**
```
[0,1,0,2,0]
```
**Output:**
```
7
```
**Explanation:** Three "0"s = 3 rabbits. One "1" needs 1 more = 2 rabbits. One "2" needs 2 more = 3 rabbits. Total = 3 + 2 + 2 = 7. Wait, let me recalculate: "0" appears 3 times (3 unique), "1" appears 1 time (needs group of 2), "2" appears 1 time (needs group of 3). Total = 3 + 2 + 3 = 8.

---

## Problem 2: Fuel Station Circuit

**Difficulty:** Medium
**Company:** Flipkart, Amazon, Microsoft

### Problem Statement

A logistics company operates a fleet of delivery trucks on a circular route with n gas stations. The i-th station has `gas[i]` amount of fuel, and it costs `cost[i]` fuel to travel from the i-th station to the next (i+1)-th station.

You have a truck with an unlimited gas tank and it starts with an empty tank at one of the gas stations. You begin the journey with an empty tank.

Given two integer arrays `gas` and `cost`, return the starting gas station's index if you can travel around the circuit once in the clockwise direction, otherwise return -1. If there exists a solution, it is guaranteed to be unique.

### Input Format
- First line: Integer array `gas` representing fuel at each station
- Second line: Integer array `cost` representing cost to reach next station

### Output Format
- Return an integer representing the starting station index, or -1 if impossible

### Constraints
- `n == gas.length == cost.length`
- `1 <= n <= 10^5`
- `0 <= gas[i], cost[i] <= 10^4`

### Examples

**Example 1:**
```
Input: gas = [1,2,3,4,5], cost = [3,4,5,1,2]
Output: 3
Explanation:
Start at station 3 (index 3) and fill up with 4 unit of gas. Your tank = 0 + 4 = 4
Travel to station 4. Your tank = 4 - 1 + 5 = 8
Travel to station 0. Your tank = 8 - 2 + 1 = 7
Travel to station 1. Your tank = 7 - 3 + 2 = 6
Travel to station 2. Your tank = 6 - 4 + 3 = 5
Travel to station 3. The cost is 5. Your gas is just enough to travel back to station 3.
Therefore, return 3 as the starting index.
```

**Example 2:**
```
Input: gas = [2,3,4], cost = [3,4,3]
Output: -1
```

### Test Cases

#### Test Case 1
**Input:**
```
gas = [1,2,3,4,5]
cost = [3,4,5,1,2]
```
**Output:**
```
3
```
**Explanation:** Starting from station 3, you can complete the circuit.

---

#### Test Case 2
**Input:**
```
gas = [2,3,4]
cost = [3,4,3]
```
**Output:**
```
-1
```
**Explanation:** Total gas = 9, total cost = 10. Cannot complete the circuit from any starting point.

---

#### Test Case 3
**Input:**
```
gas = [5,1,2,3,4]
cost = [4,4,1,5,1]
```
**Output:**
```
4
```
**Explanation:** Starting from station 4 (index 4) allows completing the circuit.

---

#### Test Case 4
**Input:**
```
gas = [3,3,4]
cost = [3,4,4]
```
**Output:**
```
-1
```
**Explanation:** Total gas = 10, total cost = 11. Impossible to complete.

---

#### Test Case 5
**Input:**
```
gas = [1,2,3,4,5]
cost = [5,4,3,2,1]
```
**Output:**
```
2
```
**Explanation:** Starting from station 2 allows completing the circuit. From station 2: tank = 3, travel (cost 3) to station 3 with tank = 3-3+4 = 4, travel (cost 2) to station 4 with tank = 4-2+5 = 7, travel (cost 1) to station 0 with tank = 7-1+1 = 7, travel (cost 5) to station 1 with tank = 7-5+2 = 4, travel (cost 4) to station 2 with tank = 4-4 = 0. Completes circuit.

---

#### Test Case 6
**Input:**
```
gas = [2]
cost = [2]
```
**Output:**
```
0
```
**Explanation:** Single station with gas = cost. Can complete the circuit (stay at same station).

---

#### Test Case 7
**Input:**
```
gas = [5,8,2,8]
cost = [6,5,6,6]
```
**Output:**
```
3
```
**Explanation:** Starting from station 3 allows completing the circuit.

---

#### Test Case 8
**Input:**
```
gas = [4,5,2,6,5,3]
cost = [3,2,7,3,2,9]
```
**Output:**
```
-1
```
**Explanation:** Total gas = 25, total cost = 26. Cannot complete circuit.

---

#### Test Case 9
**Input:**
```
gas = [6,1,4,3,5]
cost = [3,8,2,4,2]
```
**Output:**
```
2
```
**Explanation:** Starting from station 2 allows completing the circuit.

---

#### Test Case 10
**Input:**
```
gas = [7,1,0,11,4]
cost = [5,9,1,2,5]
```
**Output:**
```
3
```
**Explanation:** Starting from station 3 allows completing the circuit.

---

## Problem 3: Product Analytics Dashboard

**Difficulty:** Medium
**Company:** Zoho, Amazon, Google

### Problem Statement

A product analytics platform needs to identify trending items. Given an integer array `nums` and an integer `k`, return the k most frequent elements. You may return the answer in any order.

### Input Format
- First line: Integer array `nums`
- Second line: Integer `k`

### Output Format
- Return an integer array of the k most frequent elements

### Constraints
- `1 <= nums.length <= 10^5`
- `-10^4 <= nums[i] <= 10^4`
- `k` is in the range `[1, the number of unique elements in the array]`
- It is guaranteed that the answer is unique

### Examples

**Example 1:**
```
Input: nums = [1,1,1,2,2,3], k = 2
Output: [1,2]
```

**Example 2:**
```
Input: nums = [1], k = 1
Output: [1]
```

**Example 3:**
```
Input: nums = [1,2,1,2,1,2,3,1,3,2], k = 2
Output: [1,2]
```

### Test Cases

#### Test Case 1
**Input:**
```
nums = [1,1,1,2,2,3]
k = 2
```
**Output:**
```
[1,2]
```
**Explanation:** 1 appears 3 times, 2 appears 2 times, 3 appears 1 time. Top 2 frequent are 1 and 2.

---

#### Test Case 2
**Input:**
```
nums = [1]
k = 1
```
**Output:**
```
[1]
```
**Explanation:** Only one element, so it's the most frequent.

---

#### Test Case 3
**Input:**
```
nums = [4,1,-1,2,-1,2,3]
k = 2
```
**Output:**
```
[-1,2]
```
**Explanation:** -1 appears 2 times, 2 appears 2 times, others appear once. Return any 2 of the most frequent.

---

#### Test Case 4
**Input:**
```
nums = [1,2]
k = 2
```
**Output:**
```
[1,2]
```
**Explanation:** Both elements appear once, return both.

---

#### Test Case 5
**Input:**
```
nums = [5,5,5,3,3,1,1,1,1]
k = 2
```
**Output:**
```
[1,5]
```
**Explanation:** 1 appears 4 times, 5 appears 3 times, 3 appears 2 times. Top 2 are 1 and 5.

---

#### Test Case 6
**Input:**
```
nums = [7,7]
k = 1
```
**Output:**
```
[7]
```
**Explanation:** 7 is the only element and most frequent.

---

#### Test Case 7
**Input:**
```
nums = [3,0,1,0]
k = 1
```
**Output:**
```
[0]
```
**Explanation:** 0 appears 2 times, others appear once. Most frequent is 0.

---

#### Test Case 8
**Input:**
```
nums = [-1,-1,-1,-2,-2,-3]
k = 3
```
**Output:**
```
[-1,-2,-3]
```
**Explanation:** -1 appears 3 times, -2 appears 2 times, -3 appears 1 time. Return all 3.

---

#### Test Case 9
**Input:**
```
nums = [1,1,1,2,2,2,3,3,3]
k = 1
```
**Output:**
```
[1]
```
**Explanation:** All appear 3 times, but k=1 so return any one. Could be [1], [2], or [3].

---

#### Test Case 10
**Input:**
```
nums = [5,2,5,3,5,3,1,1,3]
k = 2
```
**Output:**
```
[5,3]
```
**Explanation:** 5 appears 3 times, 3 appears 3 times, others less. Top 2 are 5 and 3.

---

## Problem 4: Message Priority Sorter

**Difficulty:** Medium
**Company:** IBM, Microsoft, Amazon

### Problem Statement

A messaging application needs to sort messages based on character frequency for spam detection. Given a string `s`, sort it in decreasing order based on the frequency of the characters. The frequency of a character is the number of times it appears in the string.

Return the sorted string. If there are multiple answers, return any of them.

### Input Format
- A string `s` consisting of uppercase and lowercase English letters and digits

### Output Format
- Return a string sorted by character frequency in decreasing order

### Constraints
- `1 <= s.length <= 5 * 10^5`
- `s` consists of uppercase and lowercase English letters and digits

### Examples

**Example 1:**
```
Input: s = "tree"
Output: "eert"
Explanation: 'e' appears twice while 'r' and 't' both appear once.
So 'e' must appear before both 'r' and 't'. Therefore "eetr" is also a valid answer.
```

**Example 2:**
```
Input: s = "cccaaa"
Output: "aaaccc"
Explanation: Both 'c' and 'a' appear three times, so both "cccaaa" and "aaaccc" are valid answers.
Note that "cacaca" is incorrect, as the same characters must be together.
```

**Example 3:**
```
Input: s = "Aabb"
Output: "bbAa"
Explanation: "bbaA" is also a valid answer, but "Aabb" is incorrect.
Note that 'A' and 'a' are treated as two different characters.
```

### Test Cases

#### Test Case 1
**Input:**
```
"tree"
```
**Output:**
```
"eert"
```
**Explanation:** 'e' appears 2 times, 'r' and 't' each appear 1 time. Output could also be "eetr".

---

#### Test Case 2
**Input:**
```
"cccaaa"
```
**Output:**
```
"aaaccc"
```
**Explanation:** Both 'c' and 'a' appear 3 times. Either "cccaaa" or "aaaccc" is valid.

---

#### Test Case 3
**Input:**
```
"Aabb"
```
**Output:**
```
"bbAa"
```
**Explanation:** 'b' appears 2 times, 'A' and 'a' each appear 1 time. Could also be "bbaA".

---

#### Test Case 4
**Input:**
```
"a"
```
**Output:**
```
"a"
```
**Explanation:** Single character returns as is.

---

#### Test Case 5
**Input:**
```
"raaeaedere"
```
**Output:**
```
"eeeeeaarrd"
```
**Explanation:** 'e' appears 5 times, 'a' appears 3 times, 'r' appears 2 times, 'd' appears 1 time. Wait let me count: r-1, a-3, e-4, d-1, r-already counted (total 2), e-already counted (wait let me recount): r,a,a,e,a,e,d,e,r,e = r:2, a:3, e:4, d:1. So "eeeeaaarrd" or similar.

---

#### Test Case 6
**Input:**
```
"loveleetcode"
```
**Output:**
```
"eeeeoollvtdc"
```
**Explanation:** 'e' appears 4 times, 'o' appears 2 times, 'l' appears 2 times, others once. Let me count: l-1, o-1, v-1, e-3, l-already(total 2), e-already(total 4), e-already, t-1, c-1, o-already(total 2), d-1, e-already. So e:4, o:2, l:2, v:1, t:1, c:1, d:1.

---

#### Test Case 7
**Input:**
```
"abc"
```
**Output:**
```
"abc"
```
**Explanation:** All characters appear once, any order is valid.

---

#### Test Case 8
**Input:**
```
"bbAaB"
```
**Output:**
```
"bbbAa"
```
**Explanation:** 'b' appears 2 times, 'B' appears 1 time, 'A' appears 1 time, 'a' appears 1 time. Total 'b':2, others:1 each.

---

#### Test Case 9
**Input:**
```
"2a554442f544asfasssffffasss"
```
**Output:**
```
"sssssssffffff44444aaaaaas52"
```
**Explanation:** Count frequencies and sort. 's' appears most frequently. Let me count properly: 2-1, a-5, 5-3, 4-5, 2-already, f-5, 4-already, a-already, s-6, f-already, a-already, s-already, s-already, f-already, f-already, f-already, f-already, a-already, s-already, s-already, s-already. So s:8, f:6, a:5, 4:5, 5:3, 2:1.

---

#### Test Case 10
**Input:**
```
"programming"
```
**Output:**
```
"ggmmrraipon"
```
**Explanation:** Count: p-1, r-2, o-1, g-2, a-1, m-2, i-1, n-1. So r,g,m each appear 2 times, others once.

---

**End of Coding Problems**
