# Extra Problems - Dynamic Programming
## (Advanced DP Challenges)

---

## Problem 1: Array Jump Navigator

**Difficulty:** Medium
**Company:** Google, Amazon, Microsoft

### Problem Statement

A game developer is creating a platformer game where the player must navigate through obstacles. You are given an integer array `nums`. You are initially positioned at the array's first index, and each element in the array represents your maximum jump length at that position.

Return `true` if you can reach the last index, or `false` otherwise.

### Input Format
- An integer array `nums` where `nums[i]` represents maximum jump length at position i

### Output Format
- Return a boolean: `true` if last index is reachable, `false` otherwise

### Constraints
- `1 <= nums.length <= 10^4`
- `0 <= nums[i] <= 10^5`

### Examples

**Example 1:**
```
Input: nums = [2,3,1,1,4]
Output: true
Explanation: Jump 1 step from index 0 to 1, then 3 steps to the last index.
```

**Example 2:**
```
Input: nums = [3,2,1,0,4]
Output: false
Explanation: You will always arrive at index 3 no matter what. Its maximum jump length is 0, which makes it impossible to reach the last index.
```

### Test Cases

#### Test Case 1
**Input:**
```
[2,3,1,1,4]
```
**Output:**
```
true
```
**Explanation:** From index 0, jump 1 step to index 1 (can jump up to 2). From index 1, jump 3 steps to index 4 (last index). Path exists.

---

#### Test Case 2
**Input:**
```
[3,2,1,0,4]
```
**Output:**
```
false
```
**Explanation:** All paths lead to index 3 which has jump length 0. Cannot progress further to reach index 4.

---

#### Test Case 3
**Input:**
```
[0]
```
**Output:**
```
true
```
**Explanation:** Already at the last index (array length is 1).

---

#### Test Case 4
**Input:**
```
[1,1,1,1]
```
**Output:**
```
true
```
**Explanation:** Jump 1 step at a time: 0→1→2→3. Reaches last index.

---

#### Test Case 5
**Input:**
```
[1,0,1,0]
```
**Output:**
```
false
```
**Explanation:** From index 0, can only reach index 1. From index 1, jump length is 0, cannot proceed.

---

#### Test Case 6
**Input:**
```
[2,5,0,0]
```
**Output:**
```
true
```
**Explanation:** From index 0, jump 1 step to index 1. From index 1, jump 2 steps to index 3 (last index).

---

#### Test Case 7
**Input:**
```
[1,2,3]
```
**Output:**
```
true
```
**Explanation:** Multiple paths exist. Can jump directly from index 0→1→3 or 0→2→3.

---

#### Test Case 8
**Input:**
```
[0,2,3]
```
**Output:**
```
false
```
**Explanation:** Cannot move from index 0 as jump length is 0.

---

#### Test Case 9
**Input:**
```
[5,9,3,2,1,0,2,3,3,1,0,0]
```
**Output:**
```
true
```
**Explanation:** From index 0, can jump up to 5 positions. Can reach beyond the zero at index 5 by jumping from earlier positions.

---

#### Test Case 10
**Input:**
```
[1,1,0,1]
```
**Output:**
```
false
```
**Explanation:** From index 0→1→2. At index 2, jump length is 0, cannot reach index 3.

---

## Problem 2: Stock Trading Profit Maximizer

**Difficulty:** Easy
**Company:** Amazon, Microsoft, Facebook

### Problem Statement

A financial analyst is developing a stock trading strategy tool. You are given an array `prices` where `prices[i]` is the price of a given stock on the i-th day.

You want to maximize your profit by choosing a single day to buy one stock and choosing a different day in the future to sell that stock.

Return the maximum profit you can achieve from this transaction. If you cannot achieve any profit, return 0.

### Input Format
- An integer array `prices` where `prices[i]` is the stock price on day i

### Output Format
- Return an integer representing the maximum profit

### Constraints
- `1 <= prices.length <= 10^5`
- `0 <= prices[i] <= 10^4`

### Examples

**Example 1:**
```
Input: prices = [7,1,5,3,6,4]
Output: 5
Explanation: Buy on day 2 (price = 1) and sell on day 5 (price = 6), profit = 6-1 = 5.
```

