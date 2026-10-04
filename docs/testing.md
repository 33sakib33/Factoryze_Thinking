# Testing and validation

Schema validation checks file structure and frontmatter. Behavioral testing checks whether an agent follows the learning workflow.

Both are required for meaningful confidence.

## Validate the skill packages

Use the validator included with Codex's `skill-creator` skill:

```bash
python3 /path/to/skill-creator/scripts/quick_validate.py think-before-code
python3 /path/to/skill-creator/scripts/quick_validate.py refine-ui-ux-taste
python3 /path/to/skill-creator/scripts/quick_validate.py build-algorithm-reasoning
```

The validator checks naming, YAML frontmatter, and unfinished scaffold content. It does not prove correct agent behavior.

## Behavioral test matrix

Test each skill with realistic prompts.

| Test type | Expected evidence |
| --- | --- |
| Direct activation | The agent loads the named skill and follows its boundary. |
| Indirect activation | The description activates only for a matching learning task. |
| Incomplete request | The agent asks concrete questions without suggesting answers. |
| Complete brief | The agent records existing decisions and avoids repeated questions. |
| Existing repository | The agent inspects relevant files before asking about known facts. |
| Negative control | An unrelated small task does not trigger a large learning workflow. |
| Refusal to decide | The agent names the blocking decision without inventing it. |
| Implementation | The agent starts only after the applicable readiness checks pass. |

## Skill-specific checks

### Think Before Code

- Start from an empty repository and a vague build request.
- Confirm that no product files change before the contract is ready.
- Require the learner to define modules, technology reasons, order, risky tests, and finish checks.
- Test the fast lane with a small, fully specified edit.

### Refine UI/UX Taste

- Test an empty frontend repository.
- Test an existing frontend with objective defects and weak visual identity.
- Confirm that the agent separates observed defects from subjective taste.
- Confirm that the agent does not recommend styles, colors, layouts, or references before readiness.
- Check the final interface against the learner's viewport, access, state, and interaction rules.

### Build Algorithm Reasoning

- Start from an empty repository and a clear problem.
- Give the agent an incomplete or incorrect natural-language algorithm.
- Confirm that it provides evidence of the defect without supplying the correction.
- Require correctness reasoning, termination, complexity, risky cases, and exact finish checks.
- Confirm that the learner predicts one consequential test before execution.

## Record results

Keep role-labeled transcripts for failed and successful runs. Record:

- the initial prompt;
- relevant repository state;
- all learner and agent messages;
- files changed before readiness;
- commands and tests run;
- passed, failed, and unproven acceptance checks.

Improve a skill from observed failures. Prefer a narrow correction over a new universal rule.
