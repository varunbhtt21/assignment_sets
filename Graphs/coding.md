# Graphs - Coding Problems

---

## Problem 1: Security Access Validator

**Difficulty:** Medium
**Company:** Microsoft, Amazon, Facebook

### Problem Statement

A corporate security system manages building access through connected rooms. There are `n` rooms labeled from `0` to `n - 1` and all the rooms are locked except for room `0`. Your goal is to visit all the rooms. However, you cannot enter a locked room without having its key.

When you visit a room, you may find a set of distinct keys in it. Each key has a number on it, denoting which room it unlocks, and you can take all of them with you to unlock the other rooms.

Given an array `rooms` where `rooms[i]` is the set of keys that you can obtain if you visited room `i`, return `true` if you can visit all the rooms, or `false` otherwise.

### Input Format
- An array of arrays `rooms` where `rooms[i]` contains the keys found in room `i`

### Output Format
- Return `true` if all rooms can be visited, `false` otherwise

### Constraints
- `2 <= n <= 1000`
- `0 <= rooms[i].length <= 1000`
- `1 <= sum(rooms[i].length) <= 3000`
- `0 <= rooms[i][j] < n`
- All the values of `rooms[i]` are unique

### Examples

**Example 1:**
```
Input: rooms = [[1],[2],[3],[]]
Output: true
Explanation:
We visit room 0 and pick up key 1.
We then visit room 1 and pick up key 2.
We then visit room 2 and pick up key 3.
We then visit room 3.
Since we were able to visit every room, we return true.
```

**Example 2:**
```
Input: rooms = [[1,3],[3,0,1],[2],[0]]
Output: false
Explanation: We can not enter room number 2 since the only key that unlocks it is in that room.
```

### Test Cases

#### Test Case 1
**Input:**
```
[[1],[2],[3],[]]
```
**Output:**
```
true
```
**Explanation:** Starting from room 0, we get key 1 → visit room 1, get key 2 → visit room 2, get key 3 → visit room 3. All rooms visited.

---

#### Test Case 2
**Input:**
```
[[1,3],[3,0,1],[2],[0]]
```
**Output:**
```
false
```
**Explanation:** We can visit rooms 0, 1, and 3, but room 2 can only be unlocked from inside room 2 itself.

---

#### Test Case 3
**Input:**
```
[[1],[],[0]]
```
**Output:**
```
false
```
**Explanation:** From room 0, we can only access room 1. Room 2 is unreachable.

---

#### Test Case 4
**Input:**
```
[[1,2],[3],[],[]]
```
**Output:**
```
true
```
**Explanation:** Room 0 has keys to rooms 1 and 2. Room 1 has key to room 3. All rooms can be visited.

---

#### Test Case 5
**Input:**
```
[[1],[2,3],[],[]]
```
**Output:**
```
true
```
**Explanation:** Room 0 → room 1 → rooms 2 and 3. All accessible.

---

#### Test Case 6
**Input:**
```
[[1,2,3],[],[],[]]
```
**Output:**
```
true
```
**Explanation:** Room 0 directly has keys to all other rooms.

---

#### Test Case 7
**Input:**
```
[[1],[0]]
```
**Output:**
```
true
```
**Explanation:** Two rooms, both accessible (0 is unlocked, 1 has key in room 0).

---

#### Test Case 8
**Input:**
```
[[],[1]]
```
**Output:**
```
false
```
**Explanation:** Room 0 has no keys, so room 1 cannot be accessed.

---

#### Test Case 9
**Input:**
```
[[1,2],[3,4],[5],[],[],[]]
```
**Output:**
```
true
```
**Explanation:** Following the chain: 0 → 1,2 → 3,4,5. All rooms reachable.

---

#### Test Case 10
**Input:**
```
[[1,2,3,4],[5],[5],[5],[5],[]]
```
**Output:**
```
true
```
**Explanation:** Room 0 unlocks rooms 1-4, each of which has key to room 5. All rooms visited.

---

## Problem 2: Authority Identifier

**Difficulty:** Easy
**Company:** Bloomberg, Amazon, Google

### Problem Statement

A community voting system needs to identify a special authority figure. In a town, there are `n` people labeled from `1` to `n`. There is a rumor that one of these people is secretly the town judge.

