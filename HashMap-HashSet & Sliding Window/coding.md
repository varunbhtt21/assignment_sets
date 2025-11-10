# HashMap/HashSet & Sliding Window - Coding Problems

---

## Problem 1: String Character Difference Validator

**Difficulty:** Medium
**Company:** Amazon, Google, Microsoft

### Problem Statement

A text processing system for a document management platform needs to validate string similarity. The system receives a list of strings where all strings have the same length. Your task is to determine if there exist exactly 2 strings that differ by only 1 character at the same index position.

Given a list of strings `dict` where all the strings are of the same length, return `true` if there are 2 strings that only differ by 1 character in the same index, otherwise return `false`.

### Input Format
- A list of strings `dict` where all strings have equal length

### Output Format
- Return `true` if there exist 2 strings differing by exactly 1 character at the same index, otherwise return `false`

### Constraints
- The number of characters in `dict` <= 10^5
- `dict[i].length == dict[j].length`
- `dict[i]` should be unique
- `dict[i]` contains only lowercase English letters

### Examples

**Example 1:**
```
Input: ["abcd","acbd","aacd"]
Output: true
Explanation: Strings "abcd" and "aacd" differ only by one character in the index 1.
```

**Example 2:**
```
Input: ["ab","cd","yz"]
Output: false
```

**Example 3:**
```
Input: ["abcd","cccc","abyd","abab"]
Output: true
```

### Test Cases

#### Test Case 1
**Input:**
```
["abcd","acbd","aacd"]
```
**Output:**
```
true
```
**Explanation:** Strings "abcd" and "aacd" differ only by one character at index 1 ('b' vs 'a').

---

#### Test Case 2
**Input:**
```
["ab","cd","yz"]
```
**Output:**
```
false
```
**Explanation:** No two strings differ by exactly one character. Each pair differs by 2 characters.

---

#### Test Case 3
**Input:**
```
["abcd","cccc","abyd","abab"]
```
**Output:**
```
true
```
**Explanation:** Strings "abcd" and "abyd" differ only at index 2 ('c' vs 'y').

---

#### Test Case 4
**Input:**
```
["abc"]
```
**Output:**
```
false
```
**Explanation:** Only one string exists, so no pair can be found.

---

#### Test Case 5
**Input:**
```
["abc","abd"]
```
**Output:**
```
true
```
**Explanation:** "abc" and "abd" differ only at index 2 ('c' vs 'd').

---

#### Test Case 6
**Input:**
```
["abcde","abfde","abcdf"]
```
**Output:**
```
true
```
**Explanation:** "abcde" and "abfde" differ only at index 2 ('c' vs 'f').

---

#### Test Case 7
**Input:**
```
["aa","bb","cc","dd"]
```
**Output:**
```
false
```
**Explanation:** Every pair of strings differs by 2 characters (both positions).

---

#### Test Case 8
**Input:**
```
["a","b","c","d","e"]
```
**Output:**
```
true
```
**Explanation:** All single-character strings differ by 1 character at the same index (index 0). For example, "a" and "b" differ only at index 0, satisfying the condition.

---

#### Test Case 9
**Input:**
```
["abcdefgh","abcdefgi","abcdefgj"]
```
**Output:**
```
true
```
**Explanation:** "abcdefgh" and "abcdefgi" differ only at index 7 ('h' vs 'i').

---

#### Test Case 10
**Input:**
```
["hello","world","hella","helps"]
```
**Output:**
```
true
```
**Explanation:** "hello" and "hella" differ only at index 4 ('o' vs 'a').

---

## Problem 2: Repeated DNA Sequence Finder

**Difficulty:** Medium
**Company:** LinkedIn, Amazon, Google

### Problem Statement

A bioinformatics research lab is analyzing DNA sequences to identify patterns. The DNA sequence is composed of a series of nucleotides abbreviated as 'A', 'C', 'G', and 'T'. For example, "ACGAATTCCG" is a DNA sequence.

When studying DNA, it is useful to identify repeated sequences within the DNA. Given a string `s` that represents a DNA sequence, return all the 10-letter-long sequences (substrings) that occur more than once in a DNA molecule. You may return the answer in any order.

