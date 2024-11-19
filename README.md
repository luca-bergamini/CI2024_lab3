# CI2024_lab3

In this laboratory we are going to use different path-search algorithms to solve a generic $n^2 - 1$ puzzle (also known as Gem Puzzle, Boss Puzzle, Mystic Square, etc.). I implemented two different solutions:
- **A-star (A\*) Algorithm**: combines the cost of reaching a state and a heuristic estimate of the distance to the goal (**Manhattan distance**). It guarantees optimality;
- **Breadth-First Search (BFS) Algorithm**: explores all states level by level, ensuring the shortest solution in terms of moves. However, it can be slower because it's not using a heuristic to decide which is the best move.

## Results

Using as parameters:
- **PUZZLE_DIM** = 3
- **RANDOMIZE_STEPS** = 100_000

Evaluating the `path length` and the calls made to the `do_action()` function.

#### A-star (A*)

| PATH LENGTH | CALLS |
| :- | :- |
28 | 20_948

#### Breadth-First Search (BFS)

| PATH LENGTH | CALLS |
| :- | :- |
28 | 1_250_460

## Conclusion

We can conclude that **A-star (A\*)** achieves better results. Both algorithms found the optimal solution with a path length of 28, but **A\*** required **fewer calls** to the `do_action()` function. Highlighting that the heuristic used in **A\*** greatly improves the search efficiency by guiding the exploration, while **BFS** explores all the possibilities, leading to a much higher computational cost.

Finding a great way to develop the A* algorithm I discuss with @andreabioddo.