If the town judge exists, then:
1. The town judge trusts nobody.
2. Everybody (except for the town judge) trusts the town judge.
3. There is exactly one person that satisfies properties 1 and 2.

You are given an array `trust` where `trust[i] = [a_i, b_i]` representing that the person labeled `a_i` trusts the person labeled `b_i`. If a trust relationship does not exist in `trust` array, then such a trust relationship does not exist.

Return the label of the town judge if the town judge exists and can be identified, or return `-1` otherwise.

### Input Format
- First line: Integer `n` (number of people)
- Second line: 2D array `trust` where `trust[i] = [a, b]`

### Output Format
- Return the label of the town judge, or `-1` if no such person exists

### Constraints
- `1 <= n <= 1000`
- `0 <= trust.length <= 10^4`
- `trust[i].length == 2`
- All the pairs of `trust` are unique
- `a_i != b_i`
- `1 <= a_i, b_i <= n`

### Examples

**Example 1:**
```
Input: n = 2, trust = [[1,2]]
Output: 2
```

**Example 2:**
```
Input: n = 3, trust = [[1,3],[2,3]]
Output: 3
```

**Example 3:**
```
Input: n = 3, trust = [[1,3],[2,3],[3,1]]
Output: -1
```

### Test Cases

#### Test Case 1
**Input:**
```
n = 2
trust = [[1,2]]
```
**Output:**
```
2
```
**Explanation:** Person 1 trusts person 2. Person 2 trusts nobody. Person 2 is the judge.

---

#### Test Case 2
**Input:**
```
n = 3
trust = [[1,3],[2,3]]
```
**Output:**
```
3
```
**Explanation:** Persons 1 and 2 trust person 3. Person 3 trusts nobody. Person 3 is the judge.

---

#### Test Case 3
**Input:**
```
n = 3
trust = [[1,3],[2,3],[3,1]]
```
**Output:**
```
-1
```
**Explanation:** Person 3 trusts person 1, so person 3 cannot be the judge.

---

#### Test Case 4
**Input:**
```
n = 1
trust = []
```
**Output:**
```
1
```
**Explanation:** Single person who trusts nobody and is trusted by nobody (vacuously true) is the judge.

---

#### Test Case 5
**Input:**
```
n = 4
trust = [[1,3],[1,4],[2,3],[2,4],[4,3]]
```
**Output:**
```
3
```
**Explanation:** Person 3 is trusted by 1, 2, and 4. Person 3 trusts nobody. Person 3 is the judge.

---

#### Test Case 6
**Input:**
```
n = 4
trust = [[1,3],[2,3],[3,4]]
```
**Output:**
```
-1
```
**Explanation:** Person 4 is only trusted by person 3, not by all others. No judge exists.

---

#### Test Case 7
**Input:**
```
n = 2
trust = [[1,2],[2,1]]
```
**Output:**
```
-1
```
**Explanation:** Both people trust each other. Neither can be the judge.

---

#### Test Case 8
**Input:**
```
n = 5
trust = [[1,5],[2,5],[3,5],[4,5]]
```
**Output:**
```
5
```
**Explanation:** Everyone trusts person 5, and person 5 trusts nobody. Person 5 is the judge.

---

#### Test Case 9
**Input:**
```
n = 3
trust = [[1,2],[2,3]]
```
**Output:**
```
-1
```
**Explanation:** Person 3 is not trusted by person 1. No judge exists.

---

#### Test Case 10
**Input:**
```
n = 4
trust = [[1,2],[3,2],[4,2],[2,1]]
```
**Output:**
```
-1
```
**Explanation:** Person 2 trusts person 1, so person 2 cannot be the judge.

---

## Problem 3: Network Broadcast Origins

**Difficulty:** Medium
**Company:** Airbnb, Google, Amazon

### Problem Statement

A network broadcasting system uses a directed graph structure. Given a directed acyclic graph, with `n` vertices numbered from `0` to `n-1`, and an array `edges` where `edges[i] = [from_i, to_i]` represents a directed edge from node `from_i` to node `to_i`.

Find the smallest set of vertices from which all nodes in the graph are reachable. It's guaranteed that a unique solution exists.

Notice that you can return the vertices in any order.

### Input Format
- First line: Integer `n` (number of vertices)
- Second line: 2D array `edges` where `edges[i] = [from, to]`

