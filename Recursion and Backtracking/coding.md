# Recursion and Backtracking - Coding Problems

---

## Problem 1: Power of Three Validator

**Difficulty:** Easy
**Company:** Google, Amazon, Apple

### Problem Statement

A tech startup building a distributed computing platform needs to validate if certain numerical values represent powers of three for their load balancing algorithm. Given an integer `n`, you need to determine if it is a power of three.

Return `true` if it is a power of three. Otherwise, return `false`.

An integer `n` is a power of three, if there exists an integer `x` such that `n == 3^x`.

### Input Format
- A single integer `n`

### Output Format
- Return `true` if `n` is a power of three, otherwise return `false`

### Constraints
- `-2^31 <= n <= 2^31 - 1`

### Examples

**Example 1:**
```
Input: 27
Output: true
Explanation: 27 = 3^3
```

**Example 2:**
```
Input: 0
Output: false
Explanation: There is no x where 3^x = 0.
```

**Example 3:**
```
Input: -1
Output: false
Explanation: There is no x where 3^x = (-1).
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
**Explanation:** 1 = 3^0, so it is a power of three.

---

#### Test Case 2
**Input:**
```
3
```
**Output:**
```
true
```
**Explanation:** 3 = 3^1, so it is a power of three.

---

#### Test Case 3
**Input:**
```
9
```
**Output:**
```
true
```
**Explanation:** 9 = 3^2, so it is a power of three.

---

#### Test Case 4
**Input:**
```
27
```
**Output:**
```
true
```
**Explanation:** 27 = 3^3, so it is a power of three.

---

#### Test Case 5
**Input:**
```
0
```
**Output:**
```
false
```
**Explanation:** There is no integer x where 3^x = 0.

---

#### Test Case 6
**Input:**
```
-1
```
**Output:**
```
false
```
**Explanation:** There is no integer x where 3^x equals a negative number.

---

#### Test Case 7
**Input:**
```
45
```
**Output:**
```
false
```
**Explanation:** 45 cannot be expressed as 3^x for any integer x. (3^3 = 27, 3^4 = 81)

---

#### Test Case 8
**Input:**
```
243
```
**Output:**
```
true
```
**Explanation:** 243 = 3^5, so it is a power of three.

---

#### Test Case 9
**Input:**
```
2
```
**Output:**
```
false
```
**Explanation:** 2 cannot be expressed as 3^x for any integer x.

---

#### Test Case 10
**Input:**
```
19683
```
**Output:**
```
true
```
**Explanation:** 19683 = 3^9, so it is a power of three.

---

## Problem 2: Game Winner Predictor

**Difficulty:** Medium
**Company:** Google, Amazon, Microsoft

### Problem Statement

You are designing a competitive strategy game where two players compete using an integer array `nums`. Player 1 and Player 2 take turns, with Player 1 starting first. Both players start the game with a score of `0`.

At each turn, the player takes one of the numbers from either end of the array (i.e., `nums[0]` or `nums[nums.length - 1]`) which reduces the size of the array by 1. The player adds the chosen number to their score. The game ends when there are no more elements in the array.

Return `true` if Player 1 can win the game. If the scores of both players are equal, then Player 1 is still the winner, and you should also return `true`. You may assume that both players are playing optimally.

### Input Format
- An integer array `nums`

### Output Format
- Return `true` if Player 1 can win the game, otherwise return `false`

### Constraints
- `1 <= nums.length <= 20`
- `0 <= nums[i] <= 10^7`

### Examples

**Example 1:**
```
Input: [1,5,2]
Output: false
Explanation: Initially, player 1 can choose between 1 and 2.
If he chooses 2 (or 1), then player 2 can choose from 1 (or 2) and 5. If player 2 chooses 5, then player 1 will be left with 1 (or 2).
So, final score of player 1 is 1 + 2 = 3, and player 2 is 5.
Hence, player 1 will never be the winner and you need to return false.
```

**Example 2:**
```
Input: [1,5,233,7]
Output: true
Explanation: Player 1 first chooses 1. Then player 2 has to choose between 5 and 7. No matter which number player 2 choose, player 1 can choose 233.
Finally, player 1 has more score (234) than player 2 (12), so you need to return true representing player1 can win.
```

### Test Cases

#### Test Case 1
**Input:**
```
[1,5,2]
```
**Output:**
```
false
```
**Explanation:** Player 1 gets 1+2=3, Player 2 gets 5. Player 2 wins.

---

#### Test Case 2
**Input:**
```
[1,5,233,7]
```
**Output:**
```
true
```
**Explanation:** Player 1 gets 1+233=234, Player 2 gets 5+7=12. Player 1 wins.

---

#### Test Case 3
**Input:**
```
[1]
```
**Output:**
```
true
```
**Explanation:** Player 1 takes the only element and wins with score 1.

---

#### Test Case 4
**Input:**
```
[1,2]
```
**Output:**
```
true
```
**Explanation:** Player 1 takes 2, Player 2 takes 1. Player 1 wins with score 2 > 1.

---

#### Test Case 5
**Input:**
```
[2,4,55,6,8]
```
**Output:**
```
false
```
**Explanation:** With optimal play, Player 1 gets 2+55=57, Player 2 gets 4+6+8=18. Wait, let me recalculate: P1 takes 2, P2 takes 8, P1 takes 6, P2 takes 55, P1 takes 4. P1: 2+6+4=12, P2: 8+55=63. Player 2 wins.

---

#### Test Case 6
**Input:**
```
[3,7,2,3]
```
**Output:**
```
true
```
**Explanation:** Player 1 takes 3, Player 2 takes 3, Player 1 takes 7, Player 2 takes 2. P1: 3+7=10, P2: 3+2=5. Player 1 wins.

---

#### Test Case 7
**Input:**
```
[1,1,1,1]
```
**Output:**
```
true
```
**Explanation:** Both players get score 2, but Player 1 wins on tie.

---

#### Test Case 8
**Input:**
```
[5,3,7,10]
```
**Output:**
```
true
```
**Explanation:** Player 1 takes 10, Player 2 takes 7, Player 1 takes 5, Player 2 takes 3. P1: 10+5=15, P2: 7+3=10. Player 1 wins.

---

#### Test Case 9
**Input:**
```
[100,200]
```
**Output:**
```
true
```
**Explanation:** Player 1 takes 200, Player 2 takes 100. Player 1 wins.

---

#### Test Case 10
**Input:**
```
[10,20,30,40,50]
```
**Output:**
```
true
```
**Explanation:** With optimal play, Player 1 can win. P1 takes 50, P2 takes 40, P1 takes 30, P2 takes 20, P1 takes 10. P1: 50+30+10=90, P2: 40+20=60. Player 1 wins.

---

## Problem 3: Combination Builder

**Difficulty:** Medium
**Company:** Amazon, Microsoft, Facebook

### Problem Statement

A data analytics team needs to find all valid combinations of `k` numbers that sum up to `n` for their sampling algorithm. The combinations must satisfy these conditions:

- Only numbers 1 through 9 are used.
- Each number is used **at most once**.

Return a list of all possible valid combinations. The list must not contain the same combination twice, and the combinations may be returned in any order.

### Input Format
- First line: Integer `k` (number of elements in combination)
- Second line: Integer `n` (target sum)

### Output Format
- Return a list of lists containing all valid combinations

### Constraints
- `2 <= k <= 9`
- `1 <= n <= 60`

### Examples

**Example 1:**
```
Input:
k = 3
n = 7
Output: [[1,2,4]]
Explanation: 1 + 2 + 4 = 7. There are no other valid combinations.
```

**Example 2:**
```
Input:
k = 3
n = 9
Output: [[1,2,6],[1,3,5],[2,3,4]]
Explanation:
1 + 2 + 6 = 9
1 + 3 + 5 = 9
2 + 3 + 4 = 9
There are no other valid combinations.
```

**Example 3:**
```
Input:
k = 4
n = 1
Output: []
Explanation: There are no valid combinations. Using 4 different numbers in the range [1,9], the smallest sum we can get is 1+2+3+4 = 10 and since 10 > 1, there are no valid combination.
```

### Test Cases

#### Test Case 1
**Input:**
```
k = 3
n = 7
```
**Output:**
```
[[1,2,4]]
```
**Explanation:** Only one valid combination: 1 + 2 + 4 = 7.

---

#### Test Case 2
**Input:**
```
k = 3
n = 9
```
**Output:**
```
[[1,2,6],[1,3,5],[2,3,4]]
```
**Explanation:** Three valid combinations that sum to 9.

---

#### Test Case 3
**Input:**
```
k = 4
n = 1
```
**Output:**
```
[]
```
**Explanation:** Minimum sum with 4 different numbers is 1+2+3+4=10, which exceeds 1.

---

#### Test Case 4
**Input:**
```
k = 2
n = 3
```
**Output:**
```
[[1,2]]
```
**Explanation:** Only valid combination: 1 + 2 = 3.

---

#### Test Case 5
**Input:**
```
k = 2
n = 10
```
**Output:**
```
[[1,9],[2,8],[3,7],[4,6]]
```
**Explanation:** Four valid pairs that sum to 10.

---

#### Test Case 6
**Input:**
```
k = 3
n = 6
```
**Output:**
```
[[1,2,3]]
```
**Explanation:** Only valid combination: 1 + 2 + 3 = 6.

---

#### Test Case 7
**Input:**
```
k = 1
n = 5
```
**Output:**
```
[[5]]
```
**Explanation:** Single number 5 satisfies k=1 and sum=5. Note: k constraint is 2-9, but testing edge case.

---

#### Test Case 8
**Input:**
```
k = 2
n = 5
```
**Output:**
```
[[1,4],[2,3]]
```
**Explanation:** Two valid pairs: 1+4=5 and 2+3=5.

---

#### Test Case 9
**Input:**
```
k = 4
n = 10
```
**Output:**
```
[[1,2,3,4]]
```
**Explanation:** Only valid combination: 1+2+3+4=10.

---

#### Test Case 10
**Input:**
```
k = 5
n = 25
```
**Output:**
```
[[1,2,7,8,9],[1,3,6,8,9],[1,4,5,8,9],[1,4,6,7,9],[2,3,5,8,9],[2,3,6,7,9],[2,4,5,7,9],[3,4,5,6,9],[1,3,7,8,6],[1,4,6,8,5],[2,3,6,8,5],[2,4,5,8,6],[3,4,5,7,6]]
```
**Explanation:** Multiple valid combinations of 5 numbers summing to 25. (Note: Output order may vary)

---

## Problem 4: Optimal Shopping Strategy

**Difficulty:** Medium
**Company:** Amazon, Google, Microsoft

### Problem Statement

An e-commerce platform is optimizing their shopping cart system with special bundle offers. In the online store, there are `n` items to sell. Each item has a price. However, there are some special offers, and a special offer consists of one or more different kinds of items with a sale price.

You are given an integer array `price` where `price[i]` is the price of the `i-th` item, and an integer array `needs` where `needs[i]` is the number of pieces of the `i-th` item you want to buy.

You are also given an array `special` where `special[i]` is of size `n + 1` where `special[i][j]` is the number of pieces of the `j-th` item in the `i-th` offer and `special[i][n]` (i.e., the last integer in the array) is the price of the `i-th` offer.

Return the lowest price you have to pay for exactly certain items as given, where you could make optimal use of the special offers. You are not allowed to buy more items than you want, even if that would lower the overall price. You could use any of the special offers as many times as you want.

### Input Format
- First line: Array `price` (price of each item)
- Second line: Array `special` (special offers where last element is offer price)
- Third line: Array `needs` (quantity needed for each item)

### Output Format
- Return a single integer representing the minimum total price

### Constraints
- `n == price.length == needs.length`
- `1 <= n <= 6`
- `0 <= price[i], needs[i] <= 10`
- `1 <= special.length <= 100`
- `special[i].length == n + 1`
- `0 <= special[i][j] <= 50`
- The input is generated that at least one of `special[i][j]` is non-zero for `0 <= j <= n - 1`.

### Examples

**Example 1:**
```
Input:
price = [2,5]
special = [[3,0,5],[1,2,10]]
needs = [3,2]
Output: 14
Explanation: There are two kinds of items, A and B. Their prices are $2 and $5 respectively.
In special offer 1, you can pay $5 for 3A and 0B.
In special offer 2, you can pay $10 for 1A and 2B.
You need to buy 3A and 2B, so you may pay $10 for 1A and 2B (special offer 2), and $4 for 2A.
```

**Example 2:**
```
Input:
price = [2,3,4]
special = [[1,1,0,4],[2,2,1,9]]
needs = [1,2,1]
Output: 11
Explanation: The price of A is $2, and $3 for B, $4 for C.
You may pay $4 for 1A and 1B, and $9 for 2A ,2B and 1C.
You need to buy 1A ,2B and 1C, so you may pay $4 for 1A and 1B (special offer 1), and $3 for 1B, $4 for 1C.
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
**Explanation:** Buy special offer 2 (1A+2B for $10) and 2A individually for $4. Total: $14.

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
**Explanation:** Buy special offer 1 (1A+1B for $4), then 1B ($3) and 1C ($4). Total: $11.

