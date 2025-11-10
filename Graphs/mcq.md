# Graphs - MCQ Questions

---

### Q1.

What is a graph in data structures?

A. A linear data structure with nodes connected in a sequence

B. A collection of nodes (vertices) connected by edges

C. A hierarchical data structure with parent-child relationships

D. A sorted collection of elements

**Answer:** B

**Explanation:** A graph is a non-linear data structure consisting of vertices (nodes) connected by edges. Unlike trees, graphs can have cycles and don't necessarily have a hierarchical structure.

---

### Q2.

What is the difference between a directed and an undirected graph?

A. Directed graphs have weighted edges, undirected don't

B. Directed graphs have edges with direction, undirected edges have no direction

C. Directed graphs cannot have cycles

D. Undirected graphs always have more edges

**Answer:** B

**Explanation:** In a directed graph (digraph), edges have a direction (A→B is different from B→A). In an undirected graph, edges have no direction (A-B is the same as B-A).

---

### Q3.

What is the time complexity of BFS (Breadth-First Search) for a graph with V vertices and E edges?

A. O(V)

B. O(E)

C. O(V + E)

D. O(V * E)

**Answer:** C

**Explanation:** BFS visits every vertex once (O(V)) and explores every edge once (O(E)), resulting in O(V + E) time complexity when using adjacency list representation.

---

### Q4.

Which data structure is typically used to implement BFS?

A. Stack

B. Queue

C. Priority Queue

D. Array

**Answer:** B

**Explanation:** BFS uses a queue (FIFO) to explore nodes level by level. Nodes are enqueued when discovered and dequeued for processing, ensuring level-order traversal.

---

### Q5.

What is the space complexity of DFS (Depth-First Search) using recursion?

A. O(1)

B. O(V) where V is the number of vertices

C. O(E) where E is the number of edges

D. O(V + E)

**Answer:** B

**Explanation:** Recursive DFS uses the call stack, which in the worst case can go as deep as the number of vertices V (e.g., in a linear graph), requiring O(V) space.

---

### Q6.

Which graph representation uses less space for sparse graphs?

A. Adjacency Matrix

B. Adjacency List

C. Edge List

D. Both A and B use same space

**Answer:** B

**Explanation:** Adjacency list stores only existing edges, requiring O(V + E) space. For sparse graphs (E << V²), this is much less than adjacency matrix which always uses O(V²) space.

---

### Q7.

What is a cycle in a graph?

A. A path that visits all vertices

B. A path where the starting vertex is the same as the ending vertex

C. A graph with no edges

D. A tree structure

**Answer:** B

**Explanation:** A cycle is a path in a graph where you can start at a vertex, follow edges, and return to the starting vertex. For example: A→B→C→A forms a cycle.

---

### Q8.

How do you detect a cycle in an undirected graph using DFS?

A. Check if any vertex is visited twice

B. Check if we visit an already visited vertex that is not the parent

C. Count the number of edges

D. Use BFS instead

**Answer:** B

**Explanation:** In undirected graph DFS, a cycle exists if we reach a visited vertex that is not the immediate parent of the current vertex. The parent check is necessary because edges are bidirectional.

---

### Q9.

What is the adjacency matrix representation for a graph with n vertices?

A. A 1D array of size n

B. A 2D array of size n × n

C. A linked list

D. A hash table

**Answer:** B

**Explanation:** An adjacency matrix is a 2D array of size n × n where matrix[i][j] = 1 (or weight) if there's an edge from vertex i to vertex j, otherwise 0.

---

### Q10.

What is a topological sort?

A. Sorting vertices by their values

B. Linear ordering of vertices in a DAG such that for every directed edge u→v, u comes before v

C. Sorting edges by weight

D. Random ordering of vertices

**Answer:** B

**Explanation:** Topological sort is a linear ordering of vertices in a Directed Acyclic Graph (DAG) where for every directed edge u→v, vertex u appears before vertex v in the ordering.

---

### Q11.

Which algorithm is used to find the shortest path in an unweighted graph?

A. Dijkstra's algorithm

B. Bellman-Ford algorithm

C. BFS

D. DFS

**Answer:** C

**Explanation:** BFS finds the shortest path in unweighted graphs because it explores nodes level by level, ensuring the first time a node is reached is via the shortest path.

---

### Q12.

What is a connected component in an undirected graph?

A. A vertex with the most edges

B. A subgraph where every pair of vertices has a path between them

C. The longest path in the graph

D. A vertex with no edges

**Answer:** B

**Explanation:** A connected component is a maximal subgraph where there's a path between every pair of vertices. A graph can have multiple disconnected components.

---

### Q13.

What is the time complexity of detecting a cycle in a directed graph using DFS?

A. O(V)

B. O(E)

C. O(V + E)

D. O(V²)

**Answer:** C

**Explanation:** Cycle detection in directed graphs using DFS visits each vertex once and explores each edge once, resulting in O(V + E) time complexity.

---

### Q14.

What is an in-degree of a vertex?

A. The number of outgoing edges from the vertex

B. The number of incoming edges to the vertex

C. The total number of edges connected to the vertex

D. The weight of the vertex

**Answer:** B

**Explanation:** In-degree is the number of edges coming into a vertex. For example, if edges are A→B and C→B, the in-degree of B is 2.

---

### Q15.

Which algorithm can detect negative weight cycles in a graph?

A. Dijkstra's algorithm

B. BFS

C. Bellman-Ford algorithm

D. Topological sort

**Answer:** C

**Explanation:** Bellman-Ford algorithm can detect negative weight cycles. After V-1 relaxations, if we can still relax any edge, a negative cycle exists.

