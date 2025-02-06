# Minimum Dominating Set Problem (CS301 - Algorithms | Spring 2022 - 2023)

## Project Description
This project explores the **Minimum Dominating Set Problem**, a fundamental problem in graph theory and combinatorial optimization. Given an **undirected graph** $(G = (V, E))$, a **dominating set** is a subset $(D \subseteq V) $ such that every vertex in $(V - D)$ has at least one neighbor in $(D)$. The goal is to find the **smallest** possible dominating set for a given graph.

The problem is **NP-complete**, making exact solutions computationally intractable for large graphs. This project implements **two approaches** to solve the problem:
1. **Brute Force Algorithm** - An exhaustive search to find the optimal solution.
2. **Greedy Heuristic Algorithm** - An approximation method for faster computation with a performance guarantee.

## Algorithms Implemented
### 1. Brute Force Algorithm
- Generates all possible subsets of vertices.
- Checks each subset to determine if it is a dominating set.
- Returns the minimum-sized valid dominating set.
- **Time Complexity:** $( O(2^n \cdot k(n-k))$, making it impractical for large graphs.

### 2. Greedy Heuristic Algorithm
- Assigns weights to each vertex based on its degree.
- Iteratively selects the highest-weight vertex and updates the dominating set.
- Provides an approximation guarantee of **(ln(Δ) + 2)**, where Δ is the maximum degree in the graph.
- **Time Complexity:** $( O(V^2))$, making it much more efficient than brute force.

## Graph Instance Generation
To test our algorithms, we implemented a **random graph generator** that produces adjacency matrices with:
- Binary values (0 for no edge, 1 for an edge).
- Undirected structure by ensuring symmetry.
- No self-loops (diagonal elements are 0).

## Results & Performance Analysis
- The **brute force method** works accurately for small graphs but becomes infeasible for large inputs due to exponential complexity.
- The **greedy heuristic** provides a fast and reasonable approximation while maintaining a theoretical performance bound.
- Randomly generated test cases confirm the correctness of both approaches.

## References
- Garey, M. R., & Johnson, D. S. (1979). *Computers and Intractability: A Guide to the Theory of NP-Completeness.*
- Kuhn, F. (2013). *Approximation Algorithms for Dominating Set Problems.*
