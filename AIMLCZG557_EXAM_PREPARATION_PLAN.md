# AIMLCZG557 MID-SEM Exam Preparation Plan

## Exam Snapshot

- Subject: Artificial and Computational Intelligence
- Course code used in this repo: `AIMLCZG557`
- Exam type: MID-SEM
- Exam date: 21 June 2026
- Available prep time: 2 days
- Learner profile: beginner, wants slow and detailed teaching with derivations, visuals, numericals, and worked examples
- Mid-sem marks: 30

## Authoritative Scope Used

### Confirmed from course files

- `Files (Common Resources)-20260613/ACI_HO.pdf`
- `OneDrive_3_13-06-2026/Class Materials/AIMLZG557_ACI_HO.pdf`
- `Files (Common Resources)-20260613/Lecture Slides/CS1.pdf`
- `Files (Common Resources)-20260613/EC1 Dates.pdf`

### Confirmed exam boundary

- `CS1.pdf` states: `EC2: Mid-semester examination (30 marks) -> Topics covered from CS#1 to CS#8`.
- The handout maps those sessions to:
  - `CS1`: Introduction to AI
  - `CS2`: Intelligent agents, environments, rationality
  - `CS3`: Problem formulation, uninformed to informed search, heuristics, greedy best-first search, A*
  - `CS4`: heuristic design, admissibility, consistency, relaxed problems, pattern databases, local search introduction
  - `CS5`: hill climbing, local beam search, online search agents, genetic algorithm, intro to ACO
  - `CS6`: ACO and neural architecture search
  - `CS7`: NAS continuation and introduction to game playing, static evaluation, minimax
  - `CS8`: Monte Carlo tree search and stochastic games

### Exam-style evidence from local practice material

- `Assign1_PS7.pdf`: PEAS, environment dimensions, Greedy Best First Search implementation, complexity, path tracing
- `Files (Common Resources)-20260613/Webinar-1/CS4informed_search.pptx`: A* worked examples
- `Files (Common Resources)-20260613/Webinar 2 materials/Sample-questions-from-previous-year-exam.pptx`: A* tree expansion, `g(n), h(n), f(n)` calculation, PEAS, and task-environment classification
- `Files (Common Resources)-20260613/Webinar 2 materials/ACI-LabSession2A-HillClimbing-TravelOptimization.pptx`: hill climbing numerical workflow

## Important Inferences

- `CS8` slide PDF is not present in this folder, so detailed `CS8` subtopic emphasis is inferred from the handout, not from a local slide deck.
- Because both the assignment and sample-question deck are search-heavy, search numericals are likely high value for the mid-sem. This is a reasoned priority judgment, not a guaranteed marks split.
- NAS is in scope because `CS6` and `CS7` cover it, but for a 2-day beginner sprint it should be studied as a theory-first topic unless a new paper suggests otherwise.

## Workspace Inventory That Informed This Plan

### Core course material

- Handouts: `ACI_HO.pdf`, `AIMLZG557_ACI_HO.pdf`
- Lecture slides: `CS1.pdf` to `CS7.pdf`, `C1_AIMLCZG557.pdf` to `C7_AIMLCZG557.pdf`
- Recordings: 14 lecture recordings across two instructor folders

### Practical and exam-support material

- Assignment: `Assign1_PS7.pdf`
- Webinar decks: informed search, hill climbing travel optimization
- Notebooks: `A_star_implementation.ipynb`, `IDA.ipynb`, `HillClimb.ipynb`
- Sample paper material: `Sample-questions-from-previous-year-exam.pptx`

### Supporting but lower-priority material for mid-sem

- `CS4_Paper.pdf` on heuristic learning
- Additional material PDFs on algorithms and GA

### Unrelated to exam prep execution

- `.DS_Store`
- Duplicate slide copies across source folders

## Priority Order For 2 Days

### Tier 1: must-master

1. PEAS, agents, environment dimensions, rationality
2. Problem formulation
3. Greedy Best First Search
4. A* search
5. Heuristic design, admissibility, consistency
6. Hill climbing and local beam search
7. Minimax and alpha-beta pruning

### Tier 2: learn well, but after Tier 1

8. Genetic algorithms
9. Ant Colony Optimization
10. Online search agents
11. Monte Carlo tree search
12. Stochastic games

### Tier 3: theory-only if time gets tight

13. Neural architecture search
14. CoDeepNEAT / neuro-evolution details

## Prerequisite Graph

1. AI foundations -> intelligent agents -> PEAS -> environment classification
2. Problem formulation -> search tree vocabulary -> path cost `g(n)` -> heuristic `h(n)` -> evaluation `f(n)=g(n)+h(n)`
3. Greedy Best First Search -> A* -> admissibility -> consistency -> heuristic design
4. State-space optimization idea -> hill climbing -> local beam -> GA -> ACO
5. Adversarial setting -> utility -> game tree -> minimax -> alpha-beta pruning -> MCTS