---

### Q16.

What is a bipartite graph?

A. A graph with two vertices

B. A graph whose vertices can be divided into two disjoint sets such that no two vertices within the same set are adjacent

C. A graph with exactly two edges

D. A directed graph with two components

**Answer:** B

**Explanation:** A bipartite graph can be colored with two colors such that no two adjacent vertices have the same color. Example: vertices {1,3,5} and {2,4,6} with edges only between the sets.

---

### Q17.

How can you check if a graph is bipartite?

A. Count the number of vertices

B. Use BFS/DFS with 2-coloring

C. Check if it has cycles

D. Use topological sort

**Answer:** B

**Explanation:** Use BFS/DFS to color vertices with two colors. If you can color the entire graph without adjacent vertices having the same color, it's bipartite. Odd-length cycles make a graph non-bipartite.

---

### Q18.

What is the purpose of a visited array in graph traversal?

A. To store vertex values

B. To prevent infinite loops and redundant processing

C. To count edges

D. To sort vertices

**Answer:** B

**Explanation:** The visited array tracks which vertices have been explored, preventing infinite loops in graphs with cycles and avoiding redundant processing of the same vertex.

---

### Q19.

In a complete graph with n vertices, how many edges are there?

A. n

B. n - 1

C. n(n-1)/2

D. n²

**Answer:** C

**Explanation:** A complete graph has an edge between every pair of vertices. The number of ways to choose 2 vertices from n is C(n,2) = n(n-1)/2.

---

### Q20.

What is the difference between DFS and BFS traversal?

A. DFS uses queue, BFS uses stack

B. DFS explores as far as possible along each branch, BFS explores level by level

C. DFS is faster than BFS

D. BFS cannot detect cycles

**Answer:** B

**Explanation:** DFS goes deep into the graph exploring one path completely before backtracking (uses stack/recursion). BFS explores all neighbors at current level before moving to the next level (uses queue).

---

### Q21.

What is a strongly connected component (SCC) in a directed graph?

A. A component with the most vertices

B. A maximal subgraph where every vertex is reachable from every other vertex

C. A component with no cycles

D. The largest connected component

**Answer:** B

**Explanation:** In a strongly connected component, there's a directed path from any vertex to any other vertex within that component. Kosaraju's and Tarjan's algorithms find SCCs.

---

### Q22.

What is the minimum number of edges needed to make a graph with n vertices connected?

A. n

B. n - 1

C. n + 1

D. n²

**Answer:** B

**Explanation:** A tree (connected acyclic graph) with n vertices has exactly n-1 edges, which is the minimum required to connect all vertices. Adding any edge creates a cycle.

---

### Q23.

What is a DAG (Directed Acyclic Graph)?

A. A directed graph with cycles

B. An undirected graph without cycles

C. A directed graph without cycles

D. A graph with only one vertex

**Answer:** C

**Explanation:** A DAG is a directed graph that contains no cycles. It's used in scheduling, dependency resolution, and topological sorting. Every DAG has at least one topological ordering.

---

### Q24.

Which graph algorithm uses a "parent" array to track paths?

A. Only BFS

B. Only DFS

C. Both BFS and DFS

D. Neither BFS nor DFS

**Answer:** C

**Explanation:** Both BFS and DFS can use a parent array to reconstruct paths. When exploring from vertex u to v, we set parent[v] = u, allowing path reconstruction by backtracking.

---

### Q25.

What is the purpose of topological sorting?

A. To sort vertices by value

B. To find the shortest path

C. To order tasks/vertices respecting dependencies

D. To detect cycles

**Answer:** C

**Explanation:** Topological sort orders vertices in a DAG such that all dependencies come before dependent vertices. It's used in task scheduling, build systems, and course prerequisites.

---

### Q26.

How do you perform topological sort using DFS?

A. Process vertices in increasing order

B. Push vertices to stack after visiting all descendants, then pop stack

C. Use BFS instead

D. Sort vertices by in-degree

**Answer:** B

**Explanation:** In DFS-based topological sort, after visiting all descendants of a vertex, push it to a stack. The final stack (popped order) gives topological ordering.

---

### Q27.

What is Kahn's algorithm used for?

A. Finding shortest paths

B. Topological sorting using BFS and in-degree

C. Detecting cycles

D. Finding minimum spanning tree

**Answer:** B

**Explanation:** Kahn's algorithm performs topological sort by repeatedly removing vertices with in-degree 0 and reducing in-degrees of their neighbors. If all vertices are processed, a topological order exists.

---

### Q28.

In the "find the town judge" problem, what graph concept is used?

A. Cycle detection

B. In-degree and out-degree counting

C. Shortest path

D. Connected components

**Answer:** B

**Explanation:** The judge has in-degree n-1 (everyone trusts the judge) and out-degree 0 (judge trusts nobody). We count in-degrees and out-degrees to identify the judge.

---

### Q29.

What does it mean if a graph traversal uses a "recursion stack"?

A. The graph has cycles

B. DFS is being used with recursive implementation

C. BFS is being used

D. The graph is disconnected

**Answer:** B

**Explanation:** A recursion stack implies recursive DFS implementation. The call stack maintains the traversal state, with deeper recursion representing deeper exploration into the graph.

---

### Q30.

What is the space complexity of the adjacency list representation?

A. O(V)

B. O(E)

C. O(V + E)

D. O(V²)

**Answer:** C

**Explanation:** Adjacency list requires O(V) space for the array of vertices and O(E) space to store all edges, totaling O(V + E) space complexity.

---

**End of MCQ Questions**