### Input Format
- A string `s` representing a DNA sequence

### Output Format
- Return a list of all 10-letter-long sequences that appear more than once

### Constraints
- `1 <= s.length <= 10^5`
- `s[i]` is either 'A', 'C', 'G', or 'T'

### Examples

**Example 1:**
```
Input: s = "AAAAACCCCCAAAAACCCCCCAAAAAGGGTTT"
Output: ["AAAAACCCCC","CCCCCAAAAA"]
```

**Example 2:**
```
Input: s = "AAAAAAAAAAAAA"
Output: ["AAAAAAAAAA"]
```

### Test Cases

#### Test Case 1
**Input:**
```
"AAAAACCCCCAAAAACCCCCCAAAAAGGGTTT"
```
**Output:**
```
["AAAAACCCCC","CCCCCAAAAA"]
```
**Explanation:** "AAAAACCCCC" appears at positions 0 and 6. "CCCCCAAAAA" appears at positions 5 and 11.

---

#### Test Case 2
**Input:**
```
"AAAAAAAAAAAAA"
```
**Output:**
```
["AAAAAAAAAA"]
```
**Explanation:** "AAAAAAAAAA" appears at positions 0, 1, 2, and 3 (overlapping occurrences).

---

#### Test Case 3
**Input:**
```
"AAAAAAAAAAA"
```
**Output:**
```
["AAAAAAAAAA"]
```
**Explanation:** In a string of 11 A's, the 10-letter sequence "AAAAAAAAAA" appears at positions 0 and 1.

---

#### Test Case 4
**Input:**
```
"ACGTACGTAC"
```
**Output:**
```
[]
```
**Explanation:** String length is exactly 10, so only one 10-letter sequence exists and cannot repeat.

---

#### Test Case 5
**Input:**
```
"ACGTACGTACGTACGTACGT"
```
**Output:**
```
["ACGTACGTAC","CGTACGTACG","GTACGTACGT","TACGTACGTA"]
```
**Explanation:** Due to the repeating pattern, multiple 10-letter sequences appear more than once. For example, "ACGTACGTAC" appears at positions 0, 4, 8, etc.

---

#### Test Case 6
**Input:**
```
"GAGAGAGAGAGAGAGAGAGA"
```
**Output:**
```
["GAGAGAGAGA","AGAGAGAGAG"]
```
**Explanation:** Both "GAGAGAGAGA" and "AGAGAGAGAG" appear multiple times due to the repeating pattern.

---

#### Test Case 7
**Input:**
```
"ATCGATCGATCGATCGATCG"
```
**Output:**
```
["ATCGATCGAT","CGATCGATCG","GATCGATCGA","TCGATCGATC"]
```
**Explanation:** Due to the repeating pattern "ATCG", multiple 10-letter sequences appear more than once throughout the string.

---

#### Test Case 8
**Input:**
```
"GGGGGGGGGG"
```
**Output:**
```
[]
```
**Explanation:** String is exactly 10 characters long, so no 10-letter sequence can repeat.

---

#### Test Case 9
**Input:**
```
"AAAAAAAAAAC"
```
**Output:**
```
[]
```
**Explanation:** String length is 11. The only 10-letter sequences are "AAAAAAAAAA" (positions 0) and "AAAAAAAAA C" (position 1). These are different sequences, so no sequence repeats.

---

#### Test Case 10
**Input:**
```
"TTTTTTTTTTTTTT"
```
**Output:**
```
["TTTTTTTTTT"]
```
**Explanation:** "TTTTTTTTTT" appears at positions 0, 1, 2, 3, and 4.

---

## Problem 3: Maximum Consecutive Ones with One Flip

**Difficulty:** Medium
**Company:** Google, Facebook, Microsoft

### Problem Statement

A data analytics platform is optimizing their binary signal processing system. Given a binary array `nums`, you need to find the maximum number of consecutive 1's in the array if you can flip at most one 0.

Return the maximum number of consecutive 1's in the array if you can flip at most one 0.

### Input Format
- A binary array `nums` containing only 0s and 1s

### Output Format
- Return an integer representing the maximum number of consecutive 1's possible