### Output Format
- Return a list of vertices representing the minimum set of starting points

### Constraints
- `2 <= n <= 10^5`
- `1 <= edges.length <= min(10^5, n * (n - 1) / 2)`
- `edges[i].length == 2`
- `0 <= from_i, to_i < n`
- All pairs `(from_i, to_i)` are distinct

### Examples

**Example 1:**
```
Input: n = 6, edges = [[0,1],[0,2],[2,5],[3,4],[4,2]]
Output: [0,3]
Explanation: It's not possible to reach all the nodes from a single vertex. From 0 we can reach [0,1,2,5]. From 3 we can reach [3,4,2,5]. So we output [0,3].
```

**Example 2:**
```
Input: n = 5, edges = [[0,1],[2,1],[3,1],[1,4],[2,4]]
Output: [0,2,3]
Explanation: Notice that vertices 0, 3 and 2 are not reachable from any other node, so we must include them. Also any of these vertices can reach nodes 1 and 4.
```

### Test Cases

#### Test Case 1
**Input:**
```
n = 6
edges = [[0,1],[0,2],[2,5],[3,4],[4,2]]
```
**Output:**
```
[0,3]
```
**Explanation:** From 0 we reach [0,1,2,5]. From 3 we reach [3,4,2,5]. Together all nodes are covered.

---

#### Test Case 2
**Input:**
```
n = 5
edges = [[0,1],[2,1],[3,1],[1,4],[2,4]]
```
**Output:**
```
[0,2,3]
```
**Explanation:** Nodes 0, 2, 3 have no incoming edges, so they must be starting points.

---

#### Test Case 3
**Input:**
```
n = 3
edges = [[1,0],[2,0]]
```
**Output:**
```
[1,2]
```
**Explanation:** Nodes 1 and 2 have no incoming edges. Node 0 is reachable from both.

---

#### Test Case 4
**Input:**
```
n = 4
edges = [[0,1],[1,2],[2,3]]
```
**Output:**
```
[0]
```
**Explanation:** Node 0 has no incoming edge. All other nodes are reachable from node 0.

---

#### Test Case 5
**Input:**
```
n = 2
edges = [[1,0]]
```
**Output:**
```
[1]
```
**Explanation:** Node 1 is the only node with no incoming edge.

---

#### Test Case 6
**Input:**
```
n = 5
edges = [[0,2],[1,2],[2,3],[2,4]]
```
**Output:**
```
[0,1]
```
**Explanation:** Nodes 0 and 1 have no incoming edges. From them, all other nodes are reachable.

---

#### Test Case 7
**Input:**
```
n = 4
edges = [[0,1],[0,2],[0,3]]
```
**Output:**
```
[0]
```
**Explanation:** Node 0 is the only source; all others are reachable from it.

---

#### Test Case 8
**Input:**
```
n = 6
edges = [[0,3],[1,3],[2,3],[3,4],[4,5]]
```
**Output:**
```
[0,1,2]
```
**Explanation:** Nodes 0, 1, 2 have no incoming edges and are required starting points.

---

#### Test Case 9
**Input:**
```
n = 3
edges = [[0,1],[0,2]]
```
**Output:**
```
[0]
```
**Explanation:** Only node 0 has no incoming edge; nodes 1 and 2 are reachable from it.

---

#### Test Case 10
**Input:**
```
n = 7
edges = [[0,2],[1,2],[2,3],[3,4],[5,6]]
```
**Output:**
```
[0,1,5]
```
**Explanation:** Nodes 0, 1, and 5 have no incoming edges. They form the minimum set of starting vertices.

---

## Problem 4: Optimal Meeting Point Finder

**Difficulty:** Medium
**Company:** Juspay, Microsoft, Google

### Problem Statement

A logistics network planning system uses directed graphs to optimize delivery routes. You are given a directed graph of `n` nodes numbered from `0` to `n - 1`, where each node has at most one outgoing edge.

The graph is represented with a given 0-indexed array `edges` of size `n`, indicating that there is a directed edge from node `i` to node `edges[i]`. If there is no outgoing edge from `i`, then `edges[i] == -1`.

You are also given two integers `node1` and `node2`.

Return the index of the node that can be reached from both `node1` and `node2`, such that the maximum between the distance from `node1` to that node, and from `node2` to that node is minimized. If there are multiple answers, return the node with the smallest index, and if no possible answer exists, return `-1`.

