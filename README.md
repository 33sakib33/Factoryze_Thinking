# Factoryze Thinking

Factoryze Thinking is a collection of learning-focused agent skills. The skills make users state important decisions before an AI agent writes code or defines a design.

This is an initiative from [Factoryze](https://factoryze.tech/).

Explainer video: [Video](https://youtu.be/NHWibrvv0E0)

## Why this exists

AI can make software quickly. Speed does not guarantee clear requirements, sound reasoning, or a controlled project.

These skills add constructive friction. They ask the learner to explain the intended result, boundaries, tradeoffs, tests, and finish conditions. The agent can teach general principles and find gaps. It must not make the learner's material decisions for them.

The skills use simple, controlled English. They draw on ASD-STE100 principles without claiming formal ASD-STE100 compliance.

## Included skills

| Skill | Purpose |
| --- | --- |
| [`think-before-code`](./think-before-code/) | Require a user-owned project contract before a substantial software build. |
| [`refine-ui-ux-taste`](./refine-ui-ux-taste/) | Turn the user's visual and interaction preferences into checkable UI and UX rules. |
| [`build-algorithm-reasoning`](./build-algorithm-reasoning/) | Require natural-language algorithm steps, correctness reasoning, complexity reasoning, and tests before implementation. |

Each skill is independent. Install or invoke only the skill needed for the current task.

## Install with the skills CLI

The command is `npx skills add`, not `npx add skills`.

Install interactively from GitHub:

```bash
npx skills add 33sakib33/Factoryze_Thinking
```

List the available skills without installing them:

```bash
npx skills add 33sakib33/Factoryze_Thinking --list
```

Install one skill for Codex:

```bash
npx skills add 33sakib33/Factoryze_Thinking \
  --skill think-before-code \
  --agent codex
```

Install all three skills for Codex, Claude Code, and OpenCode:

```bash
npx skills add 33sakib33/Factoryze_Thinking \
  --skill '*' \
  --agent codex \
  --agent claude-code \
  --agent opencode
```

Add `--global` to make the selected skills available across projects:

```bash
npx skills add 33sakib33/Factoryze_Thinking \
  --skill '*' \
  --agent codex \
  --global
```

The commands above were tested against this repository. The CLI found all three skills and installed them for the selected agents. See the [`skills` CLI documentation](https://github.com/vercel-labs/skills#install-a-skill) for all supported agents and options.

## Manual installation

Clone this repository:

```bash
git clone https://github.com/33sakib33/Factoryze_Thinking.git
cd Factoryze_Thinking
```

Install one skill in a project:

```bash
mkdir -p /path/to/project/.codex/skills
cp -R think-before-code /path/to/project/.codex/skills/
```

Then start a task with an explicit invocation:

```text
Use $think-before-code. Help me plan and build a personal expense tracker.
```

See [Installation](./docs/installation.md) for additional project-level, user-level, and agent-neutral setup.

## Example invocations

```text
Use $think-before-code. I want to build a local-first note application.
```

```text
Use $refine-ui-ux-taste. Help me define the identity of this dashboard before changing its frontend.
```

```text
Use $build-algorithm-reasoning. Help me design a booking-interval merge algorithm before writing Python.
```

Detailed examples are available in [`examples/`](./examples/).

## How the skills divide responsibility

The user owns material decisions. These include product scope, behavior, modules, technology reasons, design identity, algorithm steps, test priorities, and finish checks.

The agent can inspect existing work, teach general principles, expose contradictions, test claims, and implement an approved contract. It must not hide a proposed answer inside a question.

These skills do not prove independent thought. They make reasoning explicit and testable while the skill is active.

## Repository structure

```text
Factoryze_Thinking/
├── think-before-code/
│   ├── SKILL.md
│   ├── agents/openai.yaml
│   └── references/build-contract.md
├── refine-ui-ux-taste/
│   ├── SKILL.md
│   ├── agents/openai.yaml
│   └── references/taste-contract.md
├── build-algorithm-reasoning/
│   ├── SKILL.md
│   ├── agents/openai.yaml
│   └── references/algorithm-contract.md
├── docs/
└── examples/
```

OpenAI describes a skill as a directory containing `SKILL.md` with optional references, scripts, templates, and other resources. See the [official OpenAI skill documentation](https://developers.openai.com/plugins/build/skills).

## Documentation

- [Installation and use](./docs/installation.md)
- [Design principles](./docs/design-principles.md)
- [Testing and validation](./docs/testing.md)
- [Contributing](./CONTRIBUTING.md)

## Project status

The three skill packages pass the Codex skill validator. They have also been tested with simulated learners in empty and existing repositories. Behavioral testing remains important because schema validation cannot prove that an agent will ask good questions.