**Example 2:**
```
Input: prices = [7,6,4,3,1]
Output: 0
Explanation: No transactions are done and the max profit = 0.
```

### Test Cases

#### Test Case 1
**Input:**
```
[7,1,5,3,6,4]
```
**Output:**
```
5
```
**Explanation:** Buy at price 1 (day 2), sell at price 6 (day 5). Profit = 6 - 1 = 5.

---

#### Test Case 2
**Input:**
```
[7,6,4,3,1]
```
**Output:**
```
0
```
**Explanation:** Prices continuously decrease. No profitable transaction possible.

---

#### Test Case 3
**Input:**
```
[1,2]
```
**Output:**
```
1
```
**Explanation:** Buy at price 1, sell at price 2. Profit = 1.

---

#### Test Case 4
**Input:**
```
[2,4,1]
```
**Output:**
```
2
```
**Explanation:** Buy at price 2, sell at price 4. Profit = 2.

---

#### Test Case 5
**Input:**
```
[3,3,5,0,0,3,1,4]
```
**Output:**
```
4
```
**Explanation:** Buy at price 0 (day 4), sell at price 4 (day 8). Profit = 4.

---

#### Test Case 6
**Input:**
```
[1,4,2]
```
**Output:**
```
3
```
**Explanation:** Buy at price 1, sell at price 4. Profit = 3.

---

#### Test Case 7
**Input:**
```
[2,1,2,0,1]
```
**Output:**
```
1
```
**Explanation:** Multiple options give profit 1. Buy at 0, sell at 1, or buy at 1, sell at 2.

---

#### Test Case 8
**Input:**
```
[5]
```
**Output:**
```
0
```
**Explanation:** Only one day, cannot buy and sell.

---

#### Test Case 9
**Input:**
```
[10,9,8,7,6,5,4,3,2,1]
```
**Output:**
```
0
```
**Explanation:** Continuously decreasing prices, no profit possible.

---

#### Test Case 10
**Input:**
```
[1,2,3,4,5,6,7,8,9,10]
```
**Output:**
```
9
```
**Explanation:** Buy at price 1 (day 1), sell at price 10 (day 10). Profit = 9.

---

## Problem 3: House Robbery Strategy Planner

**Difficulty:** Medium
**Company:** Amazon, Microsoft, Google

### Problem Statement

A security consultant is analyzing potential theft scenarios for insurance purposes. You are a professional robber planning to rob houses along a street. Each house has a certain amount of money stashed. The only constraint is that adjacent houses have security systems connected, and it will automatically contact the police if two adjacent houses were broken into on the same night.

Given an integer array `nums` representing the amount of money of each house, return the maximum amount of money you can rob tonight without alerting the police.

### Input Format
- An integer array `nums` where `nums[i]` represents money in house i

### Output Format
- Return an integer representing maximum money that can be robbed

### Constraints
- `1 <= nums.length <= 100`
- `0 <= nums[i] <= 400`

### Examples

**Example 1:**
```
Input: nums = [1,2,3,1]
Output: 4
Explanation: Rob house 1 (money = 1) and then rob house 3 (money = 3).
Total amount you can rob = 1 + 3 = 4.
```

**Example 2:**
```
Input: nums = [2,7,9,3,1]
Output: 12
Explanation: Rob house 1 (money = 2), rob house 3 (money = 9) and rob house 5 (money = 1).
Total amount you can rob = 2 + 9 + 1 = 12.
```

### Test Cases

#### Test Case 1
**Input:**
```
[1,2,3,1]
```
**Output:**
```
4
```
**Explanation:** Rob houses at index 0 and 2. Total = 1 + 3 = 4.

---

#### Test Case 2
**Input:**
```
[2,7,9,3,1]
```
**Output:**
```
12
```
**Explanation:** Rob houses at index 0, 2, and 4. Total = 2 + 9 + 1 = 12.

---

#### Test Case 3
**Input:**
```
[5,3,4,11,2]
```
**Output:**
```
16
```
**Explanation:** Rob houses at index 0 and 3. Total = 5 + 11 = 16.

---

#### Test Case 4
**Input:**
```
[1]
```
**Output:**
```
1
```
**Explanation:** Only one house, rob it for total = 1.

---

#### Test Case 5
**Input:**
```
[2,1,1,2]
```
**Output:**
```
4
```
**Explanation:** Rob houses at index 0 and 3. Total = 2 + 2 = 4.

