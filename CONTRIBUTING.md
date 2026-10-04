# Contributing

Contributions should preserve the learning goal: make reasoning explicit without making material decisions for the learner.

## Propose a change

Describe:

1. the observed failure or missing behavior;
2. the exact skill and mode affected;
3. a realistic prompt that reproduces the issue;
4. the expected behavior;
5. why the change does not constrain unrelated tasks.

Prefer narrow corrections supported by a transcript. Do not add a universal rule for a single stylistic preference.

## Modify a skill

- Keep the required `name` and `description` in `SKILL.md` frontmatter.
- Keep the description focused enough for reliable activation.
- Put shared constraints and routing in `SKILL.md`.
- Put detailed worksheets and mode-specific material in `references/`.
- Preserve user ownership and existing permission boundaries.
- Keep user-facing questions concrete and free of suggested answers.
- Keep each skill independent unless a real dependency is required.

## Validate

Run the Codex `skill-creator` validator for every changed skill:

```bash
python3 /path/to/skill-creator/scripts/quick_validate.py path/to/skill
```

Then run at least one realistic behavioral test. Include a negative or incomplete case when the trigger or questioning behavior changed.

See [Testing and validation](./docs/testing.md) for the recommended test matrix.

## Pull requests

A pull request should include:

- a short reason for the change;
- the affected skill files;
- validation output;
- a role-labeled behavioral transcript;
- any remaining unproven behavior.