### Constraints
- `1 <= nums.length <= 10^5`
- `nums[i]` is either 0 or 1

### Examples

**Example 1:**
```
Input: nums = [1,0,1,1,0]
Output: 4
Explanation:
- If we flip the first zero, nums becomes [1,1,1,1,0] and we have 4 consecutive ones.
- If we flip the second zero, nums becomes [1,0,1,1,1] and we have 3 consecutive ones.
The max number of consecutive ones is 4.
```

**Example 2:**
```
Input: nums = [1,0,1,1,0,1]
Output: 4
Explanation:
- If we flip the first zero, nums becomes [1,1,1,1,0,1] and we have 4 consecutive ones.
- If we flip the second zero, nums becomes [1,0,1,1,1,1] and we have 4 consecutive ones.
The max number of consecutive ones is 4.
```

### Test Cases

#### Test Case 1
**Input:**
```
[1,0,1,1,0]
```
**Output:**
```
4
```
**Explanation:** Flip the first 0 to get [1,1,1,1,0], which gives 4 consecutive ones.

---

#### Test Case 2
**Input:**
```
[1,0,1,1,0,1]
```
**Output:**
```
4
```
**Explanation:** Flip the first 0 to get [1,1,1,1,0,1], which gives 4 consecutive ones.

---

#### Test Case 3
**Input:**
```
[1,1,1,1,1]
```
**Output:**
```
5
```
**Explanation:** All elements are already 1, so the maximum is 5 without needing to flip.

---

#### Test Case 4
**Input:**
```
[0,0,0,0,0]
```
**Output:**
```
1
```
**Explanation:** We can flip at most one 0 to get a single 1.

---

#### Test Case 5
**Input:**
```
[1]
```
**Output:**
```
1
```
**Explanation:** Single element array with value 1.

---

#### Test Case 6
**Input:**
```
[0]
```
**Output:**
```
1
```
**Explanation:** Flip the single 0 to get 1.

---

#### Test Case 7
**Input:**
```
[1,0,1,0,1,0,1]
```
**Output:**
```
3
```
**Explanation:** Flip any 0 to connect two consecutive 1's, giving 3 consecutive ones.

---

#### Test Case 8
**Input:**
```
[1,1,0,1,1,1,0,1,1]
```
**Output:**
```
6
```
**Explanation:** Flip the 0 at index 2 to get [1,1,1,1,1,1,0,1,1], which gives 6 consecutive ones.

---

#### Test Case 9
**Input:**
```
[0,1,1,1,1,0,1,1,1]
```
**Output:**
```
8
```
**Explanation:** Flip the 0 at index 5 to get [0,1,1,1,1,1,1,1,1], which gives 8 consecutive ones starting from index 1.

---

#### Test Case 10
**Input:**
```
[1,1,1,0,0,1,1,1]
```
**Output:**
```
4
```
**Explanation:** Flip either the 0 at index 3 or 4 to connect segments, giving 4 consecutive ones.

---

## Problem 4: Customer Satisfaction Optimizer

**Difficulty:** Medium
**Company:** Amazon, Google, Apple

### Problem Statement

A retail store is analyzing customer satisfaction patterns. The store is open for `n` minutes, and you are given an integer array `customers` of length `n` where `customers[i]` is the number of customers that enter the store at the start of the i-th minute, and all those customers leave after the end of that minute.

During certain minutes, the bookstore owner is grumpy. You are given a binary array `grumpy` where `grumpy[i]` is 1 if the bookstore owner is grumpy during the i-th minute, and is 0 otherwise.

When the bookstore owner is grumpy, the customers entering during that minute are not satisfied. Otherwise, they are satisfied.

The bookstore owner knows a secret technique to remain not grumpy for `minutes` consecutive minutes, but this technique can only be used once.

Return the maximum number of customers that can be satisfied throughout the day.

### Input Format
- First line: Integer array `customers` of length `n`
- Second line: Binary array `grumpy` of length `n`
- Third line: Integer `minutes` (length of the technique window)

### Output Format
- Return an integer representing the maximum number of satisfied customers

