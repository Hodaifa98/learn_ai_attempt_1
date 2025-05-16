# Unit2-1. Problem formulation

Every search-based agent follows these steps:
1. Define the problem formally
1. Choose a search strategy
1. Execute the search to find a solution path

A problem is specified by:
- State space (possible configurations)
- Initial state
- Actions (and the successor function mapping a state -> resulting state)
- Goal test (predicate to check if a state is a goal)
- Path cost (numeric cost function; default each step = 1)

#### Key Definitions
| | |
| ------------- | ------------- |
| State | A complete description of the world at a given moment. Initial state Where the agent starts. |
| Action | A choice the agent can make; transforms one state into another. |
| Successor function: | Given a state, returns all (action, next_state) pairs. |
| Goal test | Boolean check—have we reached our objective? |
| Path cost | Sum of individual costs along a path; used to rank solutions. |

#### Example: 8-Puzzle
**State:** positions of tiles (and blank) on a 3×3 board

**Initial:** a scrambled configuration (e.g.,)
```
1 2 3
4 _ 6
7 5 8
```
**Actions:** move blank up/down/left/right (when possible)

**Successor:** swapping blank with adjacent tile

**Goal test:**
```
1 2 3
4 5 6
7 8 _
```
**Path cost:** each move costs 1; total cost = number of moves.

