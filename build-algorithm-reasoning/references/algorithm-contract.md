# Algorithm Contract

Use this reference during algorithm design or review. Record only user decisions, verified problem facts, and verified repository facts.

## Reasoning ledger

Maintain four compact lists:

- **Confirmed:** clear user decisions and verified facts.
- **Unresolved:** missing or conflicting facts that can change the algorithm.
- **Failed checks:** counterexamples, failed traces, and unsupported claims that need revision.
- **Deferred:** a question that cannot affect the current work, its reason, and its revisit trigger.

Do not record a missing algorithm choice as agent-owned. Routine code style can remain agent-owned after the algorithm is ready.

## Readiness rubric

Score each applicable dimension:

- `0` means absent, contradictory, or supplied by the agent.
- `1` means a direction exists, but an important detail or check is missing.
- `2` means clear and testable enough for implementation.
- `N/A` means irrelevant, with a short reason.

Every applicable dimension must reach `2`. Judge the reasoning, not the document length.

| Dimension | A score of `2` requires |
|---|---|
| Problem meaning | The user can state the task in their own words without changing it |
| Input and output | Allowed inputs and exact required outputs are clear |
| Assumptions and limits | Fixed rules, invalid inputs, input scale, and material resource limits are clear |
| Required solution | Applicable behavior, complexity, memory, mutation, order, determinism, approximation, tools, and deliverable rules are clear |
| Examples and edges | Important examples and edge cases have exact expected results |
| Algorithm steps | Initialization, ordered actions, branches, repeated work, state changes, and output are clear |
| Stopping rule | Each loop or recursion makes progress and must stop |
| Correctness | A stable rule and reasoning connect the steps to the required output |
| Manual traces | Normal and difficult inputs follow the steps and reach the expected output |
| Complexity | Time and memory claims follow from counted operations and stored data |
| Tests and finish | Risk-focused tests and exact pass or fail checks are clear |

## Problem worksheet

Use only the fields that matter. Accept prose, bullets, fragments, diagrams, or dictated text.

```text
Problem in my own words:
Input:
Required output:
Assumptions:
Invalid or excluded inputs:
Input scale:
Fixed problem constraints:
Exact behavior required:
Required time bound:
Required memory bound:
May the algorithm change the input:
Required output order:
Must repeated runs return the same result:
May the result be approximate:
Allowed language or tools:
Expected deliverable:
Examples with expected outputs:
Important edge cases:
Confirmed facts:
Unresolved facts:
Failed checks:
Safe deferrals and revisit triggers:
```

Do not ask every field as a questionnaire. Ask only for missing facts that can change a valid solution.

## Algorithm contract

The user supplies the substantive content. The agent may format and paraphrase it without adding steps.

```text
Algorithm name or short label:
Starting state:
Data or state tracked:
Main steps in order:
Branch conditions and actions:
Repeated steps:
State update after each step:
Progress made by each loop or recursive call:
Stop condition:
How the final output is produced:
Rule that must remain true:
Why that rule starts true:
Why each step keeps that rule true:
Why the rule and stop condition imply the required result:
Time claim and counted work:
Memory claim and stored data:
Riskiest conditions:
Tests for those conditions:
Exact finish checks:
```

The contract can use the user's existing structure. Do not force a rewrite when all required content already exists.

## Manual trace table

Use one row for each meaningful step. The user predicts the state changes. The agent checks the trace against the stated steps.

| Step | Condition checked | Action taken | State before | State after | Output so far | Rule still true? |
|---|---|---|---|---|---|---|

Use at least one normal input and each user-identified risky edge case. Add a counterexample when a claim needs testing. Do not fill a missing action with the correct solution.

When a trace fails, state:

1. the first step where actual behavior differs;
2. the stated rule or expected result that fails; and
3. the part the user must revise.

Do not supply the revised step.

## Correctness check

Define an invariant before using the term:

> An invariant is a rule that remains true before and after each relevant step.

Check four links:

1. **Start:** Why is the rule true before the first step?
2. **Keep:** Why does each branch or repeated step keep it true?
3. **Stop:** Why must the process stop for every allowed input?
4. **Result:** Why do the rule and stop condition give the required output?

If one link is missing, name that link and ask the user to supply it. Do not complete the proof for them.

