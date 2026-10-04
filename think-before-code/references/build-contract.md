# Build Contract

Use this contract for the current increment, not every imagined future feature. Eliminate unresolved high-impact ambiguity; deliberately defer only decisions that cannot change the current increment.

## Decision ledger

Maintain four compact lists throughout planning:

- **Confirmed:** explicit user decisions and verified repository facts.
- **Unresolved:** material decisions that block readiness.
- **Deferred:** a named unknown, why it is safe to defer, who or what will resolve it, and its revisit trigger.
- **Agent-owned:** routine, reversible local mechanics inside user-approved constraints and acceptance behavior.

Features, UX behavior, scope, data ownership, architecture, boundaries, material technologies, technology reasons, module order, tests, acceptance, and finish checks never become agent-owned merely because the user says “use sensible defaults.”

## Readiness rubric

Score each applicable dimension:

- `0` — absent, contradictory, vague, or being invented by the agent;
- `1` — direction exists, but a consequential choice or testable detail is missing;
- `2` — explicit and testable enough for the current increment; or
- `N/A` — irrelevant, with a stated reason.

Every applicable dimension must reach `2` before implementation. Judge substance, not document length or checkbox count.

| Dimension | A score of `2` requires |
|---|---|
| User and task | Who will use it and what that person must do |
| Steps and behavior | How the user starts, each important step, the result, and what happens when a step fails |
| Included work and limits | What this version includes, what it leaves out, and which fixed limits it follows |
| Rules and checks | Important rules plus concrete examples that clearly pass or fail |
| Data and outside systems | Who controls each item of data, which outside systems connect, who may access data, and which technical limits matter |
| Module plan | Separate modules with clear jobs, owned work, exchanged information, needed modules, and isolated tests |
| Material technologies | Exact names, affected modules, run location, provider or runtime, reasons tied to confirmed limits, and new tradeoffs |
| Build order and risk | User-owned order, reasons for that order, risky assumptions, and strongest test areas |
| Finish checks | Exact checks that another person can use to decide whether each module is finished |

## Project worksheet

Accept answers in prose, bullets, examples, fragments, or diagrams. Do not turn the worksheet into mandatory paperwork when the information already exists elsewhere.

```text
Project and current version:
Who will use it:
What the user must do:
Where or when they will use it, only if this changes the design:
What the first version must let the user complete:
What this version must include:
What this version must leave out:
Fixed limits:
Steps the user takes:
What can fail and what must happen next:
Rules and examples that clearly pass or fail:
Decisions about data, outside systems, security, privacy, or accessibility:
Material technologies and exact versions or model names used by code:
Modules that use each technology:
Where each technology runs and how the product connects:
Provider or local runtime, when applicable:
Requirement or fixed limit behind each choice:
New cost, risk, or limit from each choice:
Confirmed decisions:
Agent-owned reversible choices:
Unresolved decisions:
Safely deferred decisions and revisit triggers:
```

## Module map

Create the map for the approved increment before implementation. The user must supply the decomposition and sequence. The agent may normalize the user's words into the table but must not create, split, merge, order, or name modules on the user's behalf.

| ID | One clear job | Work and data it controls | Information it receives and returns | What it needs | Order and reason | Strongest test focus | Exact finish checks |
|---|---|---|---|---|---|---|---|

Do not supply sequencing strategies. Ask the user why the first module must precede the second, what it unlocks or proves, and what evidence would show that the order was sound. Evaluate the stated reasoning without providing a better order.

## Technology decision record

Use one record for each material technology. Do not create records for minor, interchangeable helper tools.

```text
Technology or model:
Exact version or model name used by code:
Module and job:
Where it runs:
How the product connects to it:
Inference provider, local runtime, or other operator:
Requirement or fixed limit behind the choice:
Why it fits that requirement or limit:
New cost, risk, or limit:
How the user will check that it fits:
```

A material choice cannot pass with only a product name. The user must connect the choice to a confirmed requirement or fixed limit.

If a choice conflicts with the contract, state the conflict. Ask the user to revise the choice or accept the stated tradeoff.

## Active module contract

The user supplies every substantive field before the next module is implemented. The agent may format the answers without adding content.

```text
Module:
Its one clear job:
Work it must do:
Work it must not do:
Data it controls:
Information it receives:
Information it returns:
Errors it can return:
Other parts that need it:
Other parts it needs:
Rules that must always stay true:
What can fail or reach a limit:
Other limits that affect its design:
Material technologies it uses:
Reason for each material technology:
Where each runs and how this module connects:
Why it has this place in the build order:
Behavior that needs the strongest tests:
Examples that clearly pass or fail:
Exact checks that must pass before it is finished:
```

