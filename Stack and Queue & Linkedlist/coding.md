# Stack and Queue & Linkedlist - Coding Problems

---

## Problem 1: Symmetric Data Validator

**Difficulty:** Easy
**Company:** Oracle, Amazon, Facebook

### Problem Statement

A data validation system for a database platform needs to verify if stored sequences are symmetric. Given the `head` of a singly linked list, return `true` if it is a palindrome (reads the same forward and backward) or `false` otherwise.

A palindrome is a sequence that reads the same backward as forward.

### Input Format
- The head node of a singly linked list

### Output Format
- Return `true` if the linked list is a palindrome, `false` otherwise

### Constraints
- The number of nodes in the list is in the range `[1, 10^5]`
- `0 <= Node.val <= 9`

### Examples

**Example 1:**
```
Input: head = [1,2,2,1]
Output: true
```

**Example 2:**
```
Input: head = [1,2]
Output: false
```

### Test Cases

#### Test Case 1
**Input:**
```
[1,2,2,1]
```
**Output:**
```
true
```
**Explanation:** The list reads the same forward (1→2→2→1) and backward (1→2→2→1), so it's a palindrome.

---

#### Test Case 2
**Input:**
```
[1,2]
```
**Output:**
```
false
```
**Explanation:** Forward is 1→2, backward would be 2→1. They're different, so not a palindrome.

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
**Explanation:** A single node is always a palindrome.

---

#### Test Case 4
**Input:**
```
[1,2,3,2,1]
```
**Output:**
```
true
```
**Explanation:** The list is symmetric: 1→2→3→2→1 reads the same both ways.

---

#### Test Case 5
**Input:**
```
[1,2,3,4,5]
```
**Output:**
```
false
```
**Explanation:** Forward: 1→2→3→4→5, Backward: 5→4→3→2→1. Not the same.

---

#### Test Case 6
**Input:**
```
[1,1,1,1]
```
**Output:**
```
true
```
**Explanation:** All elements are the same, so it's a palindrome.

---

#### Test Case 7
**Input:**
```
[1,0,1]
```
**Output:**
```
true
```
**Explanation:** Symmetric sequence: 1→0→1.

---

#### Test Case 8
**Input:**
```
[9,9]
```
**Output:**
```
true
```
**Explanation:** Two identical elements form a palindrome.

---

#### Test Case 9
**Input:**
```
[1,2,3,3,2,1]
```
**Output:**
```
true
```
**Explanation:** Even-length palindrome with symmetric structure.

---

#### Test Case 10
**Input:**
```
[1,2,3,4]
```
**Output:**
```
false
```
**Explanation:** No symmetry: 1→2→3→4 ≠ 4→3→2→1.

---

## Problem 2: Lexicographic String Optimizer

**Difficulty:** Medium
**Company:** Paytm, Google, Amazon

### Problem Statement

A text processing system for a payment platform needs to optimize strings for display. Given a string `s`, remove duplicate letters so that every letter appears once and only once. You must make sure your result is the smallest in lexicographical order among all possible results.

### Input Format
- A string `s` consisting of lowercase English letters

### Output Format
- Return a string with duplicates removed in smallest lexicographical order

### Constraints
- `1 <= s.length <= 10^4`
- `s` consists of lowercase English letters

### Examples

**Example 1:**
```
Input: s = "bcabc"
Output: "abc"
```

**Example 2:**
```
Input: s = "cbacdcbc"
Output: "acdb"
```

### Test Cases

#### Test Case 1
**Input:**
```
"bcabc"
```
**Output:**
```
"abc"
```
**Explanation:** Remove duplicates to get "abc" which is lexicographically smallest.

---

#### Test Case 2
**Input:**
```
"cbacdcbc"
```
**Output:**
```
"acdb"
```
**Explanation:** The smallest lexicographical order while keeping all unique letters is "acdb".

---

#### Test Case 3
**Input:**
```
"a"
```
**Output:**
```
"a"
```
**Explanation:** Single character, no duplicates to remove.

---

#### Test Case 4
**Input:**
```
"abc"
```
**Output:**
```
"abc"
```
**Explanation:** No duplicates present, string remains the same.

---

#### Test Case 5
**Input:**
```
"aaa"
```
**Output:**
```
"a"
```
**Explanation:** All characters are the same, keep only one.

---

#### Test Case 6
**Input:**
```
"bcab"
```
**Output:**
```
"bca"
```
**Explanation:** Process: b→c→a (can't remove c as it comes before a and won't appear again)→b (duplicate, skip). Result: "bca".