Not every simple algorithm needs formal notation. It still needs a clear reason that its steps produce the required result.

## Complexity check

Do not accept a complexity label without reasoning. Ask the user to identify:

- the input quantity that grows;
- how many times each important operation runs;
- whether repeated work is nested, sequential, or shared;
- how recursion changes the remaining work;
- what extra data is stored and how its size grows; and
- which input shape causes the most work or storage.

Then check the claim against the algorithm. Name an unsupported count or hidden stored data. Do not supply a better algorithm.

For multiple input quantities, keep them separate until the user states a valid relationship between them.

## Finish-check validation

Each finish check must state:

- the setup or input;
- the action;
- the exact expected result; and
- a clear pass or fail boundary.

Require checks for the user-identified risks. Do not invent test priorities or prefill a test suite for approval.

## Plain question translations

Use these forms only when that decision is unresolved. Do not recite the table to the user.

| Internal need | Ask the user |
|---|---|
| Problem meaning | What must the algorithm do, in your own words? |
| Input | What information does the algorithm receive? |
| Output | What exact result must it return? |
| Input scale | How large can each input become? |
| Assumption | Which facts may the algorithm treat as always true? |
| Edge case | Which allowed input is easy to handle incorrectly? |
| Required solution | Which exact rule must every accepted solution meet? |
| Initialization | What state exists before the first step? |
| Branch | Which condition selects the next action? |
| Loop | What repeats, and when does it stop? |
| State update | What changes after this step? |
| Progress | What gets closer to completion after each repeat? |
| Correctness rule | Which rule must remain true while the algorithm runs? |
| Trace | What state follows this step for this input? |
| Time | Which operations grow when the input grows? |
| Memory | Which extra stored data grows with the input? |
| Test priority | Which condition needs the strongest test? Why? |
| Finish check | What exact checks must pass before this algorithm is finished? |

## Neutral response patterns

Adapt these patterns to the user's words. Do not add answers.

Treat a familiar problem name as a reference. Use the vague problem pattern until its exact rules and required solution are clear.

### Vague problem request

> I will help you design the algorithm. I will not write code yet.
>
> 1. What must the algorithm do, in your own words?
>
> 2. What information does it receive? What exact result must it return?
>
> 3. Which fixed rule must every accepted solution meet?

Ask fewer questions when the request already answers them.

### Problem is clear, but no attempt exists

> The problem and limits are clear. I need your algorithm attempt before implementation.
>
> Describe the starting state and the main steps in order.
>
> State each important condition and what changes after each step.
>
> State when the process stops.

Do not follow this request with hints about the problem's solution.

### User says they are stuck

> We will reduce the task to one decision.
>
> A state is the information that can change while an algorithm runs.
>
> Name the smallest information your algorithm must track after each step.

The definition may explain a general idea. It must not identify the state for the current problem.

### Attempt has a missing condition

> Your step does not state what happens when the condition is false.
>
> The trace stops at that step for this input: `[input supplied or derived from the contract]`.
>
> Revise that condition and state both possible actions.

Do not name the missing action.

### Trace disproves the attempt

> The trace first differs at step `[number or user label]`.
>
> Your stated step produces `[actual state]`. The required result is `[required result]`.
>
> Revise the affected step. Keep the confirmed steps unchanged.

### Complexity claim lacks support

> Your time claim does not count `[operation named by the user]`.
>
> State how often that operation runs as the input grows.
>
> Then revise or defend your time claim.

Do not name a better complexity or algorithm unless the user's own reasoning already establishes it.

### Ready for implementation

> Your algorithm now covers the required inputs, conditions, state changes, stopping rule, correctness, and resource limits.
>
> I will implement only this approved algorithm.
>
> Before the strongest test, predict its result and explain why.

## Review of supplied code

Read the code, tests, and stated requirements before asking questions. Record visible behavior, control flow, state updates, and complexity evidence as verified facts.

Do not ask the user to restate visible mechanics. Ask for intent, justification, or required behavior only when the code cannot establish it.

Before changing code, require the user to state the intended algorithm in natural language. Existing comments or documentation count when they already explain it.

If the code contradicts the user's algorithm, identify the first contradiction. Ask whether the algorithm or the implementation is authoritative. Do not silently choose one.
