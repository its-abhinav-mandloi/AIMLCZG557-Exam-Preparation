# AIMLCZG557 Formula Sheet

## Search

- Greedy Best First Search selection rule:
  - choose node with minimum `h(n)`
- A* selection rule:
  - `f(n) = g(n) + h(n)`
- `g(n)`:
  - exact path cost from start to node `n`
- `h(n)`:
  - estimated remaining cost from node `n` to a goal
- Admissibility:
  - `0 <= h(n) <= h*(n)`
- Consistency:
  - `h(n) <= c(n,n') + h(n')`

## Local Search

- Hill climbing:
  - move to a better neighboring state
- Example objective:
  - minimize `h(n) = number of conflicting pairs`
- Common failure modes:
  - local maximum
  - plateau
  - ridge

## Genetic Algorithm

- Pipeline:
  - encode solution -> compute fitness -> select parents -> crossover -> mutate -> form next generation

## Ant Colony Optimization

- Transition choice depends on:
  - pheromone strength
  - route desirability / inverse cost
- Pheromone update intuition:
  - new pheromone = retained old pheromone + deposited pheromone

## Game Playing

- Minimax:
  - MAX chooses max child value
  - MIN chooses min child value
- Alpha-beta:
  - `alpha`: best score MAX can guarantee so far
  - `beta`: best score MIN can guarantee so far
  - prune when `alpha >= beta`

## PEAS Reminder

- `P`: Performance Measure
- `E`: Environment
- `A`: Actuators
- `S`: Sensors