---

#### Test Case 6
**Input:**
```
[5,1,1,5]
```
**Output:**
```
10
```
**Explanation:** Rob houses at index 0 and 3. Total = 5 + 5 = 10.

---

#### Test Case 7
**Input:**
```
[100,1,1,100]
```
**Output:**
```
200
```
**Explanation:** Rob houses at index 0 and 3. Total = 100 + 100 = 200.

---

#### Test Case 8
**Input:**
```
[1,3,1]
```
**Output:**
```
3
```
**Explanation:** Rob house at index 1. Total = 3.

---

#### Test Case 9
**Input:**
```
[2,9,8,3,6]
```
**Output:**
```
16
```
**Explanation:** Rob houses at index 0, 2, and 4. Total = 2 + 8 + 6 = 16.

---

#### Test Case 10
**Input:**
```
[10,5,2,7,10,100,50]
```
**Output:**
```
117
```
**Explanation:** Rob houses at index 0, 3, 5. Total = 10 + 7 + 100 = 117.

---

## Problem 4: Binary String Subset Analyzer

**Difficulty:** Medium
**Company:** Google, Facebook, Amazon

### Problem Statement

A data compression team is analyzing binary patterns. You are given an array of binary strings `strs` and two integers `m` and `n`.

Return the size of the largest subset of `strs` such that there are at most `m` 0's and `n` 1's in the subset.

A set x is a subset of a set y if all elements of x are also elements of y.