---

#### Test Case 7
**Input:**
```
"ecbacba"
```
**Output:**
```
"eacb"
```
**Explanation:** The lexicographically smallest string with all unique characters is "eacb".

---

#### Test Case 8
**Input:**
```
"abacb"
```
**Output:**
```
"abc"
```
**Explanation:** Remove duplicates maintaining lexicographical order: "abc".

---

#### Test Case 9
**Input:**
```
"abcd"
```
**Output:**
```
"abcd"
```
**Explanation:** Already in lexicographical order with no duplicates.

---

#### Test Case 10
**Input:**
```
"bbcaac"
```
**Output:**
```
"bac"
```
**Explanation:** The smallest lexicographical result is "bac".

---

## Problem 3: Card Deck Organizer

**Difficulty:** Medium
**Company:** Bloomberg, Microsoft, Apple

### Problem Statement

A gaming platform needs to organize card reveals in a specific order. You are given an integer array `deck`. There is a deck of cards where every card has a unique integer. The integer on the i-th card is `deck[i]`.

You can order the deck in any order you want. Initially, all the cards start face down (unrevealed) in one deck.

You will do the following steps repeatedly until all cards are revealed:

1. Take the top card of the deck, reveal it, and take it out of the deck.
2. If there are still cards in the deck, then put the next top card of the deck at the bottom of the deck.
3. If there are still unrevealed cards, go back to step 1. Otherwise, stop.

Return an ordering of the deck that would reveal the cards in increasing order.

Note that the first entry in the answer is considered to be the top of the deck.

### Input Format
- An integer array `deck` where each element is unique

### Output Format
- Return an array representing the deck order that reveals cards in increasing order

### Constraints
- `1 <= deck.length <= 1000`
- `1 <= deck[i] <= 10^6`
- All the values of `deck` are unique

### Examples

**Example 1:**
```
Input: deck = [17,13,11,2,3,5,7]
Output: [2,13,3,11,5,17,7]
Explanation:
We get the deck in the order [2,13,3,11,5,17,7] (this order doesn't matter), and reorder it.
After reordering, the deck starts as [2,13,3,11,5,17,7], where 2 is the top of the deck.
We reveal 2, and move 13 to the bottom. The deck is now [3,11,5,17,7,13].
We reveal 3, and move 11 to the bottom. The deck is now [5,17,7,13,11].
We reveal 5, and move 17 to the bottom. The deck is now [7,13,11,17].
We reveal 7, and move 13 to the bottom. The deck is now [11,17,13].
We reveal 11, and move 17 to the bottom. The deck is now [13,17].
We reveal 13, and move 17 to the bottom. The deck is now [17].
We reveal 17.
Since all the cards revealed are in increasing order, the answer is correct.
```

**Example 2:**
```
Input: deck = [1,1000]
Output: [1,1000]
```

### Test Cases

#### Test Case 1
**Input:**
```
[17,13,11,2,3,5,7]
```
**Output:**
```
[2,13,3,11,5,17,7]
```
**Explanation:** Following the reveal process results in cards being revealed in order: 2,3,5,7,11,13,17.

---

