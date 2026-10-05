# CONTRIBUTION.md

## Project Contribution

This project focuses on the architectural design and empirical performance analysis of **BFS and DFS** using a 26-node graph from **A to Z**.

## Contribution Areas

* Designed the **BFS module** using a queue-based approach.
* Designed the **DFS module** using a stack-based approach.
* Created the **26-node A–Z graph** using an adjacency-list representation.
* Defined **Best, Average, and Worst cases** as B, M, and Z.
* Implemented node expansion counting.
* Measured execution time using `time.perf_counter()`.
* Performed **3 benchmark iterations** and calculated average execution time.
* Used **py-spy** for profiling and generated `profile.svg`.
* Designed the system using the **Full C4 Model**.
* Prepared the Context, Container, Component, and Code-level architecture.
* Documented the system design and performance analysis.

## Coding Guidelines

* Keep the code simple and readable.
* Use meaningful variable and function names.
* Keep BFS and DFS implementations separate.
* Use appropriate data structures such as queue and stack.
* Maintain the same graph structure for performance comparison.
* Avoid unnecessary changes to the existing implementation.
* Test the program after making changes.

## Testing

The system should be tested for:

1. BFS traversal.
2. DFS traversal.
3. All 26 graph nodes from A to Z.
4. Starting node A.
5. Best case – B.
6. Average case – M.
7. Worst case – Z.
8. Number of nodes expanded.
9. Execution time.
10. Average execution time over 3 runs.
11. py-spy profiling output.

## Git Workflow

1. Create or update the project files.
2. Test the implementation.
3. Add the changes using Git.
4. Commit the changes with a meaningful message.
5. Push the changes to the repository.

### Example Commit Messages

```text
Added BFS implementation
Added DFS implementation
Added performance benchmarking
Added py-spy profiling
Added Full C4 architecture
Updated project documentation
```

## Architecture Contribution

The system is documented using the **Full C4 Model**:

* **Level 1 – Context:** Shows the researcher/user interacting with the BFS vs DFS analysis system.
* **Level 2 – Container:** Shows Graph Input & Case Configurator, Search Engine, BFS Module, DFS Module, Performance Profiler, and Output/Results.
* **Level 3 – Component:** Shows Frontier, Visited Set, Goal Test, and Node Counter & Timer.
* **Level 4 – Code:** Shows `bfs()`, `dfs()`, `graph`, `test_cases`, and `benchmark_search()`.

## Performance Analysis

The contribution includes comparison using two main metrics:

* **Execution time**
* **Number of nodes expanded**

The system performs multiple runs and calculates the average execution time for BFS and DFS.

## Profiling

The project uses **py-spy** to sample Python call-stack activity and generate a flame graph named:

```text
profile.svg
```

This helps visualize where execution time is spent during the search process.

## AI Contribution

AI tools were used for:

* Formatting the Full C4 Model.
* Generating Mermaid diagrams.
* Preparing draw.io-ready architecture diagrams.
* Organizing the report layout.

The implementation, empirical execution, node counting, benchmarking, and py-spy profiling were performed independently.

## Conclusion

The contribution establishes a clear connection between the system requirements, C4 architecture, search algorithms, benchmarking, and low-level implementation of the BFS vs DFS performance analysis system.
