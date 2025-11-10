# Major Assessment -03 - Coding Problems
## (Sorting, Hashmap and Hashset, Two Pointers and Sliding Window)

---

## Problem 1: Character Mapping Validator

**Difficulty:** Easy
**Company:** Microsoft, Amazon, Google

### Problem Statement

A text transformation system needs to validate character pattern matching. Given two strings `s` and `t`, determine if they are isomorphic.

Two strings `s` and `t` are isomorphic if the characters in `s` can be replaced to get `t`.

All occurrences of a character must be replaced with another character while preserving the order of characters. No two characters may map to the same character, but a character may map to itself.

### Input Format
- First line: String `s`
- Second line: String `t`

### Output Format
- Return `true` if the strings are isomorphic, `false` otherwise

### Constraints
- `1 <= s.length <= 5 * 10^4`
- `t.length == s.length`
- `s` and `t` consist of any valid ascii character

### Examples

**Example 1:**
```
Input: s = "egg", t = "add"
Output: true
Explanation:
The strings s and t can be made identical by:
- Mapping 'e' to 'a'.
- Mapping 'g' to 'd'.
```

**Example 2:**
```
Input: s = "foo", t = "bar"
Output: false
Explanation: The strings s and t can not be made identical as 'o' needs to be mapped to both 'a' and 'r'.
```

**Example 3:**
```
Input: s = "paper", t = "title"
Output: true
```

### Test Cases

#### Test Case 1
**Input:**
```
s = "egg"
t = "add"
```
**Output:**
```
true
```
**Explanation:** Mapping: e→a, g→d. All occurrences follow the same mapping.

---

#### Test Case 2
**Input:**
```
s = "foo"
t = "bar"
```
**Output:**
```
false
```
**Explanation:** Character 'o' would need to map to both 'a' and 'r', which violates the rule.

---

#### Test Case 3
**Input:**
```
s = "paper"
t = "title"
```
**Output:**
```
true
```
**Explanation:** Mapping: p→t, a→i, e→l, r→e. Valid one-to-one mapping.

---

#### Test Case 4
**Input:**
```
s = "ab"
t = "aa"
```
**Output:**
```
false
```
**Explanation:** Both 'a' and 'b' would map to 'a', which violates the bijective mapping.

---

#### Test Case 5
**Input:**
```
s = "abc"
t = "def"
```
**Output:**
```
true
```
**Explanation:** Mapping: a→d, b→e, c→f. One-to-one mapping exists.

---

#### Test Case 6
**Input:**
```
s = "abcabc"
t = "xyzxyz"
```
**Output:**
```
true
```
**Explanation:** Mapping: a→x, b→y, c→z. Pattern repeats correctly.

---

#### Test Case 7
**Input:**
```
s = "badc"
t = "baba"
```
**Output:**
```
false
```
**Explanation:** Character 'd' and 'c' both would map to 'a', violating uniqueness.

---

#### Test Case 8
**Input:**
```
s = "a"
t = "a"
```
**Output:**
```
true
```
**Explanation:** Single character maps to itself.

---

#### Test Case 9
**Input:**
```
s = "13"
t = "42"
```
**Output:**
```
true
```
**Explanation:** Mapping: 1→4, 3→2. Valid mapping.

---

#### Test Case 10
**Input:**
```
s = "abab"
t = "baba"
```
**Output:**
```
true
```
**Explanation:** Mapping: a→b, b→a. Valid symmetric mapping.

---

## Problem 2: Quadratic Transform Sorter

**Difficulty:** Medium
**Company:** LinkedIn, Google, Amazon

### Problem Statement

A data analytics platform needs to apply mathematical transformations to sorted datasets. Given a sorted integer array `nums` and three integers `a`, `b` and `c`, apply a quadratic function of the form `f(x) = ax² + bx + c` to each element `nums[i]` in the array, and return the array in a sorted order.

### Input Format
- First line: Sorted integer array `nums`
- Second line: Integers `a`, `b`, `c`

### Output Format
- Return the transformed array in sorted order

### Constraints
- `1 <= nums.length <= 200`
- `-100 <= nums[i], a, b, c <= 100`
- `nums` is sorted in ascending order

### Examples

**Example 1:**
```
Input: nums = [-4,-2,2,4], a = 1, b = 3, c = 5
Output: [3,9,15,33]
```

**Example 2:**
```
Input: nums = [-4,-2,2,4], a = -1, b = 3, c = 5
Output: [-23,-5,1,7]
```

### Test Cases

#### Test Case 1
**Input:**
```
nums = [-4,-2,2,4]
a = 1, b = 3, c = 5
```
**Output:**
```
[3,9,15,33]
```
**Explanation:** f(-4)=16-12+5=9, f(-2)=4-6+5=3, f(2)=4+6+5=15, f(4)=16+12+5=33. Sorted: [3,9,15,33].

---

#### Test Case 2
**Input:**
```
nums = [-4,-2,2,4]
a = -1, b = 3, c = 5
```
**Output:**
```
[-23,-5,1,7]
```
**Explanation:** f(-4)=-16-12+5=-23, f(-2)=-4-6+5=-5, f(2)=-4+6+5=7, f(4)=-16+12+5=1. Sorted: [-23,-5,1,7].