## Topic Sequence With Learning Outcomes

### Block 1: Foundations and agent language

- Concepts: AI viewpoints, rational agent, PEAS, observability, determinism, episodic/sequential, static/dynamic, discrete/continuous, single/multi-agent
- Must be able to do:
  - write PEAS for a scenario
  - classify the task environment with justification
  - explain why an agent is rational

### Block 2: Search basics

- Concepts: initial state, actions, transition model, goal test, path cost, state space
- Must be able to do:
  - write complete problem formulation
  - distinguish uninformed vs informed search
  - explain `g(n)`, `h(n)`, `f(n)`

### Block 3: Informed search numericals

- Concepts: greedy best-first search, A*, admissibility, consistency, relaxed problems, pattern database idea
- Must be able to do:
  - expand a search tree level by level
  - compute `g/h/f`
  - select next node correctly
  - justify optimality conditions for A*

### Block 4: Local search and optimization

- Concepts: state-as-solution, hill climbing, local maxima, plateau, ridge, local beam search, online search, GA basics, ACO basics
- Must be able to do:
  - compare path search vs local search
  - explain hill climbing step by step
  - describe GA cycle: representation -> fitness -> selection -> crossover -> mutation
  - explain ACO transition and pheromone update at a high level

### Block 5: Game playing

- Concepts: adversarial search, utility, MAX/MIN, game tree, minimax, alpha-beta pruning, static evaluation
- Must be able to do:
  - build a game tree
  - propagate utility values bottom-up
  - identify pruned branches
  - explain why minimax assumes optimal opponent play

### Block 6: Finish-theory topics

- Concepts: MCTS, stochastic games, NAS, CoDeepNEAT
- Must be able to do:
  - give intuition and pipeline
  - write short exam answers with one example

## Formula, Derivation, and Numerical Checklist

### Agents and environment

- No heavy formulas, but memorize the PEAS template and environment-dimension vocabulary.

### Search

- `g(n)`: exact path cost from start to node `n`
- `h(n)`: estimated cost from `n` to goal
- Greedy Best First Search: choose node with minimum `h(n)`
- A*: choose node with minimum `f(n)=g(n)+h(n)`
- Admissibility: `0 <= h(n) <= h*(n)`
- Consistency: `h(n) <= c(n,n') + h(n')`
- Derivation to be comfortable with:
  - why consistency implies nondecreasing `f` values along a path
  - why admissibility supports A* optimality

### Local search

- Hill climbing objective:
  - minimize or maximize evaluation/fitness
- N-Queens style fitness example:
  - `h(n) = number of conflicting queen pairs`
- GA vocabulary:
  - chromosome, gene, population, fitness, crossover, mutation, selection
- ACO core transition rule:
  - probability depends on pheromone strength and route desirability
- ACO pheromone update:
  - evaporation plus reinforcement

### Game playing

- Minimax recurrence:
  - MAX node takes maximum child utility
  - MIN node takes minimum child utility
- Alpha-beta:
  - `alpha = best guaranteed score for MAX so far`
  - `beta = best guaranteed score for MIN so far`
- Prune when `alpha >= beta`

## 2-Day Detailed Timetable

This timetable is meant for the final two focused prep days immediately before the exam on 21 June 2026.

## Day 1: 19 June 2026

- `07:00-07:30` Wake up, water, no-phone setup, print or open formula sheet
- `07:30-09:15` CS1-CS2
  - AI viewpoints
  - rational agents
  - PEAS
  - environment dimensions
  - Do 3 PEAS problems and 3 environment classifications
- `09:15-09:35` Break
- `09:35-11:35` CS3 core search
  - problem formulation
  - greedy best-first
  - A*
  - manual tree expansion
  - do one full numerical from sample-question deck
- `11:35-12:00` Active recall
  - explain `g/h/f` without notes
  - solve one mini A* example from scratch
- `12:00-13:00` Lunch and short walk
- `13:00-15:00` CS4 heuristics
  - admissibility
  - consistency
  - relaxed problems
  - pattern database idea
  - write 5 one-line exam definitions
- `15:00-15:20` Break
- `15:20-17:20` CS5 local search
  - hill climbing
  - failure modes
  - local beam
  - online search
  - one worked hill-climbing numerical from webinar material
- `17:20-17:50` Tea + visual lab review
- `17:50-19:00` Formula sheet pass 1
  - collect all search and local-search formulas
  - add one example beside each formula
- `19:00-20:00` Dinner
- `20:00-21:45` Mixed practice block
  - 2 PEAS questions
  - 1 environment classification
  - 1 A* numerical
  - 1 hill-climbing short answer
- `21:45-22:15` Error-repair session
  - write every mistake into `practice/error-log.md`
- `22:15-23:00` Light revision
  - oral recap of Day 1 concepts
- `23:00-07:00` Sleep

## Day 2: 20 June 2026

