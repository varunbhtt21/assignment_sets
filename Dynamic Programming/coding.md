# Dynamic Programming - Coding Problems

---

## Problem 1: Minimum Jump Navigator

**Difficulty:** Medium
**Company:** Amazon, Google, Microsoft

### Problem Statement

A navigation system for a delivery platform needs to optimize route planning. You are given a 0-indexed array of integers `nums` of length `n`. You are initially positioned at index 0.

Each element `nums[i]` represents the maximum length of a forward jump from index `i`. In other words, if you are at index `i`, you can jump to any index `(i + j)` where:
- `0 <= j <= nums[i]` and
- `i + j < n`

Return the minimum number of jumps to reach index `n - 1`. The test cases are generated such that you can reach index `n - 1`.

### Input Format
- An integer array `nums` of length `n`

### Output Format
- Return an integer representing the minimum number of jumps needed

### Constraints
- `1 <= nums.length <= 10^4`
- `0 <= nums[i] <= 1000`
- It's guaranteed that you can reach `nums[n - 1]`

### Examples

**Example 1:**
```
Input: nums = [2,3,1,1,4]
Output: 2
Explanation: The minimum number of jumps to reach the last index is 2. Jump 1 step from index 0 to 1, then 3 steps to the last index.
```

**Example 2:**
```
Input: nums = [2,3,0,1,4]
Output: 2
```

### Test Cases

#### Test Case 1
**Input:**
```
[2,3,1,1,4]
```
**Output:**
```
2
```
**Explanation:** Jump 1 step from index 0 to index 1, then jump 3 steps to reach the last index (index 4).

---

#### Test Case 2
**Input:**
```
[2,3,0,1,4]
```
**Output:**
```
2
```
**Explanation:** Jump 1 step from index 0 to index 1, then jump 3 steps to reach index 4.

---

#### Test Case 3
**Input:**
```
[1,2,3]
```
**Output:**
```
2
```
**Explanation:** Jump from index 0 to 1, then from 1 to 3 (2 jumps total).

---

#### Test Case 4
**Input:**
```
[1,1,1,1]
```
**Output:**
```
3
```
**Explanation:** Must jump 1 step at a time: 0→1→2→3 (3 jumps).

---

#### Test Case 5
**Input:**
```
[5,6,4,4,6,9,4,4,7,4,4,8,2,6,8,1,5,9,6,5,2,7,9,7,9,6,9,4,1,6,8,8,4,4,2,0,3,8,5]
```
**Output:**
```
5
```
**Explanation:** Optimal path with 5 jumps reaches the end.

---

#### Test Case 6
**Input:**
```
[1]
```
**Output:**
```
0
```
**Explanation:** Already at the last index, no jumps needed.

---

#### Test Case 7
**Input:**
```
[10,9,8,7,6,5,4,3,2,1,1,0]
```
**Output:**
```
2
```
**Explanation:** Jump from index 0 (value 10) can reach index 10, then one more jump to index 11.

---

#### Test Case 8
**Input:**
```
[1,2,1,1,1]
```
**Output:**
```
3
```
**Explanation:** Path: 0→1→3→4 (3 jumps).

---

#### Test Case 9
**Input:**
```
[3,2,1,0,4]
```
**Output:**
```
2
```
**Explanation:** From index 0, jump to index 1 or 2, then to index 4.

---

#### Test Case 10
**Input:**
```
[2,1,1,1,1]
```
**Output:**
```
3
```
**Explanation:** Jump from 0 to 1, then 1→2→3→4 requires 3 more steps, total 4. Actually, 0→2→3→4 is 3 jumps.

---

## Problem 2: Text Palindrome Partitioner

**Difficulty:** Medium
**Company:** Amazon, Google, Apple

### Problem Statement

A text processing system for a content management platform needs to split strings into palindromic substrings. Given a string `s`, partition `s` such that every substring of the partition is a palindrome.

Return all possible palindrome partitioning of `s`.

A palindrome is a string that reads the same backward as forward.

### Input Format
- A string `s` containing only lowercase English letters

### Output Format
- Return a list of lists, where each inner list represents one valid palindrome partitioning

### Constraints
- `1 <= s.length <= 16`
- `s` contains only lowercase English letters

### Examples

**Example 1:**
```
Input: s = "aab"
Output: [["a","a","b"],["aa","b"]]
```

**Example 2:**
```
Input: s = "a"
Output: [["a"]]
```

### Test Cases

#### Test Case 1
**Input:**
```
"aab"
```
**Output:**
```
[["a","a","b"],["aa","b"]]
```
**Explanation:** "aab" can be split as ["a","a","b"] where all parts are palindromes, or ["aa","b"] where "aa" and "b" are palindromes.

---

#### Test Case 2
**Input:**
```
"a"
```
**Output:**
```
[["a"]]
```
**Explanation:** Single character is always a palindrome.

