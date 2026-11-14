# Evaluation

## What is and is not verified

This package is a text instruction skill. Packaging checks verify file layout, metadata, privacy screening, and archive integrity. These checks do **not** prove that the skill improves a model's task performance.

The installed precursor received limited behavioral smoke tests. This release package does not claim a comparative benchmark, optimality, or any percentage improvement. The synthetic examples are acceptance cases for future evaluation, not claims of completed test runs.

## Suggested comparison

1. Choose representative tasks and keep the target model, tools, settings, inputs, and budget fixed.
2. Run the original prompt and the optimized prompt on the same inputs. Use multiple repetitions where feasible.
3. Judge final outputs against task-specific observable criteria, preferably without showing the evaluator which prompt was used.
4. Record failures, latency, token cost, user intervention, and number of turns, not just subjective prose quality.
5. For staged workflows, include the total cost and handoff errors across all stages.
6. Report sample size and uncertainty. Do not generalize from a few examples to every model or task.

## Minimum behavior checks

- Exact word/count/format constraints remain intact.
- Missing evidence becomes a question or explicit placeholder, never a fabricated fact.
- Draft-only and no-action boundaries remain intact.
- A simple task does not receive needless mandatory stages.
- Added stages have a real dependency and pass/stop gate.
- A failed result receives a targeted correction, not cosmetic prompt expansion.
- Fresh review chats receive the original contract and relevant artifacts.
- Private session details do not leak into unrelated prompts.

Use synthetic fixtures or authorized redacted data when sharing evaluation cases publicly.
