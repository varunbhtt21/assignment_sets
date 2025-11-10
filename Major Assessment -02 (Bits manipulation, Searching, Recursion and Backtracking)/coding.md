# Major Assessment -02 - Coding Problems
## (Bits Manipulation, Searching, Recursion and Backtracking)

---

## Problem 1: Optimal Shopping Strategy

**Difficulty:** Medium
**Company:** MathWorks, Amazon, Google

### Problem Statement

An e-commerce platform is designing an optimal pricing system for bulk purchases. In the online store, there are `n` items to sell. Each item has a price. However, there are some special offers, and a special offer consists of one or more different kinds of items with a sale price.

You are given an integer array `price` where `price[i]` is the price of the i-th item, and an integer array `needs` where `needs[i]` is the number of pieces of the i-th item you want to buy.

You are also given an array `special` where `special[i]` is of size `n + 1` where `special[i][j]` is the number of pieces of the j-th item in the i-th offer and `special[i][n]` (i.e., the last integer in the array) is the price of the i-th offer.

Return the lowest price you have to pay for exactly certain items as given, where you could make optimal use of the special offers. You are not allowed to buy more items than you want, even if that would lower the overall price. You could use any of the special offers as many times as you want.

### Input Format
- First line: Array `price` of length `n`
- Second line: Array `special` of special offers
- Third line: Array `needs` of length `n`

### Output Format
- Return an integer representing the minimum price to pay

### Constraints
- `n == price.length == needs.length`
- `1 <= n <= 6`
- `0 <= price[i], needs[i] <= 10`
- `1 <= special.length <= 100`
- `special[i].length == n + 1`
- `0 <= special[i][j] <= 50`

### Examples

**Example 1:**
```
Input: price = [2,5], special = [[3,0,5],[1,2,10]], needs = [3,2]
Output: 14
Explanation: There are two kinds of items, A and B. Their prices are $2 and $5 respectively.
In special offer 1, you can pay $5 for 3A and 0B
In special offer 2, you can pay $10 for 1A and 2B.
You need to buy 3A and 2B, so you may pay $10 for 1A and 2B (special offer #2), and $4 for 2A.
```

**Example 2:**
```
Input: price = [2,3,4], special = [[1,1,0,4],[2,2,1,9]], needs = [1,2,1]
Output: 11
Explanation: The price of A is $2, and $3 for B, $4 for C.
You may pay $4 for 1A and 1B, and $9 for 2A ,2B and 1C.
You need to buy 1A ,2B and 1C, so you may pay $4 for 1A and 1B (special offer #1), and $3 for 1B, $4 for 1C.
You cannot add more items, though only $9 for 2A ,2B and 1C.
```

### Test Cases

