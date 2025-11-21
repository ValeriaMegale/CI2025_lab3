

## Solvers Implemented

### 1. Greedy Best-First Search (`best_first_solver`)

This is an **informed search algorithm** prioritizing speed and efficiency.

* **Usage**: `best_first_solver(problem, heuristic_map, source, target)`
* **Mechanism**: It selects the next node based on a **heuristic function**, which is the Euclidean distance from the current node to the target.
* **Characteristics**:
    * Designed to prioritize nodes that appear closer to the goal.
    * **Fast**, but generally **not guaranteed to find the optimal shortest path**.
    * *Note: While the original description states it achieves the same results as Bellman-Ford, Greedy Best-First is fundamentally non-optimal.*

### 2. SPFA - Shortest Path Faster Algorithm (`solver`)

This is an **optimal search algorithm** that handles complex graph conditions.

* **Usage**: `solver(problem, source, target)`
* **Mechanism**: It is an optimization of the standard Bellman-Ford algorithm. It uses a queue to selectively relax only the vertices whose distances have recently changed, which avoids redundant computations.
* **Characteristics**:
    * It supports graphs with **negative edge weights**.
    * It includes logic to correctly detect **negative cycles** in the graph.
    * **Results**: It guarantees the **optimal shortest path** (or correctly identifies an unconstrained path due to a negative cycle).
    * It typically runs faster than the full Bellman-Ford algorithm on sparse graphs.

work with: https://github.com/LucaFavole