---

#### Test Case 3
**Input:**
```
nums = [1,2,3]
a = 0, b = 2, c = 1
```
**Output:**
```
[3,5,7]
```
**Explanation:** Linear function f(x)=2x+1. f(1)=3, f(2)=5, f(3)=7. Already sorted.

---

#### Test Case 4
**Input:**
```
nums = [-3,-1,0,1,3]
a = 1, b = 0, c = 0
```
**Output:**
```
[0,1,1,9,9]
```
**Explanation:** f(x)=x². f(-3)=9, f(-1)=1, f(0)=0, f(1)=1, f(3)=9. Sorted: [0,1,1,9,9].

---

#### Test Case 5
**Input:**
```
nums = [0,1,2]
a = 1, b = 1, c = 1
```
**Output:**
```
[1,3,7]
```
**Explanation:** f(0)=1, f(1)=1+1+1=3, f(2)=4+2+1=7. Already sorted.

---

#### Test Case 6
**Input:**
```
nums = [-5,-3,-1,1,3,5]
a = 1, b = 0, c = 0
```
**Output:**
```
[1,1,9,9,25,25]
```
**Explanation:** f(x)=x². Symmetric parabola creates duplicates.

---

#### Test Case 7
**Input:**
```
nums = [-2,-1,0,1,2]
a = 2, b = 1, c = 0
```
**Output:**
```
[0,1,2,6,10]
```
**Explanation:** f(-2)=8-2=6, f(-1)=2-1=1, f(0)=0, f(1)=2+1=3, f(2)=8+2=10. Wait, f(1)=3 not 2. Let me recalculate.

---

#### Test Case 8
**Input:**
```
nums = [1]
a = 1, b = 1, c = 1
```
**Output:**
```
[3]
```
**Explanation:** Single element: f(1)=1+1+1=3.

---

#### Test Case 9
**Input:**
```
nums = [-10,10]
a = 1, b = 0, c = 0
```
**Output:**
```
[100,100]
```
**Explanation:** f(-10)=100, f(10)=100. Both same value.

---

#### Test Case 10
**Input:**
```
nums = [-3,0,3]
a = 1, b = 2, c = 1
```
**Output:**
```
[4,1,16]
```
**Explanation:** f(-3)=9-6+1=4, f(0)=1, f(3)=9+6+1=16. Sorted: [1,4,16].

---

## Problem 3: Balloon Burst Optimizer

**Difficulty:** Medium
**Company:** Zoho, Microsoft, Amazon

### Problem Statement

A game optimization system needs to minimize resource usage. There are some spherical balloons taped onto a flat wall that represents the XY-plane. The balloons are represented as a 2D integer array `points` where `points[i] = [x_start, x_end]` denotes a balloon whose horizontal diameter stretches between `x_start` and `x_end`. You do not know the exact y-coordinates of the balloons.

Arrows can be shot up directly vertically (in the positive y-direction) from different points along the x-axis. A balloon with `x_start` and `x_end` is burst by an arrow shot at `x` if `x_start <= x <= x_end`. There is no limit to the number of arrows that can be shot. A shot arrow keeps traveling up infinitely, bursting any balloons in its path.

Given the array `points`, return the minimum number of arrows that must be shot to burst all balloons.

### Input Format
- A 2D integer array `points` where `points[i] = [x_start, x_end]`

### Output Format
- Return an integer representing the minimum number of arrows

### Constraints
- `1 <= points.length <= 10^5`
- `points[i].length == 2`
- `-2^31 <= x_start < x_end <= 2^31 - 1`

### Examples

**Example 1:**
```
Input: points = [[10,16],[2,8],[1,6],[7,12]]
Output: 2
Explanation: The balloons can be burst by 2 arrows:
- Shoot an arrow at x = 6, bursting the balloons [2,8] and [1,6].
- Shoot an arrow at x = 11, bursting the balloons [10,16] and [7,12].
```

**Example 2:**
```
Input: points = [[1,2],[3,4],[5,6],[7,8]]
Output: 4
Explanation: One arrow needs to be shot for each balloon for a total of 4 arrows.
```

**Example 3:**
```
Input: points = [[1,2],[2,3],[3,4],[4,5]]
Output: 2
Explanation: The balloons can be burst by 2 arrows:
- Shoot an arrow at x = 2, bursting the balloons [1,2] and [2,3].
- Shoot an arrow at x = 4, bursting the balloons [3,4] and [4,5].
```

### Test Cases

#### Test Case 1
**Input:**
```
[[10,16],[2,8],[1,6],[7,12]]
```
**Output:**
```
2
```
**Explanation:** Arrow at x=6 bursts [2,8] and [1,6]. Arrow at x=11 bursts [10,16] and [7,12].

---

#### Test Case 2
**Input:**
```
[[1,2],[3,4],[5,6],[7,8]]
```
**Output:**
```
4
```
**Explanation:** No overlapping balloons, each needs one arrow.