### Input Format
- First line: Array of binary strings `strs`
- Second line: Integer `m` (maximum 0's allowed)
- Third line: Integer `n` (maximum 1's allowed)

### Output Format
- Return an integer representing the size of the largest subset

### Constraints
- `1 <= strs.length <= 600`
- `1 <= strs[i].length <= 100`
- `strs[i]` consists only of digits '0' and '1'
- `1 <= m, n <= 100`

### Examples

**Example 1:**
```
Input: strs = ["10","0001","111001","1","0"], m = 5, n = 3
Output: 4
Explanation: The largest subset with at most 5 0's and 3 1's is {"10", "0001", "1", "0"}, so the answer is 4.
```

**Example 2:**
```
Input: strs = ["10","0","1"], m = 1, n = 1
Output: 2
Explanation: The largest subset is {"0", "1"}, so the answer is 2.
```

### Test Cases

#### Test Case 1
**Input:**
```
strs = ["10","0001","111001","1","0"]
m = 5
n = 3
```
**Output:**
```
4
```
**Explanation:** Subset {"10", "0001", "1", "0"} has 5 zeros and 3 ones. Size = 4.

---

#### Test Case 2
**Input:**
```
strs = ["10","0","1"]
m = 1
n = 1
```
**Output:**
```
2
```
**Explanation:** Subset {"0", "1"} has 1 zero and 1 one. Size = 2.

---

#### Test Case 3
**Input:**
```
strs = ["0","1","0","1","0"]
m = 3
n = 2
```
**Output:**
```
5
```
**Explanation:** Can take all strings. Total = 3 zeros, 2 ones. Size = 5.

---

#### Test Case 4
**Input:**
```
strs = ["111","1000","1000","1000"]
m = 9
n = 3
```
**Output:**
```
3
```
**Explanation:** Subset {"1000", "1000", "1000"} has 9 zeros and 3 ones. Size = 3.

---

#### Test Case 5
**Input:**
```
strs = ["10","0001"]
m = 5
n = 3
```
**Output:**
```
2
```
**Explanation:** Can take both strings. "10" = 1 zero, 1 one. "0001" = 3 zeros, 1 one. Total = 4 zeros, 2 ones. Size = 2.

---

#### Test Case 6
**Input:**
```
strs = ["0","11","1000","01","0","101","1","1","1","0","0","0","0","1","0","0110101","0","11","01","00","01111","0","10","0","11","0","0","0","0","101","001110","1","0","1","011","11","11","0","10","0000","0","1","0","0","0","101","001010","0","10","1","1","1","011","0","10","0","1","1","1","1"]
m = 50
n = 50
```
**Output:**
```
58
```
**Explanation:** Optimal subset selection gives 58 strings that fit within the constraints of 50 zeros and 50 ones.

---

#### Test Case 7
**Input:**
```
strs = ["0","0","1","1"]
m = 2
n = 2
```
**Output:**
```
4
```
**Explanation:** Can take all 4 strings. Total = 2 zeros, 2 ones. Size = 4.

---

#### Test Case 8
**Input:**
```
strs = ["111","1000"]
m = 3
n = 3
```
**Output:**
```
1
```
**Explanation:** Can only take "111" (0 zeros, 3 ones) or "1000" (3 zeros, 1 one). Size = 1.

---

#### Test Case 9
**Input:**
```
strs = ["00","000","0000","00000"]
m = 10
n = 0
```
**Output:**
```
3
```
**Explanation:** Subset {"00", "000", "0000"} has 9 zeros, 0 ones. Size = 3.

---

#### Test Case 10
**Input:**
```
strs = ["1","0","1","0","1"]
m = 2
n = 3
```
**Output:**
```
5
```
**Explanation:** Can take all strings. Total = 2 zeros, 3 ones. Size = 5.

---

## Problem 5: Coin Change Calculator

**Difficulty:** Medium
**Company:** Amazon, Google, Microsoft

### Problem Statement

A payment processing system needs to optimize cash transactions. You are given an integer array `coins` representing coins of different denominations and an integer `amount` representing a total amount of money.

Return the fewest number of coins that you need to make up that amount. If that amount of money cannot be made up by any combination of the coins, return -1.

You may assume that you have an infinite number of each kind of coin.

### Input Format
- First line: Integer array `coins` representing available coin denominations
- Second line: Integer `amount` representing target amount

### Output Format
- Return an integer representing minimum number of coins needed, or -1 if impossible

### Constraints
- `1 <= coins.length <= 12`
- `1 <= coins[i] <= 2^31 - 1`
- `0 <= amount <= 10^4`

### Examples

**Example 1:**
```
Input: coins = [1,2,5], amount = 11
Output: 3
Explanation: 11 = 5 + 5 + 1
```

**Example 2:**
```
Input: coins = [2], amount = 3
Output: -1
```

**Example 3:**
```
Input: coins = [1], amount = 0
Output: 0
```

### Test Cases

#### Test Case 1
**Input:**
```
coins = [1,2,5]
amount = 11
```
**Output:**
```
3
```
**Explanation:** 11 = 5 + 5 + 1. Minimum 3 coins needed.

---

#### Test Case 2
**Input:**
```
coins = [2]
amount = 3
```
**Output:**
```
-1
```
**Explanation:** Cannot make amount 3 with only coin denomination 2.

---

#### Test Case 3
**Input:**
```
coins = [1]
amount = 0
```
**Output:**
```
0
```
**Explanation:** No coins needed for amount 0.

---

#### Test Case 4
**Input:**
```
coins = [1,2,5]
amount = 100
```
**Output:**
```
20
```
**Explanation:** 100 = 20 × 5. Minimum 20 coins of denomination 5.

---

#### Test Case 5
**Input:**
```
coins = [1,3,4,5]
amount = 7
```
**Output:**
```
2
```
**Explanation:** 7 = 3 + 4. Minimum 2 coins.

---

#### Test Case 6
**Input:**
```
coins = [2,5,10,1]
amount = 27
```
**Output:**
```
4
```
**Explanation:** 27 = 10 + 10 + 5 + 2. Minimum 4 coins.

---

#### Test Case 7
**Input:**
```
coins = [186,419,83,408]
amount = 6249
```
**Output:**
```
20
```
**Explanation:** Optimal combination uses 20 coins to make 6249.

---

#### Test Case 8
**Input:**
```
coins = [1,2147483647]
amount = 2
```
**Output:**
```
2
```
**Explanation:** 2 = 1 + 1. Need 2 coins of denomination 1.

---

#### Test Case 9
**Input:**
```
coins = [3,7,405,436]
amount = 8839
```
**Output:**
```
25
```
**Explanation:** Optimal combination uses 25 coins to make 8839.

---

#### Test Case 10
**Input:**
```
coins = [1,5,10,25]
amount = 63
```
**Output:**
```
6
```
**Explanation:** 63 = 25 + 25 + 10 + 1 + 1 + 1. Minimum 6 coins.

---

**End of Coding Problems**
