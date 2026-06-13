# Teaching Workflow

Use this exact sequence unless the user explicitly asks for a smaller slice.

1. Short prerequisite diagnostic
   - Ask or infer 2 to 5 quick checks.
   - If the learner is missing a prerequisite, teach that first.
2. Plain-language intuition
   - Explain what problem the concept solves.
   - Avoid symbols in the first pass.
3. Practical example
   - Pick one concrete scenario from local course material when possible.
4. Diagram or visualization
   - Use ASCII, a table, a simple sketch, or the visual lab.
5. Notation table
   - Define every symbol and variable.
6. Formula derivation
   - Show the logic step by step.
   - State each assumption clearly.
7. Fully worked numerical
   - Show each intermediate calculation.
   - Label `g(n)`, `h(n)`, `f(n)`, utility, fitness, or any other quantity explicitly.
8. Similar learner problem
   - Give a close variant for the learner to try.
9. Error diagnosis
   - Compare the learner attempt with the correct method.
   - Name the mistake pattern, not just the final error.
10. Exam-ready answer
   - Compress the same concept into a concise answer format suitable for writing in the exam.
11. Closed-book mastery check
   - End with a short oral, written, or numerical check.

## Topic-Specific Notes

### PEAS and environment questions

- Use exact headings.
- Give one-line justification for each environment label.

### Search numericals

- Draw the tree or frontier progression.
- Write the selection rule before solving.
- Show why the next node was chosen.

### Hill climbing and optimization

- Separate state, neighbors, and objective value.
- Name failure cases such as local maxima, plateau, and ridge.

### Minimax and alpha-beta

- Mark node type as MAX or MIN at every level.
- Propagate values bottom-up.
- Mark where pruning begins and why.