---

#### Test Case 3
**Input:**
```
price = [2,2]
special = [[1,1,1]]
needs = [2,2]
```
**Output:**
```
2
```
**Explanation:** Buy special offer twice (1A+1B for $1 each time). Total: $2.

---

#### Test Case 4
**Input:**
```
price = [10]
special = [[1,8]]
needs = [1]
```
**Output:**
```
8
```
**Explanation:** Use special offer to buy 1 item for $8 instead of $10.

---

#### Test Case 5
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
**Explanation:** Buy special offer twice for total $2, much cheaper than $36 regular price.

---

#### Test Case 6
**Input:**
```
price = [3,4]
special = [[2,2,6]]
needs = [1,1]
```
**Output:**
```
7
```
**Explanation:** Special offer gives 2A+2B for $6, but we only need 1A+1B. Buy individually: $3+$4=$7.

---

#### Test Case 7
**Input:**
```
price = [2,3,4]
special = [[1,1,1,5]]
needs = [2,2,2]
```
**Output:**
```
10
```
**Explanation:** Buy special offer twice (1A+1B+1C for $5 each). Total: $10.

---

#### Test Case 8
**Input:**
```
price = [5]
special = [[1,3]]
needs = [5]
```
**Output:**
```
15
```
**Explanation:** Buy special offer 5 times (1 item for $3 each). Total: $15.

---

#### Test Case 9
**Input:**
```
price = [1,1,1]
special = [[1,1,1,0]]
needs = [3,3,3]
```
**Output:**
```
0
```
**Explanation:** Special offer gives 1A+1B+1C for free ($0). Use it 3 times. Total: $0.

---

#### Test Case 10
**Input:**
```
price = [10,10,10]
special = [[1,0,0,8],[0,1,0,8],[0,0,1,8],[1,1,1,20]]
needs = [2,2,2]
```
**Output:**
```
40
```
**Explanation:** Buy bundle offer twice (1A+1B+1C for $20 each). Total: 2 × $20 = $40. This is cheaper than individual special offers (which would be $48).

---

**End of Coding Problems**
