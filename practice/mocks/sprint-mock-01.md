# Sprint Mock 01: AIMLCZG557 ACI

Time: 120 minutes

Marks: 30

Conditions: Closed book. Show search tables, path costs, heuristic values, and
brief justifications.

Status: Original sprint mock based on local sample-question analysis, not an
instructor paper.

## Question 1: PEAS And Environment Classification [6 marks]

A hospital wants an autonomous medicine-delivery robot that moves through
wards, avoids people, delivers medicine boxes, and returns to charging docks.

1. Write the PEAS description. [2]
2. Classify the task environment on observability, determinism, episodic versus
   sequential, static versus dynamic, discrete versus continuous, and
   single-agent versus multi-agent. Give one-line justification for each. [3]
3. State whether the agent should be rational or omniscient, and explain the
   difference. [1]

## Question 2: Problem Formulation And Greedy Best-First Search [6 marks]

A rescue drone must travel from `S` to `G` using this graph:

```text
S-A:2, S-B:4
A-C:2, A-D:5
B-D:1, B-E:4
C-G:5
D-G:3
E-G:2
```

Heuristic values to goal:

```text
h(S)=6, h(A)=4, h(B)=3, h(C)=4, h(D)=2, h(E)=1, h(G)=0
```

1. Give the problem formulation: initial state, actions, transition model, goal
   test, and path cost. [2]
2. Apply Greedy Best-First Search and list the expansion order. [2]
3. Give the path found and total path cost. [1]
4. State one weakness of greedy best-first search. [1]

## Question 3: A* Search And Heuristic Quality [6 marks]

Use the same graph and heuristic from Question 2.

1. Apply A* search using `f(n)=g(n)+h(n)`. Show a table with node, `g`, `h`,
   and `f` for each expanded or frontier node. [3]
2. Give the final path and total cost. [1]
3. State the definition of admissibility. [1]
4. State the definition of consistency and explain why consistency is stronger
   for graph search. [1]

## Question 4: Local Search, GA, And ACO [6 marks]

A timetable optimizer tries to minimize clashes, room changes, and late-evening
classes.

1. Explain why this can be treated as a local search problem. [1]
2. Trace one hill-climbing iteration using this neighborhood:

```text
Current score = 18 clashes
Neighbor 1 = 15 clashes
Neighbor 2 = 20 clashes
Neighbor 3 = 14 clashes
```

Choose the next state and justify. [1]
3. Explain local maxima, plateau, and ridge in this context. [1.5]
4. Describe the GA cycle for this problem: representation, fitness, selection,
   crossover, mutation. [1.5]
5. Give one high-level role of pheromone and heuristic desirability in ACO.
   [1]

## Question 5: Game Playing, Alpha-Beta, And MCTS [6 marks]

Consider this left-to-right game tree. Root is MAX. Its children are MIN nodes.
Leaf utilities are:

```text
Left MIN: 3, 5, 2
Middle MIN: 4, 6, 1
Right MIN: 7, 8, 9
```

1. Compute the minimax value of each MIN node and the root. [2]
2. Trace alpha-beta pruning left to right. State where pruning occurs, if any.
   [2]
3. Explain why minimax assumes an optimal opponent. [0.75]
4. Describe the four MCTS phases and when MCTS is useful. [1.25]

## Marking Discipline

After the timer ends:

- Search errors go to `../error-log.md` with the exact wrong open-list choice.
- PEAS/environment errors must be repaired with a new scenario.
- Alpha-beta errors must be repaired by retracing a smaller tree before retrying
  this one.