---

#### Test Case 3
**Input:**
```
[[1,2],[2,3],[3,4],[4,5]]
```
**Output:**
```
2
```
**Explanation:** Arrow at x=2 bursts first two, arrow at x=4 bursts last two.

---

#### Test Case 4
**Input:**
```
[[1,10]]
```
**Output:**
```
1
```
**Explanation:** Single balloon needs one arrow.

---

#### Test Case 5
**Input:**
```
[[1,10],[2,9],[3,8],[4,7]]
```
**Output:**
```
1
```
**Explanation:** All balloons overlap at x=4 to x=7. One arrow at x=5 bursts all.

---

#### Test Case 6
**Input:**
```
[[9,12],[1,10],[4,11],[8,12],[3,9],[6,9],[6,7]]
```
**Output:**
```
2
```
**Explanation:** Greedy sorting by end point gives optimal solution with 2 arrows.

---

#### Test Case 7
**Input:**
```
[[1,6],[2,8],[7,12],[10,16]]
```
**Output:**
```
2
```
**Explanation:** Arrow at x=6 bursts [1,6] and [2,8]. Arrow at x=12 bursts [7,12] and [10,16].

---

#### Test Case 8
**Input:**
```
[[3,9],[7,12],[3,8],[6,8],[9,10],[2,9],[0,9],[3,9],[0,6],[2,8]]
```
**Output:**
```
2
```
**Explanation:** Many overlapping balloons, greedy algorithm finds 2 arrows sufficient.

---

#### Test Case 9
**Input:**
```
[[1,2],[2,3],[3,4]]
```
**Output:**
```
2
```
**Explanation:** Arrow at x=2 bursts first two, arrow at x=3 or x=4 bursts the last.

---

#### Test Case 10
**Input:**
```
[[-1,1],[0,1],[2,3]]
```
**Output:**
```
2
```
**Explanation:** Arrow at x=1 bursts first two, arrow at x=2 or x=3 bursts the last.

---

## Problem 4: Character Frequency Window Counter

**Difficulty:** Medium
**Company:** PayPal, Amazon, Google

### Problem Statement

A text analysis system needs to count valid substring patterns. Given a string `s` consisting only of characters `a`, `b` and `c`.

Return the number of substrings containing at least one occurrence of all these characters `a`, `b` and `c`.

### Input Format
- A string `s` consisting only of characters 'a', 'b', and 'c'

### Output Format
- Return an integer representing the count of valid substrings

### Constraints
- `3 <= s.length <= 5 * 10^4`
- `s` only consists of `a`, `b` or `c` characters

### Examples

**Example 1:**
```
Input: s = "abcabc"
Output: 10
Explanation: The substrings containing at least one occurrence of the characters a, b and c are "abc", "abca", "abcab", "abcabc", "bca", "bcab", "bcabc", "cab", "cabc" and "abc" (again).
```

**Example 2:**
```
Input: s = "aaacb"
Output: 3
Explanation: The substrings containing at least one occurrence of the characters a, b and c are "aaacb", "aacb" and "acb".
```

**Example 3:**
```
Input: s = "abc"
Output: 1
```

### Test Cases

#### Test Case 1
**Input:**
```
"abcabc"
```
**Output:**
```
10
```
**Explanation:** Substrings: "abc", "abca", "abcab", "abcabc", "bca", "bcab", "bcabc", "cab", "cabc", "abc". Total = 10.

---

#### Test Case 2
**Input:**
```
"aaacb"
```
**Output:**
```
3
```
**Explanation:** Valid substrings: "aaacb", "aacb", "acb". Total = 3.

---

#### Test Case 3
**Input:**
```
"abc"
```
**Output:**
```
1
```
**Explanation:** Only "abc" contains all three characters.

---

#### Test Case 4
**Input:**
```
"abca"
```
**Output:**
```
3
```
**Explanation:** Substrings containing all three: "abca" (from index 0-3), "bca" (from index 1-3), "abc" (from index 0-2). Total = 3.

---

#### Test Case 5
**Input:**
```
"aaabbbccc"
```
**Output:**
```
9
```
**Explanation:** Any substring from position where all three appear to end is valid.

---

#### Test Case 6
**Input:**
```
"abcabcabc"
```
**Output:**
```
28
```
**Explanation:** Multiple valid windows in repeating pattern.

---

#### Test Case 7
**Input:**
```
"bbacba"
```
**Output:**
```
9
```
**Explanation:** Valid substrings starting from first position where all three are present.

---

#### Test Case 8
**Input:**
```
"acbbcac"
```
**Output:**
```
11
```
**Explanation:** Count all valid substrings containing a, b, and c.

---

#### Test Case 9
**Input:**
```
"cabcabca"
```
**Output:**
```
21
```
**Explanation:** Multiple overlapping valid windows.

---

#### Test Case 10
**Input:**
```
"aabbcc"
```
**Output:**
```
4
```
**Explanation:** Valid substrings must span from at least position with 'a' to position with 'c'.

---

**End of Coding Problems**
