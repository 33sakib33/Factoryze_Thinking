# Design principles

## Constructive friction

The skills slow down only decisions that can materially change the result. They do not require long essays or professional vocabulary.

A learner can answer with short sentences, bullets, examples, diagrams, or dictated text. Clarity matters more than format.

## User ownership

The user owns decisions that define the product or solution. The agent must not write an answer and ask the user to approve it.

The agent can:

- inspect supplied files;
- record decisions already made by the user;
- teach a general reasoning method;
- identify a contradiction or missing boundary;
- provide a counterexample to a claim;
- implement and test an approved contract.

Before readiness, the agent must not:

- choose the user's product scope;
- propose features as answers to its own questions;
- select the product's visual identity;
- supply the missing algorithm step;
- select material technologies for the user;
- invent finish criteria and ask for approval.

## Concrete questions

Questions ask for an exact person, action, rule, limit, reason, or check. They avoid vague phrases such as “in what situation” and “what observable result.”

The skills use common words and short sentences. A necessary technical term is defined before the learner must use it.

## Requirements before technology

Libraries, frameworks, models, providers, and runtimes follow the system's requirements and boundaries.

For each material technology, the learner states:

- its exact name when that detail changes the result;
- its job and module;
- where it runs;
- how the system connects to it;
- why it fits a confirmed requirement;
- which risk, cost, or limit it adds.

## Checkable completion

“Looks good,” “works,” and “tests pass” are not finish checks.

A useful finish check states:

1. the setup;
2. the action;
3. the expected result;
4. the pass or fail boundary.

## Proportional effort

The skills should not turn a small change into a large planning process.

`think-before-code` includes full, delta, fast, and bounded experiment lanes. The UI/UX and algorithm skills also ask only for decisions that can change the current result.

## Independent skills

The three skills share a philosophy, but each one can run alone.

- Use `think-before-code` for complete software planning and controlled delivery.
- Use `refine-ui-ux-taste` when the learning goal is a distinct and checkable interface identity.
- Use `build-algorithm-reasoning` when the learner must own and prove an algorithm.
