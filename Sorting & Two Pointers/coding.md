# Sorting & Two Pointers - Coding Problems

---

## Problem 1: Dutch National Flag Problem

**Difficulty:** Medium
**Company:** Microsoft, Facebook, Amazon

### Problem Statement

A manufacturing company produces objects in three colors: red, white, and blue. Due to a system error, the objects on the production line are mixed up. You need to sort them in-place so that objects of the same color are adjacent, with the colors in the order red, white, and blue.

Given an array `nums` with `n` objects colored red, white, or blue, sort them in-place so that objects of the same color are adjacent, with the colors in the order red, white, and blue.

We will use the integers `0`, `1`, and `2` to represent the color red, white, and blue, respectively.

You must solve this problem without using the library's sort function.

### Input Format
- An array `nums` containing integers 0, 1, and 2

### Output Format
- The same array sorted in-place (no return value, modify the array directly)

### Constraints
- `n == nums.length`
- `1 <= n <= 300`
- `nums[i]` is either `0`, `1`, or `2`

### Examples

**Example 1:**
```
Input: [2,0,2,1,1,0]
Output: [0,0,1,1,2,2]
```

**Example 2:**
```
Input: [2,0,1]
Output: [0,1,2]
```

### Test Cases

#### Test Case 1
**Input:**
```
[2,0,2,1,1,0]
```
**Output:**
```
[0,0,1,1,2,2]
```
**Explanation:** All 0s come first, then 1s, then 2s.

---

#### Test Case 2
**Input:**
```
[2,0,1]
```
**Output:**
```
[0,1,2]
```
**Explanation:** Simple case with one of each color.

---

#### Test Case 3
**Input:**
```
[0]
```
**Output:**
```
[0]
```
**Explanation:** Single element array remains unchanged.

---

#### Test Case 4
**Input:**
```
[1]
```
**Output:**
```
[1]
```
**Explanation:** Single element array with value 1.

---

#### Test Case 5
**Input:**
```
[2,2,2,2]
```
**Output:**
```
[2,2,2,2]
```
**Explanation:** All elements are the same color (blue).

---

#### Test Case 6
**Input:**
```
[0,0,0,0]
```
**Output:**
```
[0,0,0,0]
```
**Explanation:** All elements are the same color (red).

---

#### Test Case 7
**Input:**
```
[1,1,1,1]
```
**Output:**
```
[1,1,1,1]
```
**Explanation:** All elements are the same color (white).

---

#### Test Case 8
**Input:**
```
[2,1,0]
```
**Output:**
```
[0,1,2]
```
**Explanation:** Reverse sorted input becomes properly sorted.

---

#### Test Case 9
**Input:**
```
[1,2,0,1,2,0,1,2]
```
**Output:**
```
[0,0,1,1,1,2,2,2]
```
**Explanation:** Mixed colors get grouped together.

---

#### Test Case 10
**Input:**
```
[2,0,2,1,1,0,2,0,1]
```
**Output:**
```
[0,0,0,1,1,1,2,2,2]
```
**Explanation:** Larger array with equal distribution of colors.

---

## Problem 2: Array Equalization Problem

**Difficulty:** Medium
**Company:** Google, Amazon, Microsoft

### Problem Statement

A game developer is balancing player statistics. Given an integer array `nums` of size `n`, you need to find the minimum number of moves required to make all array elements equal.

In one move, you can increment or decrement an element of the array by 1.

Test cases are designed so that the answer will fit in a 32-bit integer.

### Input Format
- An integer array `nums` of size `n`

### Output Format
- Return a single integer representing the minimum number of moves

### Constraints
- `n == nums.length`
- `1 <= nums.length <= 10^5`
- `-10^9 <= nums[i] <= 10^9`

### Examples

**Example 1:**
```
Input: [1,2,3]
Output: 2
Explanation: Only two moves are needed (remember each move increments or decrements one element):
[1,2,3] => [2,2,3] => [2,2,2]
```