#### Test Case 2
**Input:**
```
[1,1000]
```
**Output:**
```
[1,1000]
```
**Explanation:** Reveal 1, move 1000 to bottom (but it's the last card), reveal 1000.

---

#### Test Case 3
**Input:**
```
[1]
```
**Output:**
```
[1]
```
**Explanation:** Single card, no reordering needed.

---

#### Test Case 4
**Input:**
```
[1,2,3]
```
**Output:**
```
[1,3,2]
```
**Explanation:** Reveal 1, move 3 to bottom → [2,3], reveal 2, move 3 to bottom, reveal 3.

---

#### Test Case 5
**Input:**
```
[1,2,3,4]
```
**Output:**
```
[1,3,2,4]
```
**Explanation:** Process reveals in order 1,2,3,4.

---

#### Test Case 6
**Input:**
```
[1,2,3,4,5]
```
**Output:**
```
[1,5,2,4,3]
```
**Explanation:** Following the reveal process: reveal 1, move 5 to bottom, reveal 2, move 4 to bottom, reveal 3, move 5 to bottom (wait, let me recalculate). Actually the simulation reveals cards in increasing order with this arrangement.

---

#### Test Case 7
**Input:**
```
[5,4,3,2,1]
```
**Output:**
```
[1,5,2,4,3]
```
**Explanation:** Input is unsorted, but after sorting becomes [1,2,3,4,5], and the reveal arrangement is [1,5,2,4,3].

---

#### Test Case 8
**Input:**
```
[10,20]
```
**Output:**
```
[10,20]
```
**Explanation:** Two cards: reveal 10, move 20 to bottom, reveal 20.

---

#### Test Case 9
**Input:**
```
[2,4,6,8]
```
**Output:**
```
[2,6,4,8]
```
**Explanation:** Reveals in order: 2,4,6,8.

---

#### Test Case 10
**Input:**
```
[7,6,5,4,3,2,1]
```
**Output:**
```
[1,6,2,5,3,7,4]
```
**Explanation:** After sorting to [1,2,3,4,5,6,7], the reveal arrangement is [1,6,2,5,3,7,4] to achieve increasing reveal order.

---

## Problem 4: Linked List Block Reverser

**Difficulty:** Hard
**Company:** Adobe, Microsoft, Amazon

### Problem Statement

A data transformation system for a document processing platform needs to reverse sections of linked data. Given the `head` of a linked list, reverse the nodes of the list `k` at a time, and return the modified list.

`k` is a positive integer and is less than or equal to the length of the linked list. If the number of nodes is not a multiple of `k`, then left-out nodes, in the end, should remain as it is.

You may not alter the values in the list's nodes, only nodes themselves may be changed.

### Input Format
- First line: The head node of a linked list
- Second line: Integer `k` (group size for reversal)

### Output Format
- Return the head of the modified linked list

### Constraints
- The number of nodes in the list is `n`
- `1 <= k <= n <= 5000`
- `0 <= Node.val <= 1000`

### Examples

**Example 1:**
```
Input: head = [1,2,3,4,5], k = 2
Output: [2,1,4,3,5]
```

**Example 2:**
```
Input: head = [1,2,3,4,5], k = 3
Output: [3,2,1,4,5]
```

### Test Cases

#### Test Case 1
**Input:**
```
head = [1,2,3,4,5]
k = 2
```
**Output:**
```
[2,1,4,3,5]
```
**Explanation:** Reverse first 2 nodes (1,2 → 2,1), then next 2 nodes (3,4 → 4,3), leave 5 as is.

---

#### Test Case 2
**Input:**
```
head = [1,2,3,4,5]
k = 3
```
**Output:**
```
[3,2,1,4,5]
```
**Explanation:** Reverse first 3 nodes (1,2,3 → 3,2,1), remaining 2 nodes stay as is.

---

#### Test Case 3
**Input:**
```
head = [1,2,3,4,5]
k = 1
```
**Output:**
```
[1,2,3,4,5]
```
**Explanation:** Reversing groups of size 1 means no change.

---

#### Test Case 4
**Input:**
```
head = [1,2,3,4,5]
k = 5
```
**Output:**
```
[5,4,3,2,1]
```
**Explanation:** Reverse all 5 nodes.

---

#### Test Case 5
**Input:**
```
head = [1]
k = 1
```
**Output:**
```
[1]
```
**Explanation:** Single node, no change.

---

#### Test Case 6
**Input:**
```
head = [1,2]
k = 2
```
**Output:**
```
[2,1]
```
**Explanation:** Reverse the pair.

---

#### Test Case 7
**Input:**
```
head = [1,2,3,4,5,6,7,8]
k = 3
```
**Output:**
```
[3,2,1,6,5,4,7,8]
```
**Explanation:** Reverse first 3 (1,2,3 → 3,2,1), next 3 (4,5,6 → 6,5,4), leave remaining 2 as is.

---

#### Test Case 8
**Input:**
```
head = [1,2,3,4]
k = 2
```
**Output:**
```
[2,1,4,3]
```
**Explanation:** Perfect groups: (1,2 → 2,1), (3,4 → 4,3).

---

#### Test Case 9
**Input:**
```
head = [1,2,3,4,5,6]
k = 2
```
**Output:**
```
[2,1,4,3,6,5]
```
**Explanation:** Three groups of 2: each pair reversed.

---

#### Test Case 10
**Input:**
```
head = [1,2,3,4,5,6,7]
k = 4
```
**Output:**
```
[4,3,2,1,5,6,7]
```
**Explanation:** First 4 nodes reversed (1,2,3,4 → 4,3,2,1), remaining 3 stay as is.

---

**End of Coding Problems**