#### Test Case 1
**Input:**
```
price = [2,5]
special = [[3,0,5],[1,2,10]]
needs = [3,2]
```
**Output:**
```
14
```
**Explanation:** Pay $10 for 1A and 2B (special offer #2), and $4 for 2A. Total = 14.

---

#### Test Case 2
**Input:**
```
price = [2,3,4]
special = [[1,1,0,4],[2,2,1,9]]
needs = [1,2,1]
```
**Output:**
```
11
```
**Explanation:** Pay $4 for 1A and 1B (offer #1), $3 for 1B, $4 for 1C. Total = 11.

---

#### Test Case 3
**Input:**
```
price = [2,5]
special = [[3,0,5]]
needs = [3,2]
```
**Output:**
```
15
```
**Explanation:** Use special offer for 3A ($5), then buy 2B at regular price ($10). Total = 15.

---

#### Test Case 4
**Input:**
```
price = [2,3]
special = [[1,1,4]]
needs = [1,1]
```
**Output:**
```
4
```
**Explanation:** Special offer gives 1A + 1B for $4, which matches needs exactly.

---

#### Test Case 5
**Input:**
```
price = [3,4]
special = [[2,2,7]]
needs = [2,2]
```
**Output:**
```
7
```
**Explanation:** Special offer gives 2A + 2B for $7, which is better than regular price 3*2 + 4*2 = 14.

---

#### Test Case 6
**Input:**
```
price = [1,1,1]
special = [[1,1,1,1]]
needs = [3,3,3]
```
**Output:**
```
3
```
**Explanation:** Use special offer 3 times (each gives 1A+1B+1C for $1). Total = 3.

---

#### Test Case 7
**Input:**
```
price = [5,5]
special = [[2,0,9],[0,2,9]]
needs = [2,2]
```
**Output:**
```
18
```
**Explanation:** Use both special offers: 2A for $9 and 2B for $9. Total = 18.

---

#### Test Case 8
**Input:**
```
price = [2,2,2]
special = [[1,1,1,2]]
needs = [1,1,1]
```
**Output:**
```
2
```
**Explanation:** Special offer gives all items for $2, better than 3*2 = 6.

---

#### Test Case 9
**Input:**
```
price = [10]
special = [[1,5]]
needs = [2]
```
**Output:**
```
10
```
**Explanation:** Use special offer twice: 2 items for 2*$5 = $10, same as regular 2*$10 = $20. Special is better.

---

#### Test Case 10
**Input:**
```
price = [9,9]
special = [[1,1,1]]
needs = [2,2]
```
**Output:**
```
2
```
**Explanation:** Use special offer twice (each gives 1A+1B for $1). Total = 2.

---

## Problem 2: Number Line Navigator

**Difficulty:** Medium
**Company:** Meesho, Amazon, Microsoft

### Problem Statement

A delivery tracking system needs to calculate optimal movement distances. You are standing at position `0` on an infinite number line. There is a destination at position `target`.

You can make some number of moves `numMoves` so that:
- On each move, you can either go left or right.
- During the i-th move (starting from i = 1 to i = numMoves), you take i steps in the chosen direction.

Given the integer `target`, return the minimum number of moves required (i.e., the minimum `numMoves`) to reach the destination.

### Input Format
- An integer `target`

### Output Format
- Return an integer representing the minimum number of moves

### Constraints
- `-10^9 <= target <= 10^9`
- `target != 0`

### Examples

**Example 1:**
```
Input: target = 2
Output: 3
Explanation:
On the 1st move, we step from 0 to 1 (1 step).
On the 2nd move, we step from 1 to -1 (2 steps).
On the 3rd move, we step from -1 to 2 (3 steps).
```

**Example 2:**
```
Input: target = 3
Output: 2
Explanation:
On the 1st move, we step from 0 to 1 (1 step).
On the 2nd move, we step from 1 to 3 (2 steps).
```

### Test Cases

#### Test Case 1
**Input:**
```
2
```
**Output:**
```
3
```
**Explanation:** Move sequence: +1, -2, +3 reaches 2.

---

#### Test Case 2
**Input:**
```
3
```
**Output:**
```
2
```
**Explanation:** Move sequence: +1, +2 reaches 3.

---

#### Test Case 3
**Input:**
```
1
```
**Output:**
```
1
```
**Explanation:** Single move of +1 reaches 1.

---

#### Test Case 4
**Input:**
```
5
```
**Output:**
```
5
```
**Explanation:** Move sequence: -1, +2, +3, -4, +5 reaches 5.

---

#### Test Case 5
**Input:**
```
4
```
**Output:**
```
3
```
**Explanation:** Move sequence: +1, +2, -3 reaches 4. Or +1, -2, +3, +4 = 6 with diff 2, but 1+2+3=6, flip none to get 6, need diff of 2 so flip step 1: -1+2+3=4.

---

#### Test Case 6
**Input:**
```
10
```
**Output:**
```
4
```
**Explanation:** 1+2+3+4=10, all positive reaches 10.

---

#### Test Case 7
**Input:**
```
-10
```
**Output:**
```
4
```
**Explanation:** Symmetric to positive 10, takes 4 moves.

---

#### Test Case 8
**Input:**
```
6
```
**Output:**
```
3
```
**Explanation:** 1+2+3=6, all positive reaches 6.

---

#### Test Case 9
**Input:**
```
7
```
**Output:**
```
5
```
**Explanation:** 1+2+3+4=10, need to reduce by 3. Flip step 2: 1-2+3+4=6, still need more. Need 1+2+3+4+5=15, flip 4: 1+2+3-4+5=7.

---

#### Test Case 10
**Input:**
```
-3
```
**Output:**
```
2
```
**Explanation:** Symmetric to positive 3, move sequence: -1, -2 reaches -3.

---

## Problem 3: Valid Digit String Counter

**Difficulty:** Medium
**Company:** Microsoft, Google, Amazon

### Problem Statement

A data validation system needs to count valid digit patterns. A digit string is good if the digits (0-indexed) at even indices are even and the digits at odd indices are prime (2, 3, 5, or 7).

For example, "2582" is good because the digits (2 and 8) at even positions are even and the digits (5 and 2) at odd positions are prime. However, "3245" is not good because 3 is at an even index but is not even.

Given an integer `n`, return the total number of good digit strings of length `n`. Since the answer may be large, return it modulo `10^9 + 7`.

A digit string is a string consisting of digits 0 through 9 that may contain leading zeros.

### Input Format
- An integer `n` (length of digit string)

### Output Format
- Return an integer representing count of good digit strings modulo `10^9 + 7`

### Constraints
- `1 <= n <= 10^15`

### Examples

**Example 1:**
```
Input: n = 1
Output: 5
Explanation: The good numbers of length 1 are "0", "2", "4", "6", "8".
```

**Example 2:**
```
Input: n = 4
Output: 400
```

**Example 3:**
```
Input: n = 50
Output: 564908303
```

### Test Cases

#### Test Case 1
**Input:**
```
1
```
**Output:**
```
5
```
**Explanation:** Even digits at position 0: {0, 2, 4, 6, 8}. Count = 5.

---

#### Test Case 2
**Input:**
```
2
```
**Output:**
```
20
```
**Explanation:** Position 0 has 5 choices (even), position 1 has 4 choices (prime). Total = 5 * 4 = 20.

---

#### Test Case 3
**Input:**
```
3
```
**Output:**
```
100
```
**Explanation:** Positions 0,2 have 5 choices each (even), position 1 has 4 choices (prime). Total = 5 * 4 * 5 = 100.

---

#### Test Case 4
**Input:**
```
4
```
**Output:**
```
400
```
**Explanation:** Pattern: even-prime-even-prime. Total = 5 * 4 * 5 * 4 = 400.

---

#### Test Case 5
**Input:**
```
5
```
**Output:**
```
2000
```
**Explanation:** Pattern: even-prime-even-prime-even. Total = 5 * 4 * 5 * 4 * 5 = 2000.

---

#### Test Case 6
**Input:**
```
10
```
**Output:**
```
3200000
```
**Explanation:** 5 even positions (0,2,4,6,8), 5 prime positions (1,3,5,7,9). Total = 5^5 * 4^5 = 3,125 * 1,024 = 3,200,000.

---

#### Test Case 7
**Input:**
```
6
```
**Output:**
```
8000
```
**Explanation:** 3 even positions (0,2,4), 3 prime positions (1,3,5). Total = 5^3 * 4^3 = 125 * 64 = 8000.

---

#### Test Case 8
**Input:**
```
7
```
**Output:**
```
40000
```
**Explanation:** 4 even positions (0,2,4,6), 3 prime positions (1,3,5). Total = 5^4 * 4^3 = 625 * 64 = 40,000.

---

#### Test Case 9
**Input:**
```
8
```
**Output:**
```
160000
```
**Explanation:** 4 even positions, 4 prime positions. Total = 5^4 * 4^4 = 625 * 256 = 160,000.

---

#### Test Case 10
**Input:**
```
50
```
**Output:**
```
564908303
```
**Explanation:** 25 even positions, 25 prime positions. Total = 5^25 * 4^25 mod (10^9 + 7) = 564908303.

---

## Problem 4: Case Transformation Generator

**Difficulty:** Medium
**Company:** Google, Facebook, Amazon

### Problem Statement

A text processing system needs to generate all case variations. Given a string `s`, you can transform every letter individually to be lowercase or uppercase to create another string.

Return a list of all possible strings we could create. Return the output in any order.

### Input Format
- A string `s` consisting of lowercase/uppercase English letters and digits

### Output Format
- Return a list of all possible case transformations

### Constraints
- `1 <= s.length <= 12`
- `s` consists of lowercase English letters, uppercase English letters, and digits

### Examples

**Example 1:**
```
Input: s = "a1b2"
Output: ["a1b2","a1B2","A1b2","A1B2"]
```

**Example 2:**
```
Input: s = "3z4"
Output: ["3z4","3Z4"]
```

### Test Cases

#### Test Case 1
**Input:**
```
"a1b2"
```
**Output:**
```
["a1b2","a1B2","A1b2","A1B2"]
```
**Explanation:** 2 letters, each can be lower or upper. Total = 2^2 = 4 permutations.

---

#### Test Case 2
**Input:**
```
"3z4"
```
**Output:**
```
["3z4","3Z4"]
```
**Explanation:** Only 1 letter, so 2 permutations.

---

#### Test Case 3
**Input:**
```
"a"
```
**Output:**
```
["a","A"]
```
**Explanation:** Single letter has 2 cases.

---

#### Test Case 4
**Input:**
```
"12345"
```
**Output:**
```
["12345"]
```
**Explanation:** No letters, only one permutation.

---

#### Test Case 5
**Input:**
```
"ab"
```
**Output:**
```
["ab","aB","Ab","AB"]
```
**Explanation:** 2 letters, 2^2 = 4 permutations.

---

#### Test Case 6
**Input:**
```
"C"
```
**Output:**
```
["c","C"]
```
**Explanation:** Single uppercase letter can be lower or upper.

---

#### Test Case 7
**Input:**
```
"a1"
```
**Output:**
```
["a1","A1"]
```
**Explanation:** 1 letter, 2 permutations.

---

#### Test Case 8
**Input:**
```
"abc"
```
**Output:**
```
["abc","abC","aBc","aBC","Abc","AbC","ABc","ABC"]
```
**Explanation:** 3 letters, 2^3 = 8 permutations.

---

#### Test Case 9
**Input:**
```
"0"
```
**Output:**
```
["0"]
```
**Explanation:** Single digit, only one permutation.

---

#### Test Case 10
**Input:**
```
"mL"
```
**Output:**
```
["ml","mL","Ml","ML"]
```
**Explanation:** 2 letters (both already in string), 2^2 = 4 permutations.

---

**End of Coding Problems**