**Example 2:**
```
Input: [1,10,2,9]
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
**Explanation:** Move to median value 2. Moves: |1-2| + |2-2| + |3-2| = 1 + 0 + 1 = 2.

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
**Explanation:** Move to median value 5.5, but we use integer 5 or 6. Using 5: |1-5| + |10-5| + |2-5| + |9-5| = 4 + 5 + 3 + 4 = 16.

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
**Explanation:** Sorted: [0,0,1,6,8]. Median is 1. Moves: |0-1| + |0-1| + |1-1| + |6-1| + |8-1| = 1 + 1 + 0 + 5 + 7 = 14.

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
**Explanation:** Single element array, already equal, 0 moves needed.

---

#### Test Case 5
**Input:**
```
[1,1,1,1]
```
**Output:**
```
0
```
**Explanation:** All elements already equal, 0 moves needed.

---

#### Test Case 6
**Input:**
```
[1,5]
```
**Output:**
```
4
```
**Explanation:** Median between 1 and 5 is 3. Moves: |1-3| + |5-3| = 2 + 2 = 4.

---

#### Test Case 7
**Input:**
```
[5,5,5,5,5]
```
**Output:**
```
0
```
**Explanation:** All elements identical, 0 moves needed.

---

#### Test Case 8
**Input:**
```
[1,100]
```
**Output:**
```
99
```
**Explanation:** Median is 50.5, use 50 or 51. Using 50: |1-50| + |100-50| = 49 + 50 = 99.

---

#### Test Case 9
**Input:**
```
[3,7,9]
```
**Output:**
```
6
```
**Explanation:** Median is 7. Moves: |3-7| + |7-7| + |9-7| = 4 + 0 + 2 = 6.

---

#### Test Case 10
**Input:**
```
[1,2,3,4,5,6,7,8,9,10]
```
**Output:**
```
25
```
**Explanation:** Median is between 5 and 6, use 5.5 but take 5 or 6. Using 5: sum of distances = 4+3+2+1+0+1+2+3+4+5 = 25. Using 6: sum = 5+4+3+2+1+0+1+2+3+4 = 25.

---

## Problem 3: In-Place Word Reversal

**Difficulty:** Medium
**Company:** Amazon, Microsoft, Apple

### Problem Statement

A text processing system needs to reverse the order of words in a character array. Given a character array `s`, reverse the order of the words.

A word is defined as a sequence of non-space characters. The words in `s` will be separated by a single space.

Your code must solve the problem in-place, i.e. without allocating extra space.

### Input Format
- A character array `s` where words are separated by single spaces

### Output Format
- The same array modified in-place with words in reverse order (no return value)

### Constraints
- `1 <= s.length <= 10^5`
- `s[i]` is an English letter (uppercase or lowercase), digit, or space `' '`
- There is at least one word in `s`
- `s` does not contain leading or trailing spaces
- All the words in `s` are guaranteed to be separated by a single space

### Examples

**Example 1:**
```
Input: ["t","h","e"," ","s","k","y"," ","i","s"," ","b","l","u","e"]
Output: ["b","l","u","e"," ","i","s"," ","s","k","y"," ","t","h","e"]
```

**Example 2:**
```
Input: ["a"]
Output: ["a"]
```

### Test Cases

#### Test Case 1
**Input:**
```
["t","h","e"," ","s","k","y"," ","i","s"," ","b","l","u","e"]
```
**Output:**
```
["b","l","u","e"," ","i","s"," ","s","k","y"," ","t","h","e"]
```
**Explanation:** The words are reversed: "the sky is blue" becomes "blue is sky the".

---

#### Test Case 2
**Input:**
```
["a"]
```
**Output:**
```
["a"]
```
**Explanation:** Single character, no change needed.

---

#### Test Case 3
**Input:**
```
["h","e","l","l","o"]
```
**Output:**
```
["h","e","l","l","o"]
```
**Explanation:** Single word, remains unchanged.

---

#### Test Case 4
**Input:**
```
["a"," ","b"]
```
**Output:**
```
["b"," ","a"]
```
**Explanation:** Two single-letter words are swapped.

---

#### Test Case 5
**Input:**
```
["h","e","l","l","o"," ","w","o","r","l","d"]
```
**Output:**
```
["w","o","r","l","d"," ","h","e","l","l","o"]
```
**Explanation:** "hello world" becomes "world hello".

---

#### Test Case 6
**Input:**
```
["a","b","c"," ","d","e","f"," ","g","h","i"]
```
**Output:**
```
["g","h","i"," ","d","e","f"," ","a","b","c"]
```
**Explanation:** Three words reversed.

---

#### Test Case 7
**Input:**
```
["1","2","3"," ","4","5","6"]
```
**Output:**
```
["4","5","6"," ","1","2","3"]
```
**Explanation:** Numeric characters work the same way.

---

#### Test Case 8
**Input:**
```
["o","n","e"," ","t","w","o"," ","t","h","r","e","e"," ","f","o","u","r"]
```
**Output:**
```
["f","o","u","r"," ","t","h","r","e","e"," ","t","w","o"," ","o","n","e"]
```
**Explanation:** Four words reversed.

---

#### Test Case 9
**Input:**
```
["a"," ","b"," ","c"," ","d"," ","e"]
```
**Output:**
```
["e"," ","d"," ","c"," ","b"," ","a"]
```
**Explanation:** Five single-letter words reversed.

---

#### Test Case 10
**Input:**
```
["g","o","o","d"," ","m","o","r","n","i","n","g"]
```
**Output:**
```
["m","o","r","n","i","n","g"," ","g","o","o","d"]
```
**Explanation:** "good morning" becomes "morning good".

---

## Problem 4: Optimal Heater Placement

**Difficulty:** Medium
**Company:** Google, Microsoft, Facebook

### Problem Statement

A smart home system needs to determine the optimal heater settings. During winter, you need to design a standard heater with a fixed warm radius to warm all the houses.

Every house can be warmed, as long as the house is within the heater's warm radius range.

Given the positions of `houses` and `heaters` on a horizontal line, return the minimum radius standard of heaters so that those heaters could cover all houses.

Notice that all the heaters follow your radius standard, and the warm radius will be the same.

### Input Format
- First line: Array `houses` containing positions of houses
- Second line: Array `heaters` containing positions of heaters

### Output Format
- Return a single integer representing the minimum radius

### Constraints
- `1 <= houses.length, heaters.length <= 3 * 10^4`
- `1 <= houses[i], heaters[i] <= 10^9`

### Examples

**Example 1:**
```
Input:
houses = [1,2,3]
heaters = [2]
Output: 1
Explanation: The only heater was placed in the position 2, and if we use the radius 1 standard, then all the houses can be warmed.
```

**Example 2:**
```
Input:
houses = [1,2,3,4]
heaters = [1,4]
Output: 1
Explanation: The two heaters were placed at positions 1 and 4. We need to use a radius 1 standard, then all the houses can be warmed.
```

**Example 3:**
```
Input:
houses = [1,5]
heaters = [2]
Output: 3
```

### Test Cases

#### Test Case 1
**Input:**
```
houses = [1,2,3]
heaters = [2]
```
**Output:**
```
1
```
**Explanation:** Heater at position 2 with radius 1 covers houses at 1, 2, and 3.

---

#### Test Case 2
**Input:**
```
houses = [1,2,3,4]
heaters = [1,4]
```
**Output:**
```
1
```
**Explanation:** Heaters at 1 and 4 with radius 1 cover all houses.

---

#### Test Case 3
**Input:**
```
houses = [1,5]
heaters = [2]
```
**Output:**
```
3
```
**Explanation:** Heater at 2 needs radius 3 to cover house at 5 (distance = 3).

---

#### Test Case 4
**Input:**
```
houses = [1]
heaters = [1]
```
**Output:**
```
0
```
**Explanation:** Heater is at the same position as the house, radius 0 needed.

---

#### Test Case 5
**Input:**
```
houses = [1,2,3,4,5]
heaters = [1,5]
```
**Output:**
```
2
```
**Explanation:** Heaters at 1 and 5 need radius 2 to cover house at 3 (middle house is farthest from any heater).

---

#### Test Case 6
**Input:**
```
houses = [1,1,1,1,1,1,999,999,999,999,999]
heaters = [499,500,501]
```
**Output:**
```
498
```
**Explanation:** Houses at 1 need radius 498 from nearest heater at 499.

---

#### Test Case 7
**Input:**
```
houses = [1,2,3]
heaters = [1,2,3]
```
**Output:**
```
0
```
**Explanation:** Each house has a heater at its exact position.

---

#### Test Case 8
**Input:**
```
houses = [10,20,30,40]
heaters = [15,35]
```
**Output:**
```
5
```
**Explanation:** Heater at 15 covers 10 and 20, heater at 35 covers 30 and 40. Distances: |10-15|=5, |20-15|=5, |30-35|=5, |40-35|=5. Maximum distance is 5.

---

#### Test Case 9
**Input:**
```
houses = [1,100]
heaters = [50]
```
**Output:**
```
50
```
**Explanation:** Heater at 50 needs to cover both houses. Distances: |1-50|=49, |100-50|=50. Maximum distance is 50.

---

#### Test Case 10
**Input:**
```
houses = [5,10,15,20,25]
heaters = [10,20]
```
**Output:**
```
5
```
**Explanation:** Houses at positions 5,10,15,20,25 with heaters at 10,20. Distances: |5-10|=5, |10-10|=0, |15-10|=5 or |15-20|=5, |20-20|=0, |25-20|=5. Maximum distance is 5.

---

**End of Coding Problems**