### Constraints
- `n == customers.length == grumpy.length`
- `1 <= minutes <= n <= 2 * 10^4`
- `0 <= customers[i] <= 1000`
- `grumpy[i]` is either 0 or 1

### Examples

**Example 1:**
```
Input: customers = [1,0,1,2,1,1,7,5], grumpy = [0,1,0,1,0,1,0,1], minutes = 3
Output: 16
Explanation:
The bookstore owner keeps themselves not grumpy for the last 3 minutes.
The maximum number of customers that can be satisfied = 1 + 1 + 1 + 1 + 7 + 5 = 16.
```

**Example 2:**
```
Input: customers = [1], grumpy = [0], minutes = 1
Output: 1
```

### Test Cases

#### Test Case 1
**Input:**
```
customers = [1,0,1,2,1,1,7,5]
grumpy = [0,1,0,1,0,1,0,1]
minutes = 3
```
**Output:**
```
16
```
**Explanation:** The bookstore owner keeps themselves not grumpy for the last 3 minutes. The maximum number of customers that can be satisfied = 1 + 1 + 1 + 1 + 7 + 5 = 16.

---

#### Test Case 2
**Input:**
```
customers = [1]
grumpy = [0]
minutes = 1
```
**Output:**
```
1
```
**Explanation:** Single customer and owner is not grumpy, so 1 customer is satisfied.

---

#### Test Case 3
**Input:**
```
customers = [1]
grumpy = [1]
minutes = 1
```
**Output:**
```
1
```
**Explanation:** Owner uses the technique for the single minute, satisfying 1 customer.

---

#### Test Case 4
**Input:**
```
customers = [4,10,10]
grumpy = [1,1,0]
minutes = 2
```
**Output:**
```
24
```
**Explanation:** Use technique on first 2 minutes (both grumpy). Total: 4 + 10 + 10 = 24.

---

#### Test Case 5
**Input:**
```
customers = [2,6,6,9]
grumpy = [0,0,1,1]
minutes = 1
```
**Output:**
```
17
```
**Explanation:** Already satisfied: 2 + 6 = 8. Use technique on minute 3 (9 customers): 8 + 9 = 17.

---

#### Test Case 6
**Input:**
```
customers = [3,8,7,1]
grumpy = [1,0,1,1]
minutes = 3
```
**Output:**
```
18
```
**Explanation:** Already satisfied: 8 (minute 1, grumpy=0). Best 3-minute window is [0,1,2] which saves 3+0+7=10 additional customers. Total: 8 + 10 = 18.

---

#### Test Case 7
**Input:**
```
customers = [5,5,5,5,5]
grumpy = [0,0,0,0,0]
minutes = 3
```
**Output:**
```
25
```
**Explanation:** Owner is never grumpy, so all 25 customers are satisfied regardless of technique usage.

---

#### Test Case 8
**Input:**
```
customers = [5,5,5,5,5]
grumpy = [1,1,1,1,1]
minutes = 3
```
**Output:**
```
15
```
**Explanation:** All minutes are grumpy. Use technique on any 3 consecutive minutes: 5 + 5 + 5 = 15.

---

#### Test Case 9
**Input:**
```
customers = [10,20,30,40,50]
grumpy = [1,0,1,0,1]
minutes = 2
```
**Output:**
```
110
```
**Explanation:** Already satisfied: 20 + 40 = 60 (minutes with grumpy=0). Best 2-minute window is [3,4] which saves 0+50=50 additional customers. Total: 60 + 50 = 110.

---

#### Test Case 10
**Input:**
```
customers = [1,2,3,4,5,6,7,8,9,10]
grumpy = [1,0,1,0,1,0,1,0,1,0]
minutes = 3
```
**Output:**
```
46
```
**Explanation:** Already satisfied (non-grumpy): 2 + 4 + 6 + 8 + 10 = 30. Best 3-minute window covering grumpy minutes: positions 4-6 gives 5 + 6 + 7 = 18, but position 5 is not grumpy. Window 6-8: 7 + 8 + 9 = 24, but positions 7 is not grumpy. Best window: 4-6 saves 5 + 7 = 12. Actually, window 6-8 saves 7 + 9 = 16. Total: 30 + 16 = 46.

---

**End of Coding Problems**