---

#### Test Case 3
**Input:**
```
"aa"
```
**Output:**
```
[["a","a"],["aa"]]
```
**Explanation:** Can split as two single characters or keep as one palindrome "aa".

---

#### Test Case 4
**Input:**
```
"aba"
```
**Output:**
```
[["a","b","a"],["aba"]]
```
**Explanation:** Can split into three single characters or keep entire string "aba" as it's a palindrome.

---

#### Test Case 5
**Input:**
```
"abc"
```
**Output:**
```
[["a","b","c"]]
```
**Explanation:** No substrings of length > 1 are palindromes, so only one way to partition.

---

#### Test Case 6
**Input:**
```
"abba"
```
**Output:**
```
[["a","b","b","a"],["a","bb","a"],["abba"]]
```
**Explanation:** Multiple ways: all singles, "bb" in middle, or entire string.

---

#### Test Case 7
**Input:**
```
"racecar"
```
**Output:**
```
[["r","a","c","e","c","a","r"],["r","a","cec","a","r"],["r","aceca","r"],["racecar"]]
```
**Explanation:** Multiple palindromic partitions possible including the entire string.

---

#### Test Case 8
**Input:**
```
"ab"
```
**Output:**
```
[["a","b"]]
```
**Explanation:** "ab" is not a palindrome, so must split into individual characters.

---

#### Test Case 9
**Input:**
```
"aaa"
```
**Output:**
```
[["a","a","a"],["a","aa"],["aa","a"],["aaa"]]
```
**Explanation:** All possible partitions where each part is a palindrome.

---

#### Test Case 10
**Input:**
```
"abcba"
```
**Output:**
```
[["a","b","c","b","a"],["a","bcb","a"],["abcba"]]
```
**Explanation:** Can split into singles, "bcb" in middle, or entire palindrome "abcba".

---

## Problem 3: Grid Distance Calculator

**Difficulty:** Medium
**Company:** Microsoft, Google, Facebook

### Problem Statement

A warehouse management system needs to calculate distances from storage locations. Given an `m x n` binary matrix `mat`, return the distance of the nearest 0 for each cell.

The distance between two adjacent cells sharing a common edge is 1.

### Input Format
- A 2D binary matrix `mat` where `mat[i][j]` is either 0 or 1

### Output Format
- Return a 2D matrix of the same dimensions where each cell contains the distance to the nearest 0

### Constraints
- `m == mat.length`
- `n == mat[i].length`
- `1 <= m, n <= 10^4`
- `1 <= m * n <= 10^4`
- `mat[i][j]` is either 0 or 1
- There is at least one 0 in `mat`

### Examples

**Example 1:**
```
Input: mat = [[0,0,0],[0,1,0],[0,0,0]]
Output: [[0,0,0],[0,1,0],[0,0,0]]
```

**Example 2:**
```
Input: mat = [[0,0,0],[0,1,0],[1,1,1]]
Output: [[0,0,0],[0,1,0],[1,2,1]]
```

### Test Cases

#### Test Case 1
**Input:**
```
[[0,0,0],[0,1,0],[0,0,0]]
```
**Output:**
```
[[0,0,0],[0,1,0],[0,0,0]]
```
**Explanation:** The cell (1,1) with value 1 is surrounded by 0s at distance 1.

---

#### Test Case 2
**Input:**
```
[[0,0,0],[0,1,0],[1,1,1]]
```
**Output:**
```
[[0,0,0],[0,1,0],[1,2,1]]
```
**Explanation:** Cell (2,1) is distance 2 from nearest 0. Cells (2,0) and (2,2) are distance 1.

---

#### Test Case 3
**Input:**
```
[[0]]
```
**Output:**
```
[[0]]
```
**Explanation:** Single cell with value 0 has distance 0 to itself.

---

#### Test Case 4
**Input:**
```
[[1]]
```
**Output:**
```
[[0]]
```
**Explanation:** Wait, this violates the constraint "at least one 0 in mat". Let me fix this.

---

#### Test Case 4 (Fixed)
**Input:**
```
[[0,1]]
```
**Output:**
```
[[0,1]]
```
**Explanation:** Cell with 0 has distance 0, adjacent cell with 1 has distance 1.

---

#### Test Case 5
**Input:**
```
[[0,1,0]]
```
**Output:**
```
[[0,1,0]]
```
**Explanation:** Middle cell is distance 1 from both adjacent 0s.

---

#### Test Case 6
**Input:**
```
[[1,1,1],[1,1,1],[1,1,0]]
```
**Output:**
```
[[4,3,2],[3,2,1],[2,1,0]]
```
**Explanation:** Only one 0 at position (2,2). All distances calculated from this cell.

---

