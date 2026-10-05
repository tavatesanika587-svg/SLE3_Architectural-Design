# BFS vs DFS – 26-Node Empirical Performance Analysis System

## 1. Project Overview

The **BFS vs DFS Empirical Performance Analysis System** evaluates the traversal performance of Breadth-First Search (BFS) and Depth-First Search (DFS) on a 26-node graph from A to Z, starting from node A.

The system measures execution time, counts the number of nodes expanded, and uses py-spy to generate a flame graph profile.

## 2. Objectives

* Implement BFS and DFS.
* Evaluate traversal on a 26-node graph.
* Measure the number of nodes expanded.
* Measure execution time using `time.perf_counter()`.
* Perform 3 benchmark runs.
* Calculate average execution time.
* Generate performance profiles using py-spy.
* Design the system using the Full C4 Model.

## 3. Technologies Used

* Python
* BFS
* DFS
* `collections.deque`
* Python `set`
* `time.perf_counter()`
* py-spy
* Mermaid
* draw.io

## 4. System Architecture

The system is documented using the four levels of the C4 Model:

**Context → Container → Component → Code**

### Level 1 – System Context

The user/researcher provides the graph topology and target goal cases.

The system performs the search and returns:

* Node expansion count
* Average execution time
* Flame graph profile

The external profiler used is **py-spy**.

### Level 2 – Container

The main containers are:

* Graph Input & Case Configurator
* Search Engine
* BFS Module
* DFS Module
* Performance Profiler
* Output / Results

### Level 3 – Component

The Search Engine contains:

* **Frontier** – stores active candidate paths.
* **Visited Set** – prevents duplicate visits and cyclic loops.
* **Goal Test** – checks whether the current node is the target.
* **Node Counter & Timer** – counts node expansions and measures execution time.

### Level 4 – Code

The main code elements are:

* `bfs(graph, start, goal)`
* `dfs(graph, start, goal)`
* `graph`
* `test_cases`
* `benchmark_search()`

## 5. Graph

The system uses a graph containing **26 nodes from A to Z**.

The starting node is **A**.

The system evaluates:

* Best Case – Goal B
* Average Case – Goal M
* Worst Case – Goal Z

## 6. BFS Module

BFS performs level-by-level traversal.

It uses `collections.deque` as a FIFO queue.

The BFS function returns the complete path and the number of nodes expanded.

## 7. DFS Module

DFS explores branches deeply before backtracking.

It uses a standard Python list as a LIFO stack.

The DFS function returns the complete path and the number of nodes expanded.

## 8. Performance Profiler

The Performance Profiler:

* Executes 3 iterations per case.
* Uses `time.perf_counter()`.
* Calculates average runtime.
* Uses py-spy for stack profiling.
* Generates `profile.svg`.

## 9. Output

The system provides:

* Search path
* Total nodes expanded
* Execution duration
* Average performance results

## 10. Design Decisions

### Adjacency List

The graph is represented using a Python dictionary of lists for clean key lookup and low memory overhead.

### Procedural Architecture

Standalone functions such as `bfs()` and `dfs()` are used instead of complex OOP structures.

### Dual Metrics

Both execution time and the number of nodes expanded are measured.

Node expansion provides a useful hardware-independent comparison because execution time on a 26-node graph can be extremely small.

## 11. Profiling Output

The py-spy profiler generates:

```text
profile.svg
```

The profile represents the sampled CPython call stack as a flame graph.

## 12. Conclusion

The system provides an empirical comparison of BFS and DFS traversal performance.

The Full C4 Model connects the overall system with its containers, components, and code-level implementation.

The architecture shows how queue-based and stack-based traversal affect node expansion and execution performance.
