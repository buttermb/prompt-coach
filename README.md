<p align="center">
  <img src="assets/hero.png" alt="Prompt Coach — Better prompts. Better next steps." width="100%">
</p>

<p align="center">
  <strong>A prompt strategist, not a thesaurus.</strong><br>
  Turn a rough request into a better first prompt—and the right next steps.
</p>

<p align="center">
  <a href="LICENSE"><img alt="MIT License" src="https://img.shields.io/badge/License-MIT-CBFF00?style=flat-square&labelColor=0B1224"></a>
  <img alt="Plain Markdown" src="https://img.shields.io/badge/Built_with-Markdown-F7F4E8?style=flat-square&labelColor=0B1224">
  <img alt="No API key required by this package" src="https://img.shields.io/badge/API_key-Not_required-CBFF00?style=flat-square&labelColor=0B1224">
</p>

<p align="center">
  <a href="#quick-start">Quick start</a> · <a href="#install">Install</a> · <a href="EXAMPLES.md">Examples</a> · <a href="EVALUATION.md">Evaluation</a> · <a href="CONTRIBUTING.md">Contribute</a>
</p>

---

## Same model. A better approach.

Sometimes a model's first answer is merely okay. A well-targeted follow-up can make it much more useful. But repeating “make it better” is not a strategy—and three prompts are not always better than one.

**Prompt Coach helps choose the smallest useful workflow for the actual task.** It improves the starting instructions, recommends task-specific follow-ups when they matter, and adapts those follow-ups to the output you bring back.

It optimizes for **the final result**, not longer prompts or fancy language. Keep your chosen model. Keep your intent. Improve the approach.

> Prompt Coach is a portable Markdown skill, not a hosted app or a model. It does not execute your underlying task by default, and it cannot guarantee that a cheaper model will match a more capable one.

## Quick start

After loading the skill, paste:

```text
Use Prompt Coach.

Task: [what I want to accomplish]
Model: [the model I plan to use, if known]
Good looks like: [what would make the result useful]
Constraints: [anything it must preserve or avoid]

Give me the best starting prompt. Include up to two follow-ups only
if they would materially improve the result.
```

**Already have a weak answer?** Bring the original request and the output:

```text
Use Prompt Coach. Here is my original request and the model's answer.
Give me the next prompt that fixes the biggest remaining weakness.
Preserve what already works. If it is good enough, tell me to stop.
```

You do not need to fill every field. A rough idea is enough to begin; genuinely missing inputs are flagged rather than invented.

## What you get

| Situation | Coach's approach |
| --- | --- |
| A straightforward rewrite | One concise, copy-ready prompt |
| A task with a meaningful dependency | Two or three stages, with a purpose for each |
| A promising but weak first answer | A targeted follow-up based on the actual output |
| Missing sources, files or access | A precise gap, not fabricated context |
| A result that meets the goal | Stop instead of polishing forever |

### The working loop

**Understand → Frame → Try → Inspect → Improve only what matters**

1. Identify the desired outcome and likely failure point.
2. Preserve constraints and define observable success checks.
3. Write the first usable prompt.
4. Add stages only when their expected benefit justifies the extra work.
5. Use the actual result to fix the largest remaining gap.

The default response is short: an approach recommendation, a starting prompt, and at most two conditional follow-ups. Complex workflows can be longer when the task truly needs it.

## Install

### Option A · Any chat model, no installation

1. Open [`prompt-coach/SKILL.md`](prompt-coach/SKILL.md).
2. Copy the instructions below the YAML header (the first `---` block) into a fresh conversation.
3. Add your task using the quick-start template above.

This is manual use for that conversation, not a persistent install. Your chat provider's normal limits and charges still apply.

### Option B · A compatible skill-enabled assistant

1. Download this repository using **Code → Download ZIP**, or clone it:
   ```sh
   git clone https://github.com/buttermb/prompt-coach.git
   ```
2. Import or copy the inner `prompt-coach/` folder using your assistant's supported skill-installation flow. Keep `SKILL.md` inside it.
3. Start or refresh the session if your host requires it, then invoke **Prompt Coach** by name or with the host's skill selector.

Invocation syntax and install locations vary by product. Some hosts use `$prompt-coach`, others use a skill menu or natural language. This repository does not register itself with any platform or promise automatic loading in every chat mode.

<details>
<summary><strong>Repository layout</strong></summary>

```text
prompt-coach/
├── README.md
├── LICENSE
├── EXAMPLES.md
├── EVALUATION.md
├── CONTRIBUTING.md
├── assets/
│   ├── hero.png
│   └── logo.png
└── prompt-coach/
    ├── SKILL.md
    └── agents/openai.yaml
```

`agents/openai.yaml` is optional UI metadata for compatible hosts. The core instructions live in `SKILL.md`.
</details>

## Designed for real work

- **Writing:** keep the correct audience, context and natural voice.
- **Coding:** respect current state, ownership, evidence and action boundaries.
- **Research:** separate observations from assumptions and require source-grounded checks.
- **Visual briefs:** specify references, exact copy, dimensions and final deliverables.
- **Estimates:** preserve units, time windows and the actual cost basis.

See [six synthetic examples](EXAMPLES.md) for inputs and expected behavior.

## Honest limits

Prompting cannot replace missing evidence, permissions, tools or model capabilities. Extra turns can add cost, latency and mistakes. Self-review is not independent verification.

The skill has received limited behavioral smoke testing, **not a comparative performance benchmark**. No percentage improvement or model-equivalence claim is made. [Evaluation guide →](EVALUATION.md)

## Privacy & permissions

This package has no API client, telemetry, dependencies or automatic uploads. Your chosen model/service still processes what you submit. Do not include secrets or unnecessary private history. Improving a prompt does not grant permission to send messages, spend money, publish or change systems.

## Contribute

Useful improvements start with a real failure, not more rules. Share a minimal synthetic or redacted example, the expected outcome and what went wrong. See [CONTRIBUTING.md](CONTRIBUTING.md).

## License

[MIT](LICENSE). Original project branding was created with AI assistance. No affiliation with or endorsement by model providers is implied.