#### Test Case 7
**Input:**
```
[[0,1,1,1],[1,1,1,1],[1,1,1,1],[1,1,1,0]]
```
**Output:**
```
[[0,1,2,3],[1,2,3,2],[2,3,2,1],[3,2,1,0]]
```
**Explanation:** Two 0s at corners (0,0) and (3,3). Each cell gets distance to nearest 0.

---

#### Test Case 8
**Input:**
```
[[0,0],[0,0]]
```
**Output:**
```
[[0,0],[0,0]]
```
**Explanation:** All cells are 0, so all distances are 0.

---

#### Test Case 9
**Input:**
```
[[1,0,1],[1,1,1],[1,0,1]]
```
**Output:**
```
[[1,0,1],[2,1,2],[1,0,1]]
```
**Explanation:** Cells at (0,1) and (2,1) are 0. Corner cells are distance 1, center cells in first and last row are distance 1, but center cell (1,1) is distance 2 (must go through adjacent cells to reach a 0).

---

#### Test Case 10
**Input:**
```
[[0,1,1],[1,1,1],[1,1,1]]
```
**Output:**
```
[[0,1,2],[1,2,3],[2,3,4]]
```
**Explanation:** Single 0 at top-left corner. Distances increase as we move away.

---

## Problem 4: Playlist Configuration Counter

**Difficulty:** Hard
**Company:** Spotify, Amazon, Google

### Problem Statement

A music streaming platform needs to calculate possible playlist configurations. Your music player contains `n` different songs. You want to listen to `goal` songs (not necessarily different) during your trip. To avoid boredom, you will create a playlist so that:

- Every song is played at least once.
- A song can only be played again only if `k` other songs have been played.

Given `n`, `goal`, and `k`, return the number of possible playlists that you can create. Since the answer can be very large, return it modulo `10^9 + 7`.

### Input Format
- Three integers: `n` (number of different songs), `goal` (total songs to play), and `k` (gap between replays)

### Output Format
- Return an integer representing the number of possible playlists modulo `10^9 + 7`

### Constraints
- `0 <= k < n <= goal <= 100`

### Examples

**Example 1:**
```
Input: n = 3, goal = 3, k = 1
Output: 6
Explanation: There are 6 possible playlists: [1,2,3], [1,3,2], [2,1,3], [2,3,1], [3,1,2], and [3,2,1].
```

**Example 2:**
```
Input: n = 2, goal = 3, k = 0
Output: 6
Explanation: There are 6 possible playlists: [1,1,2], [1,2,1], [2,1,1], [2,2,1], [2,1,2], and [1,2,2].
```

**Example 3:**
```
Input: n = 2, goal = 3, k = 1
Output: 2
Explanation: There are 2 possible playlists: [1,2,1] and [2,1,2].
```

### Test Cases

#### Test Case 1
**Input:**
```
n = 3, goal = 3, k = 1
```
**Output:**
```
6
```
**Explanation:** All 6 permutations of 3 songs are valid since we play each exactly once.

---

#### Test Case 2
**Input:**
```
n = 2, goal = 3, k = 0
```
**Output:**
```
6
```
**Explanation:** With k=0, songs can be replayed immediately. Possible: [1,1,2], [1,2,1], [2,1,1], [2,2,1], [2,1,2], [1,2,2].

---

#### Test Case 3
**Input:**
```
n = 2, goal = 3, k = 1
```
**Output:**
```
2
```
**Explanation:** With k=1, need 1 other song between replays. Only [1,2,1] and [2,1,2] are valid.

---

#### Test Case 4
**Input:**
```
n = 1, goal = 1, k = 0
```
**Output:**
```
1
```
**Explanation:** Only one song played once: [1].

---

#### Test Case 5
**Input:**
```
n = 3, goal = 4, k = 0
```
**Output:**
```
36
```
**Explanation:** All songs must be played at least once in 4 slots. With k=0, many configurations possible.

---

#### Test Case 6
**Input:**
```
n = 3, goal = 4, k = 1
```
**Output:**
```
18
```
**Explanation:** Similar to previous but with k=1 constraint, fewer valid playlists.

---

#### Test Case 7
**Input:**
```
n = 3, goal = 4, k = 2
```
**Output:**
```
6
```
**Explanation:** With k=2, after playing a song, need 2 other songs before replaying it.

---

#### Test Case 8
**Input:**
```
n = 4, goal = 4, k = 0
```
**Output:**
```
24
```
**Explanation:** All 24 permutations of 4 songs (4! = 24).

---

#### Test Case 9
**Input:**
```
n = 4, goal = 4, k = 3
```
**Output:**
```
24
```
**Explanation:** With n=4, goal=4, k=3, each song played exactly once, so 4! = 24 ways.

---

#### Test Case 10
**Input:**
```
n = 3, goal = 5, k = 1
```
**Output:**
```
42
```
**Explanation:** With 3 songs in 5 slots and k=1 constraint (need 1 other song between replays), there are 42 valid playlist configurations.

---

**End of Coding Problems**
