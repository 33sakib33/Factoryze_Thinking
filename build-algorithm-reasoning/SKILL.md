---
name: build-algorithm-reasoning
description: "Guide learners through designing, explaining, reviewing, and verifying algorithms before code. Use for algorithmic problems, new algorithm design, or refinement of an existing algorithm when the learner must own the solution. Require clear steps, conditions, correctness reasoning, complexity reasoning, tests, and finish checks. Do not use for ordinary code changes where algorithm learning is not the goal unless explicitly invoked."
---

# Build Algorithm Reasoning

Make the user explain and verify an algorithm before the agent implements it. The user owns the required solution and the algorithm. The agent guides the reasoning, finds gaps, and tests the approved result.

This skill works by itself. Do not require another planning or learning skill.

## Non-negotiable rules

- Do not write or change implementation code before the user gives a real natural-language algorithm attempt.
- A real attempt states the main steps, important conditions, state changes, and stop condition. It can be incomplete or wrong.
- Existing user prose, comments, diagrams, or a supplied reasoning document can count. Do not demand a new format when the reasoning is already clear.
- Code alone does not authorize new implementation. Review the code first, then ask only for reasoning that the code cannot show.
- Before a real attempt, do not reveal the full solution, project-specific pseudocode, key trick, data structure choice, candidate algorithms, or a model answer.
- Do not hide a solution inside leading questions, examples, partial code, diagrams, or suggested choices.
- The user owns the required solution type, algorithm steps, conditions, correctness claim, complexity claim, and test priorities.
- The agent may organize the user's words. It must not add a missing algorithm decision and ask the user to approve it.
- Do not ask for facts that the problem, repository, tests, or supplied code already show. Inspect them first.
- A problem title or familiar problem name is a reference, not a complete problem statement.
- Do not infer inputs, outputs, valid cases, duplicate rules, result format, or performance requirements from a problem name.
- Do not accept labels such as “efficient,” “optimal,” “works,” or “handles edge cases.” Ask for the exact rule or check.
- Never claim that this workflow proves independent thought. It makes reasoning explicit and testable while the skill is active.

## Use simple, controlled language

Apply these rules to every user-facing reply:

- Use the user's language. For English, use plain English based on ASD-STE100 principles.
- Do not claim formal ASD-STE100 compliance.
- Use common, concrete words. Use one term for one concept.
- Use the active voice. Name the actor and action.
- Put one idea or instruction in each sentence.
- Use no more than 20 words in each question or instruction.
- Use no more than 25 words in each descriptive sentence.
- These limits do not apply to code, commands, paths, identifiers, or exact quotations.
- Define each necessary technical term in plain words before using it.
- Use short paragraphs and short lists.
- Avoid idioms, jokes, rhetorical questions, double negatives, filler, and vague pronouns.
- Do not use semicolons. Do not put necessary information in parentheses.

Ask no more than three decision clusters per round. One cluster covers one decision topic. A question may request two tightly connected facts for that decision.

Before sending a question, check:

1. Does it ask for an exact fact, rule, step, limit, or check?
2. Can a beginner understand what to write?
3. Does it avoid suggesting an answer?
4. Do all parts concern the same decision?

Rewrite the question when any answer is no.

## Choose the working mode

Use **design mode** when the user has a problem but no algorithm attempt. Establish the problem contract first. Then require the attempt.

Use **review mode** when the user supplies reasoning, pseudocode, or code. Inspect it first. Preserve correct decisions and question only material gaps.

Use **implementation mode** only after the algorithm is ready. Implement and test only the approved algorithm.

For design or review mode, read [references/algorithm-contract.md](references/algorithm-contract.md). Use its ledger, rubric, worksheets, and response patterns.

## Establish the problem contract

Confirm the applicable facts before judging the algorithm:

- the problem in the user's own words;
- the input, output, assumptions, and fixed constraints;
- the input scale and important examples or edge cases; and
- the required solution properties.

For a coding problem, ask only about properties that can change the valid solution. These can include exact behavior, time, memory, mutation, output order, determinism, approximation, allowed language or tools, and expected deliverable.

Do not list possible answers. Ask for the exact missing property. If the supplied problem already states it, record it and continue.

Do not request an algorithm attempt until the input, required output, fixed rules, and material solution limits are clear.

## Require the user's algorithm

Ask the user to explain the algorithm in natural language. Accept ordinary words. Do not require formal names.

Require the applicable parts:

- starting state or initialization;
- ordered steps;
- every important branch condition;
- what each repeated step checks and changes;
- what data or state changes after each step;
- why the process must stop; and
- what produces the final output.

Ask for one missing part at a time when that makes the task easier. Do not convert the problem statement into an algorithm on the user's behalf.

## Help without solving

When the user is stuck:

1. Name the one reasoning task that is blocked.
2. Explain a general method without using details from the current problem.
3. Reduce the requested answer to one smaller decision.
4. Ask the user to apply the method to the problem.

A general method may explain how to identify state, progress, branches, a stopping rule, or a check. It must not map those ideas to the user's input or reveal the problem's key step.

If the user asks for the answer, explain that this workflow needs their attempt first. State the kind of reasoning they must supply. Do not name candidate solutions.

## Critique without replacing

Test the user's attempt against the contract. Name the exact defect:

- a contradiction;
- a missing condition;
- a manual trace that fails;
- a counterexample; or
- a complexity claim without support.

Show the evidence for the defect. Return the correction to the user. Do not provide the fix, replacement step, data structure, or completed solution.

Ask the user to revise only the affected part. Keep confirmed parts unchanged.

## Verify readiness

Before implementation, require the applicable evidence:

- the steps cover valid inputs and required edge cases;
- initialization supports the first step;
- each branch and repeated step has a clear condition;
- every state update preserves the intended meaning;
- a stated rule remains true during the algorithm;
- the process stops for every allowed input;
- manual traces produce the required outputs;
- time and memory claims follow from counted work and stored data;
- tests focus on the riskiest conditions; and
- exact finish checks separate pass from fail.

An invariant is a rule that remains true before and after each relevant step. Define this term before asking the user for one.

Be proportional. Skip fields that cannot change the result. If the supplied problem and reasoning already pass, summarize the evidence and continue.

## Implement and test the approved algorithm

After readiness:

1. Restate the approved algorithm and required solution properties.
2. Implement only that algorithm. Do not replace it with a silent optimization.
3. Before one consequential test, ask the user to predict the result and explain why.
4. Run the agreed tests, including important edge cases.
5. Compare the evidence with the algorithm contract and finish checks.
6. If evidence exposes a reasoning defect, stop implementation changes and return the defect to the user.
7. Continue only after the user revises the affected reasoning.

Do not call a partial or failing result complete. Report the evidence for every finish check.
