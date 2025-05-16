# Unit2-2. Uninformed Search Strategies
These strategies don't know anything about the goal’s location or how far it is—they just explore blindly, based on the search tree.

#### Search Strategy Dimensions
To compare strategies, we look at:

| Property             | Meaning                                              |
| -------------------- | ---------------------------------------------------- |
| **Completeness**     | Will it always find a solution if one exists?        |
| **Optimality**       | Does it find the *lowest-cost* solution?             |
| **Time Complexity**  | How many nodes are expanded (worst-case)?            |
| **Space Complexity** | How much memory is needed (e.g., to store frontier)? |

## 1. Breadth-First Search (BFS)
- Expand shallowest node first (level-order)
- Uses a FIFO queue (first-in, first-out)
- Good for finding shortest path (in steps), but slow and memory-hungry

**Properties:**
- Complete ✅
- Optimal ✅ (if cost = 1 per step)
- Time: O(b^d)
- Space: O(b^d)

```
b: branching factor (avg actions per state)
d: depth of the shallowest goal
```

## 2. Depth-First Search (DFS)
- Expand deepest node first (go down one branch before backtracking)
- Uses a LIFO stack (last-in, first-out)
- Fast and low memory, but can go infinitely deep or miss better solutions

**Properties:**
- Complete ❌ (fails if infinite depth or loops)
- Optimal ❌
- Time: O(b^m)
- Space: O(bm)

```
m: max depth of tree
```

## 3. Uniform-Cost Search (UCS)
- Expands node with lowest path cost (not depth)
- Uses a priority queue ordered by cumulative cost
- General version of BFS where costs may vary

**Properties:**
- Complete ❌ (fails if infinite depth or loops)
- Optimal ❌
- Time: O(b^⌈C*/ε⌉)
- Space: Same as time (keeps all nodes in memory)

```
C*: optimal solution cost
ε: smallest step cost
```

## 4. Depth-Limited Search
DFS with a depth cutoff

## 5. Iterative Deepening DFS (IDDFS)
Runs DFS to depth 1, 2, 3, … until goal found
Combines DFS’s low space with BFS’s completeness

## Summary table:
| Algorithm   | Complete        | Optimal | Time         | Space        |
| ----------- | --------------- | ------- | ------------ | ------------ |
| BFS         | ✅               | ✅       | O(b^d)       | O(b^d)       |
| DFS         | ❌               | ❌       | O(b^m)       | O(bm)        |
| UCS         | ✅               | ✅       | O(b^⌈C\*/ε⌉) | O(b^⌈C\*/ε⌉) |
| DLS / IDDFS | DLS ❌ / IDDFS ✅ | ❌ / ✅   | O(b^d)       | O(bd)        |
