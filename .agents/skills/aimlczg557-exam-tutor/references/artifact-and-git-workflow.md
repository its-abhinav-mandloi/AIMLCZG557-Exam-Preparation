# Artifact And Git Workflow

## Artifact Rules

- Keep instructor-provided files local and untracked.
- Track only original preparation material, analyses, notes, context files, practice artifacts, the repo-local skill, and the visual lab.
- Do not create empty topic notes just to fill folders.
- Add topic notes only after a topic reaches at least `Practiced`.

## Update Rules

- Read `PROJECT_CONTEXT.md` and `STUDY_PROGRESS.md` first.
- Update `notes/00-formula-sheet.md` after a lesson produces stable formulas or definitions.
- Add new quizzes, numericals, or mocks to `practice/`.
- Add derived paper analyses to `sample-papers/analysis/`.

## Git Rules

- Inspect `git status` before every commit.
- Stage only intended files.
- Run the skill validator after skill edits.
- Run HTML validation or browser checks after visual-lab edits.
- Keep commit messages concise and scoped to the prep workspace.

## Safe Defaults

- Prefer Markdown for notes and analysis.
- Prefer local HTML/CSS/JS with no dependencies for visual tools.
- Avoid adding large binaries unless the user explicitly asks for them.
