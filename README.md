# CI2024_lab3

## Solving an n^2-1 puzzle aka the Mystic Square

This project implements an A* algorithm to solve the sliding puzzle problem

Initially, the Manhattan Distance heuristic was used. While this heuristic provided correct solutions, it resulted in a high cost (number of states evaluated) during the search.

To optimize performance, the Linear Conflict heuristic was introduced. Linear Conflict builds upon Manhattan Distance by adding penalties for tiles that are in the correct row or column but in the wrong order. This improvement significantly reduced the cost of solving puzzles by exploring fewer states while maintaining the same solution quality.

## 3x3 Results
For the 3x3 puzzle with 100,000 randomizations at initialization, the following results were observed for a random state:  
    - Manhattan distance: Quality=20, Cost=357  
    - Linear Conflict: Quality = 20, Cost = 199

## 4x4 Results
For the 4x4 puzzle, the number of randomizations was reduced to allow observing results within a reasonable runtime:  
    - Manhattan distance: Quality=30, Cost=7079   
    - Linear Conflict: Quality=30, Cost=1838

## Concluding Notes
- Linear Conflict showed promise but requires further optimization for large puzzles.
- Linear Conflict significantly reduces the cost compared to Manhattan distance
- Perhaps introducing some new heuristic could help provde a more optimized solution