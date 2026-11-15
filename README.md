<p align="center">
  <img src="hero.png" alt="Prompt Coach: Better prompts. Better next steps." width="100%">
</p>

<p align="center">
  <strong>Get more out of the model you're already using.</strong><br>
  A better starting prompt, plus follow-ups when they actually help.
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

## Why I made this

The idea is pretty simple. You give a model a prompt, get something back, and it's just okay. Then two or three follow-ups later, the output is actually good. Same model, much better result.

I wanted a way to get there with less guessing. Something that looks at what I'm trying to do and says: use this prompt first, then this follow-up if you need it. Or just do it in one shot if a better starting prompt is enough.

That's Prompt Coach.

**The goal is a better final result with the least extra work.** Not turning every request into a giant prompt or making you go through three rounds for no reason.

It's a Markdown skill you give to an assistant. It helps you write the prompts; it doesn't do the underlying task by default. You keep using whichever model you want.

## Quick start

Load the skill using one of the [install options below](#install), then paste this:

```text
Use Prompt Coach.

Task: [what I want to accomplish]
Model: [the model I plan to use, if known]
Good looks like: [what would make the result useful]
Constraints: [anything it must preserve or avoid]

Give me the best starting prompt. Include up to two follow-ups only
if they would materially improve the result.
```

You don't have to fill out every field. Start with what you have.

Already tried a prompt and don't like the answer? Bring both back:

```text
Use Prompt Coach. Here is my original request and the model's answer.
Give me the next prompt that fixes the biggest remaining weakness.
Preserve what already works. If it is good enough, tell me to stop.
```

That second part matters. A follow-up based on the actual output is more useful than guessing what will go wrong before you've even tried it.

## What it gives you

- **One prompt** when the task can reasonably be done in one shot.
- **Two or three steps** when splitting the work has a real purpose.
- **A targeted next prompt** when you bring back an answer that needs work.
- **A clear missing input** when the problem is missing context, files or access.
- **A stopping point** when the result already does what you need.

The default is short: a recommendation, a copy-ready starting prompt, and up to two conditional follow-ups. More steps are possible for genuinely complex work, but I don't want extra steps to be the default.

Basically, fix the biggest thing that's holding the output back. Keep what works. Then stop.

## Install

### Option A · Any chat model, no installation

1. Open [`prompt-coach/SKILL.md`](prompt-coach/SKILL.md).
2. Copy the instructions below the YAML header (the block between the first two `---` lines) into a fresh conversation.
3. Add your task using the quick-start template above.

This is manual use for that conversation, not a persistent install. Your chat provider's normal limits and charges still apply.

### Option B · A compatible skill-enabled assistant

1. Download this repository using **Code → Download ZIP**, or clone it:
   ```sh
   git clone https://github.com/buttermb/prompt-coach.git
   ```
2. Import or copy the inner `prompt-coach/` folder using your assistant's supported skill-installation flow. Keep `SKILL.md` inside it.
3. Start or refresh the session if your host requires it, then invoke **Prompt Coach** by name or with the host's skill selector.

Invocation syntax and install locations vary by product. Some hosts use `$prompt-coach`, others use a skill menu or natural language. This repo doesn't register itself with a platform or automatically load in every chat mode.

<details>
<summary><strong>Repository layout</strong></summary>

```text
prompt-coach/
├── README.md
├── LICENSE
├── EXAMPLES.md
├── EVALUATION.md
├── CONTRIBUTING.md
├── hero.png
├── logo.png
└── prompt-coach/
    ├── SKILL.md
    └── agents/openai.yaml
```

`agents/openai.yaml` is optional UI metadata for compatible hosts. The core instructions live in `SKILL.md`.
</details>

## A few things to try it on

Writing, code, research, visual briefs, estimates. The useful details change with the task: audience and voice for writing, existing code and boundaries for coding, sources for research, references and dimensions for visual work.

I've included [six made-up examples](EXAMPLES.md) so you can see the intended behavior without anyone's private conversations being in the repo.

## What I'm not claiming

I want this to help you get more from the model you're already using, including cheaper models. That doesn't mean it can make every model equally capable. A better prompt can't supply missing evidence, tools or permissions.

Extra rounds can cost more and sometimes make things worse. And asking a model to check itself isn't independent verification.

This has had limited behavioral smoke testing, **not a comparative benchmark**. There are no measured savings or model-equivalence claims here. The [evaluation guide](EVALUATION.md) lays out how to compare results.

## Privacy and permissions

There's no API client, telemetry, dependencies or automatic uploading in this package. Your chosen assistant still processes whatever you paste into it, so leave secrets and unnecessary private history out.

Improving a prompt also doesn't give an assistant permission to send messages, spend money, publish things or change your systems.

## Want to improve it?

Send a small example of where it falls short, what you expected, and what happened. Made-up or properly redacted examples only, please.

I'd rather fix a real failure than keep adding rules just because they sound useful. [Contribution notes](CONTRIBUTING.md).

## License

[MIT](LICENSE). The original branding was made with AI assistance. This project isn't affiliated with or endorsed by any model provider.