- `07:00-07:20` Wake up and recall Day 1 from memory
- `07:20-09:20` CS5 advanced + CS6
  - genetic algorithms
  - ACO
  - NAS theory
  - focus on process diagrams and definitions, not implementation
- `09:20-09:40` Break
- `09:40-12:10` CS7-CS8 game playing
  - adversarial search
  - utility
  - minimax
  - alpha-beta pruning
  - MCTS and stochastic games overview
  - solve 2 minimax trees and mark pruned branches
- `12:10-13:00` Lunch
- `13:00-14:15` Formula sheet pass 2
  - finalize one-page fast-revision list
- `14:15-16:15` Timed mock exam
  - 90 minutes writing
  - 30 minutes self-check
  - Structure:
    - 1 PEAS/environment question
    - 1 A* numerical
    - 1 heuristics theory question
    - 1 hill climbing / GA / ACO question
    - 1 minimax / alpha-beta question
- `16:15-16:45` Break
- `16:45-18:15` Error-repair session
  - re-solve every mock mistake without notes
- `18:15-19:00` Dinner
- `19:00-20:30` Weak-zone repair
  - if numericals weak: redo A* and minimax
  - if theory weak: redo GA, ACO, NAS, MCTS definitions
- `20:30-21:15` Active recall sprint
  - answer 20 short oral questions closed-book
- `21:15-22:00` Final revision
  - formula sheet
  - PEAS template
  - environment dimension keywords
  - A* conditions
  - hill climbing pitfalls
  - alpha-beta rule
- `22:00-06:30` Sleep

## Exam Morning: 21 June 2026

- `06:30-07:00` Wake and hydrate
- `07:00-08:00` Formula sheet only
- `08:00-08:30` One A* micro-problem and one minimax micro-problem
- `08:30-09:00` PEAS + environment definitions
- `09:00 onwards` Stop learning new material

## Practical Example Activities

- Use the sample paper deck to rehearse grid-world A* by hand.
- Use the assignment PDF to practice PEAS and task-environment classification from real course phrasing.
- Use `A_star_implementation.ipynb` only after solving the numerical manually.
- Use `HillClimb.ipynb` after you can predict the next move without running it.
- Use the visual lab in this repo for:
  - changing heuristic terms in A*
  - observing hill-climbing neighbor evaluation
  - tracing minimax and alpha-beta decisions

## Active-Recall Questions

1. What makes an agent rational?
2. How is PEAS different from problem formulation?
3. Why is chess fully observable but poker partially observable?
4. What is the difference between `g(n)` and `h(n)`?
5. Why can greedy best-first search fail to find an optimal path?
6. Under what condition is A* optimal?
7. What is an admissible heuristic?
8. What is a consistent heuristic?
9. Why does local search not care about the path?
10. What causes hill climbing to get stuck?
11. How does local beam search differ from hill climbing?
12. What are chromosome, fitness, crossover, and mutation?
13. What do pheromone and evaporation mean in ACO?
14. Why is NAS low priority for a beginner with 2 days left?
15. What is a utility function in game playing?
16. Why does minimax alternate max and min?
17. What are `alpha` and `beta`?
18. When can alpha-beta prune a branch?
19. What is the intuition behind MCTS?
20. Which mid-sem topics look most numerical from the local material?

## Topic Mastery Checks

### You can mark a topic as mastered only if you can do all of these

- Agents and PEAS:
  - create PEAS for a new scenario in under 4 minutes
  - classify 6 environment dimensions with reasons
- A*:
  - compute `g/h/f`
  - expand nodes in correct order
  - explain admissibility and consistency in words
- Hill climbing:
  - evaluate neighbors and explain local maxima / plateau / ridge
- GA:
  - explain one full generation step with a concrete encoding
- ACO:
  - explain transition probability and pheromone update intuitively
- Minimax:
  - solve a tree cleanly
  - mark at least one alpha cut and one beta cut correctly

## Timed Mock Rules

- Use blank paper only.
- No slides or notes during the 90-minute write.
- After finishing, mark:
  - conceptual errors
  - arithmetic errors
  - skipped steps
  - poor answer presentation

## Answer-Writing Strategy

- For PEAS/environment questions:
  - write headings exactly as `Performance Measure`, `Environment`, `Actuators`, `Sensors`
  - give one-line justifications for environment labels
- For search numericals:
  - draw the search tree neatly
  - label each node with `g`, `h`, and `f`
  - show the open-list decision each step
- For derivations:
  - define every symbol before using it
  - write the condition first, then the implication
- For algorithm questions:
  - give intuition, steps, example, limitation
- For game trees:
  - write MAX/MIN on alternating levels
  - propagate terminal values bottom-up in one color or notation style

## Final Recommendation

For full-marks preparation under a 2-day constraint, spend about:

- `40%` on search and heuristics
- `20%` on PEAS, environments, and problem formulation
- `20%` on local search, GA, and ACO
- `15%` on minimax and alpha-beta
- `5%` on NAS, MCTS, and stochastic games