Note that `edges` may contain cycles.

### Input Format
- First line: Array `edges` where `edges[i]` is the outgoing edge from node `i` (or `-1` if none)
- Second line: Integer `node1` (first starting node)
- Third line: Integer `node2` (second starting node)

### Output Format
- Return the index of the optimal meeting node, or `-1` if none exists

### Constraints
- `n == edges.length`
- `2 <= n <= 10^5`
- `-1 <= edges[i] < n`
- `edges[i] != i`
- `0 <= node1, node2 < n`

### Examples

**Example 1:**
```
Input: edges = [2,2,3,-1], node1 = 0, node2 = 1
Output: 2
Explanation: The distance from node 0 to node 2 is 1, and the distance from node 1 to node 2 is 1.
The maximum of those two distances is 1. It can be proven that we cannot get a node with a smaller maximum distance than 1, so we return node 2.
```

**Example 2:**
```
Input: edges = [1,2,-1], node1 = 0, node2 = 2
Output: 2
Explanation: The distance from node 0 to node 2 is 2, and the distance from node 2 to itself is 0.
The maximum of those two distances is 2. It can be proven that we cannot get a node with a smaller maximum distance than 2, so we return node 2.
```

### Test Cases

#### Test Case 1
**Input:**
```
edges = [2,2,3,-1]
node1 = 0
node2 = 1
```
**Output:**
```
2
```
**Explanation:** Distance from 0 to 2 is 1, from 1 to 2 is 1. Maximum is 1, which is optimal.

---

#### Test Case 2
**Input:**
```
edges = [1,2,-1]
node1 = 0
node2 = 2
```
**Output:**
```
2
```
**Explanation:** Distance from 0 to 2 is 2, from 2 to itself is 0. Maximum is 2.

---

#### Test Case 3
**Input:**
```
edges = [1,2,3,4,-1]
node1 = 0
node2 = 2
```
**Output:**
```
2
```
**Explanation:** Common nodes: 2, 3, 4. Node 2 has max(2,0)=2. Node 3 has max(3,1)=3. Node 4 has max(4,2)=4. Node 2 is optimal.

---

#### Test Case 4
**Input:**
```
edges = [4,4,4,5,6,-1,-1]
node1 = 1
node2 = 2
```
**Output:**
```
4
```
**Explanation:** Node 4 is reachable from both with distance 1 each. Maximum distance is 1.

---

#### Test Case 5
**Input:**
```
edges = [1,2,-1]
node1 = 0
node2 = 1
```
**Output:**
```
1
```
**Explanation:** Common nodes: 1, 2. Node 1 has max(1,0)=1. Node 2 has max(2,1)=2. Node 1 is optimal with smaller max distance.

---

#### Test Case 6
**Input:**
```
edges = [-1,-1]
node1 = 0
node2 = 1
```
**Output:**
```
-1
```
**Explanation:** No outgoing edges from either node, so no common reachable node exists.

---

#### Test Case 7
**Input:**
```
edges = [2,0,1]
node1 = 0
node2 = 1
```
**Output:**
```
0
```
**Explanation:** Cycle exists: 0→2→1→0. Common nodes: 0, 1, 2. Node 0 has max(0,1)=1. Node 1 has max(2,0)=2. Node 2 has max(1,2)=2. Node 0 is optimal.

---

#### Test Case 8
**Input:**
```
edges = [1,2,3,4,5,6,7,-1]
node1 = 0
node2 = 4
```
**Output:**
```
4
```
**Explanation:** Common nodes: 4, 5, 6, 7. Node 4 has max(4,0)=4. Node 5 has max(5,1)=5. Node 6 has max(6,2)=6. Node 7 has max(7,3)=7. Node 4 is optimal.

---

#### Test Case 9
**Input:**
```
edges = [5,4,5,4,6,6,-1]
node1 = 0
node2 = 2
```
**Output:**
```
5
```
**Explanation:** Both nodes 0 and 2 reach node 5 early in their paths.

---

#### Test Case 10
**Input:**
```
edges = [1,-1]
node1 = 0
node2 = 1
```
**Output:**
```
1
```
**Explanation:** From 0, we reach 1 (distance 1). From 1, distance to itself is 0. Maximum is 1.

---

**End of Coding Problems**
