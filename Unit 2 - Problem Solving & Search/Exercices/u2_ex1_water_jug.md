# Unit 2 - Exercice 1 - Water jug problem
## Problem:
- Two jugs: 4L and 3L jugs, infinite water supply.
- Goal: Measure exactly 2L.

Define: 
- State representation
- Actions & successor function
- Goal test
- Path cost

---

## Solution:
#### 1. State representation

We need a way to describe any configuration of the two jugs. A good choice is a tuple:

```
State = (x, y)
```

where:

- x is the amount of water in the 4-liter jug (0 ≤ x ≤ 4)
- y is the amount of water in the 3-liter jug (0 ≤ y ≤ 3)

Initial state (both jugs ar empty): 
```
(0,0)
```

Goal test: Check if either jug contains exactly 2 liters.

```
x == 2 or y == 2
```

#### 2. Actions and Successor Function
At any state, the agent can perform the following actions:

| Action | Description | Format |
| ---------- | --------------------- |
| `Fill4`    | Fill the 4L jug | (4, y) |
| `Fill3`    | Fill the 3L jug | (x, 3) |
| `Empty4`   | Empty the 4L jug | (0, y) |
| `Empty3`   | Empty the 3L jug | (x, 0) |
| `Pour4to3` | Pour water from 4L to 3L until one is full/empty | (x - min(x, 3 - y), y + min(x, 3 - y)) |
| `Pour3to4` | Pour water from 3L to 4L until one is full/empty | (x + min(y, 4 - x), y - min(y, 4 - x)) |

For example:

- From (4, 0), action Pour4to3 → (1, 3) (3L is full, 4L has 1L left)
- From (0, 2), action Empty3 → (0, 0)
- Each action leads to a new state.

The successor function as a function that takes a state and returns the resulting states from all valid actions.

Path Cost: 

Each action costs 1 (uniform step cost).
So, total cost = number of steps to reach goal.

## Sample Partial Search Tree
1. Start from (0,0):
1. Fill4 → (4, 0)
1. Pour4to3 → (1, 3)
1. Empty3 → (1, 0)
1. Pour4to3 → (0, 1)
1. Fill4 → (4, 1)
1. Pour4to3 → (2, 3)

**Total path cost:** 7 (each action has cost 1)

A partial search tree is a subset of a search tree, a structure that represents all possible paths the agents could take from initial state to the goal.

NB: Search tree will be covered next.