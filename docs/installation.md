# Installation and use

Each skill in this repository is independent. Copy the complete skill folder, including its `agents/` and `references/` directories.

## Clone the repository

```bash
git clone https://github.com/33sakib33/Factoryze_Thinking.git
cd Factoryze_Thinking
```

## Codex project installation

Project installation limits the skill to one repository. This is the best default when a team wants the same workflow.

From the `Factoryze_Thinking` directory, copy the required skills:

```bash
mkdir -p /path/to/project/.codex/skills
cp -R think-before-code /path/to/project/.codex/skills/
cp -R refine-ui-ux-taste /path/to/project/.codex/skills/
cp -R build-algorithm-reasoning /path/to/project/.codex/skills/
```

The resulting project structure is:

```text
your-project/
└── .codex/
    └── skills/
        ├── think-before-code/
        ├── refine-ui-ux-taste/
        └── build-algorithm-reasoning/
```

You can install only one or two folders. The skills do not depend on each other.

## Codex user installation

User installation makes a skill available across your Codex projects.

```bash
mkdir -p ~/.codex/skills
cp -R think-before-code ~/.codex/skills/
cp -R refine-ui-ux-taste ~/.codex/skills/
cp -R build-algorithm-reasoning ~/.codex/skills/
```

Use project installation when a workflow applies only to one codebase. Use user installation when you want the learning workflow in many projects.

## Use a skill

Invoke a skill by name when you want predictable activation:

```text
Use $think-before-code. Help me build a study planner.
```

```text
Use $refine-ui-ux-taste. Help me define the UI identity for this checkout flow.
```

```text
Use $build-algorithm-reasoning. Help me solve this graph problem without giving me the algorithm.
```

Codex can also select a skill from its name and description when the request clearly matches it.

## Use the skills in another project without copying

For local development, create a symbolic link from the target project to this clone:

```bash
mkdir -p /path/to/project/.codex/skills
ln -s /absolute/path/to/Factoryze_Thinking/think-before-code /path/to/project/.codex/skills/think-before-code
```

Use an absolute source path. Repeat the command for each required skill.

## Use with another coding agent

If the agent supports the Agent Skills directory format, copy each complete skill folder into its documented project or user skill directory.

The folder must keep this structure:

```text
skill-name/
├── SKILL.md
├── agents/
└── references/
```

The `SKILL.md` file contains the main instructions. Files under `references/` contain detailed contracts and checklists. The `agents/openai.yaml` file provides Codex interface metadata. Other agents can ignore that metadata when they do not use it.

If an agent does not support skills, keep the folder in the project and give the agent an explicit instruction:

```text
Read and follow ./path/to/skill-name/SKILL.md for this task. Read linked references when the file tells you to.
```

Do not combine all three `SKILL.md` files into one permanent system prompt. Their triggers and readiness rules differ.

## Update an installation

Pull the latest repository version, then replace only the installed skill folders that you want to update:

```bash
git pull --ff-only
```

Review changes before copying them into a shared or global skill directory. Agent instructions can affect file changes, tool use, and project workflow.

## Confirm the installation

Start a new task and invoke the skill explicitly. A substantial vague build should cause the agent to ask for missing decisions before it writes product code.

For a stronger check, use the scenarios in [`../examples/`](../examples/) and the validation process in [Testing](./testing.md).

## Official references

- [Build skills](https://developers.openai.com/plugins/build/skills)
- [Testing Agent Skills Systematically with Evals](https://developers.openai.com/blog/eval-skills)