Challenge the contract when responsibilities overlap, interfaces leak internal details, dependencies cycle, failure ownership is unclear, or the module cannot be tested independently. Explain the concrete consequence and ask the user to revise or consciously accept the tradeoff.

## Finish checklist validation

The user authors each module's finish checklist. Do not present a prefilled checklist for them to select or approve. Validate each item by asking whether it states:

- what must work;
- the setup or input;
- the action to take;
- the exact result the tester must see or measure; and
- a clear boundary between pass and fail.

Ask neutral questions about any user-identified risk, interface, failure case, integration, or quality constraint that lacks completion evidence. Do not invent checklist items or testing priorities.

## Calibration rules

- When the user supplies a vague claim, ask for the exact condition that another person can check. Do not supply that condition.
- For a clone, ask who will use it, what they will do, what stays, what changes, and what goes.
- Also ask where it runs, which modules come first, which behavior needs strong tests, and which checks prove completion.
- Ask for material technologies only after the requirements and module needs can guide the choice.
- Do not accept a technology name without the requirement or fixed limit that caused the choice.
- Do not force the user to choose minor helper tools that cannot change the contract.
- When the user's answer is incomplete, identify only the missing category and why it affects implementation. Do not follow the critique with a candidate answer.

## Plain question translations

Use these translations when the internal contract uses an abstract term. Ask only the questions that matter now.

| Internal term | Ask the user |
|---|---|
| Target user | Who will use it? |
| Place | Where will the user do this? |
| Time | When will the user do this? |
| Device | Which device will the user use? |
| User goal | What must the user be able to do? |
| Successful outcome | What must the user be able to complete in this version? |
| Scope | What must this version include? |
| Non-goal | What must this version leave out? |
| Constraint | Which fixed limit must the design follow? |
| User flow | What does the user do first? What happens next? |
| Failure behavior | What can go wrong? What must the product do then? |
| Module responsibility | What one job belongs to this module? |
| Interface | What information does this module receive, return, or reject? |
| Dependency | Which other part must work before this part can work? |
| Invariant | Which rule must always stay true? |
| Material technology | Which exact technology will this module use? |
| Technology reason | Which requirement or fixed limit led to this choice? |
| Run location | Where will it run? |
| Provider or runtime | Which service or local program will run it? |
| Version or model name | Which exact version or model name will the code use? |
| Technology tradeoff | What new cost, risk, or limit will you accept? |
| Test priority | Which behavior needs the strongest tests? Why? |
| Definition of Done | Which exact checks must pass before you call this module finished? |

## LLM technology questions

Use this section only when the approved design includes an LLM.

An inference provider is a remote service that runs a model and returns its output.

A local runtime is software that runs a model on local hardware.

Do not treat local execution and API access as the same decision. A local runtime can also expose an API.

Ask only unresolved questions. Use no more than three decision clusters in one round.

1. Where will the model run? How will the product connect to it?
2. Which exact model name will the code use? Which provider or local runtime will run it?
3. Which requirement or fixed limit led to each choice?

Require separate reasons for the model and the provider or runtime. Do not name candidate models, providers, or runtimes.

## Response pattern for a vague request

Do not recite the entire worksheet. Ask the smallest set that unlocks the next gate. If the user requests one question at a time, ask only the first item and wait.

> The reference does not define your product. I will not start implementation yet.
>
> 1. Who will use the product?
>
> This tells me whose needs the product must serve.
>
> 2. What must that person be able to do in the first version?
>
> This sets the main task for the first version.
>
> 3. What must this version include? What must it leave out?
>
> This sets the boundary for the first version.
>
> I will record your answers. Then I will ask about the next missing decision.

For “Make a Pac-Man clone,” use the product's own words:

> 1. Who will play this game?
>
> This tells me which players the design must serve.
>
> 2. What must the player be able to do in the first version?
>
> This sets the player's main task for the first version.
>
> 3. Which Pac-Man rules must this game keep, change, or leave out?
>
> This defines how this game differs from Pac-Man.

Do not add “in what situation?” Ask separately about place, time, or device only when one changes the design.

For a visual-fidelity request, ask these questions in separate rounds:

1. Which exact reference states must match?
2. Where will users view them?
3. What must be the same before you accept the result?

Do not list devices, thresholds, or visual treatments.
