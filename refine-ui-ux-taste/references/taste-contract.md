# Taste Contract

Use this contract for the current screen, flow, or bounded set of outputs. Do not force decisions about unrelated future work.

## Compact decision ledger

Keep these lists short and update them after each useful answer:

- **Confirmed:** user-owned taste rules, reasons, exclusions, and acceptance checks.
- **Observed:** relevant facts found in supplied references or existing work, without assumed approval.
- **Unresolved:** material taste choices that still block the current work.
- **Conflicts:** confirmed rules that cannot both pass in the same state.
- **Deferred:** a named unknown, why it is safe to delay, and the event that reopens it.
- **Agent-owned:** small, reversible craft choices that stay inside the confirmed direction.

Do not move an agent-created choice into **Confirmed** because the user accepted a prefilled brief. Record the user's own words or prior material first.

## Readiness rubric

Score only the dimensions that can change the current work:

- `0` — absent, contradictory, vague, or being invented by the agent;
- `1` — a direction exists, but a material rule, reason, or check is missing;
- `2` — specific enough to apply and check; or
- `N/A` — cannot affect the current work, with a recorded reason.

Every applicable dimension must reach `2` before substantial design or implementation.

| Dimension | A score of `2` requires |
|---|---|
| Work boundary | The exact screen, flow, state, or output set is clear |
| User and purpose | The relevant user and task are clear, or verified as already known |
| Identity | The intended character, its reason, and visible meaning are clear |
| References and exclusions | Each relevant reference has retain, change, and avoid decisions; unwanted traits are explicit |
| Hierarchy, layout, and density | Importance order and information arrangement have clear rules tied to the task |
| Visual language | Material text, color, shape, surface, image, and icon rules are clear |
| Interaction language | Important responses and motion have rules tied to the intended experience |
| States and view sizes | Material states and relevant size changes have clear rules |
| Access | Known access needs and checkable access requirements are protected |
| Evidence | Each material rule has a location and a check that can pass or fail |

Do not lower a score because the user used plain words. Judge the decision, not the vocabulary.

## Taste worksheet

Accept answers in prose, fragments, marked screenshots, spoken notes, or existing documents. Do not require the user to fill this form when the information already exists.

```text
Mode:
Current screen, flow, or output set:
Known user and task:
Intended character:
Why that character fits:
Visible rules that express it:
Traits that must not appear:
References supplied by the user:
What to retain from each reference:
What to change from each reference:
What to avoid from each reference:
Why those choices fit:
Importance order:
Layout and information density rules:
Text rules:
Color jobs and rules:
Shape, border, layer, and depth rules:
Image and icon rules:
Response and motion rules:
Key states:
Rules across relevant view sizes:
Access needs and checks:
Material rule locations:
Checks that can pass or fail:
Confirmed decisions:
Observed facts:
Open decisions:
Conflicts:
Safely deferred decisions and revisit events:
Agent-owned reversible details:
```

## Reference observation record

Use one record for each user-supplied reference that affects the current work.

```text
Reference:
Exact screen or state:
Visible composition and importance order:
Visible spacing and information density:
Visible text roles:
Visible color roles:
Visible shape, border, layer, and depth rules:
Visible image and icon rules:
Visible response or motion, when evidence exists:
Behavior across view sizes, when evidence exists:
Facts the reference cannot prove:
User decision about what to retain:
User decision about what to change:
User decision about what to avoid:
User reason for each decision:
```

Describe only evidence that the supplied material shows. A static image cannot prove motion, keyboard behavior, loading behavior, or responsive rules.

Do not use the reference's whole appearance as a substitute for explicit user choices.

## Screen and state contract

Use one compact contract for each screen or state whose material rules differ. Combine screens when the same rules and checks apply.

```text
Screen or state:
User task here:
What users must notice first, second, and later:
Layout and density rule:
Text rule:
Color rule:
Shape and surface rule:
Image and icon rule:
Important user action:
Required response:
Motion rule, when material:
What changes across relevant view sizes:
What must stay fixed across those sizes:
Access rule:
Traits that must not appear:
Reason for each material rule:
Visible or measurable acceptance check:
Source of each confirmed rule:
```

Do not require a field that cannot change the current screen or state. Record `N/A` with a short reason when omission might otherwise look accidental.

## Plain question translations

Use these questions only when that decision is both unknown and material. Define the bold term before using it with a beginner.

| Internal decision | Ask the user |
|---|---|
| Work boundary | Which screen, flow, or output are we defining now? |
| User and purpose | Who uses this screen? What must that person finish here? |
| **Identity:** how the product should look and feel | How should this interface look and feel? Why does that direction fit? |
| Reference meaning | What must we retain, change, and avoid from this reference? Why? |
| Exclusion | Which visual or interaction traits must never appear? Why? |
| **Hierarchy:** the order in which people notice information | What must users notice first, second, and later? |
| Layout and density | How much information should this view show? How must the arrangement support the task? |
| Text system | How must headings, labels, and other text show their different jobs and importance? |
| Color system | What must color show or distinguish? Which color rules must stay consistent? |
| Shape and surface system | Which rules must control corners, borders, shadows, and overlapping areas? |
| Images and icons | What must images and icons communicate? Why do they fit the identity? |
| Motion | Which changes need motion? What must the motion communicate? |
| Interaction response | What response must follow each important action? How must it support the intended character? |
| **Screen state:** what a screen shows under one condition | Which conditions change this screen? What must remain clear in each condition? |
| Responsive behavior | Which view sizes matter? What must change or stay fixed at each size? |
| Access | Which access needs apply? Which checks will prove support for them? |
| Rationale | Which user need, task, character rule, or reference decision supports this choice? |
| Acceptance evidence | Where must this rule appear? What must a reviewer see, do, or measure? |

Do not ask the whole table in one round. Ask no more than three narrow decision clusters.

## Test each material rule

A useful acceptance check states:

- the exact screen, state, element, or action;
- the condition before the check;
- what the reviewer sees, does, or measures;
- the required result; and
- the boundary between pass and fail.

The user owns the intended result. The agent may test whether the wording has a clear pass boundary without writing that boundary for them.

Reject checks such as “looks polished,” “feels intuitive,” or “matches the brand.” Ask what visible behavior or property makes the claim true.

## Review record

Use this table when an approved taste contract exists.

| Contract rule | Output location | Status | Evidence |
|---|---|---|---|
| User-owned rule | Screen, state, element, or action | Passed, failed, conflicting, or not proven | Visible or measurable fact |

Then report:

```text
Review boundary:
Passed rules:
Failed rules:
Conflicting rules:
Rules without enough evidence:
Observations outside the contract:
Decision needed from the user:
```

Do not convert an observation outside the contract into a defect. Ask the user whether it should become a new rule.

## Neutral response patterns

Adapt these patterns to the current work. Do not add sample design answers.

### Vague creation request

> I need your direction before I design this interface.
>
> 1. Who uses this screen? What must that person finish here?
>
> This connects the design to a real task.
>
> 2. How should this interface look and feel? Why does that direction fit?
>
> This sets the product's character without choosing it for you.
>
> 3. Which visual or interaction traits must not appear? Why?
>
> This sets a clear boundary.

### Reference-only request

> The reference does not define your product's taste.
>
> 1. What must we retain from this reference?
>
> 2. What must we change from this reference?
>
> 3. What must we avoid from this reference? Why?

### Vague taste word

> “Modern” does not define a visible rule.
>
> What must a reviewer see before that word is true for this product?

Use the user's actual word in place of “modern.” Do not supply visual traits.

### Request for a recommendation

> I will not choose the product's taste.
>
> Compare your choice with the user task, intended character, access needs, and supplied reference evidence.
>
> State your choice and explain which confirmed need it supports.

### Existing pattern

> I found this visible rule in the current work: [observed rule].
>
> Must this rule stay, change, or disappear? Why?

### Conflicting rules

> These confirmed rules conflict in [screen or state].
>
> [Rule one and visible consequence.]
>
> [Rule two and visible consequence.]
>
> Which rule controls this screen or state? Why?

Do not add a preferred resolution.

### Review-only result

> I checked [output] against the approved taste contract.
>
> Passed: [rules with evidence].
>
> Failed: [rules with evidence].
>
> Not proven: [rules without enough evidence].
>
> I made no changes.

## Proportionality checks

Before asking another question, check:

1. Can this answer change the current output?
2. Is the answer already present in supplied material?
3. Does the user own this choice, or can the agent safely handle it?
4. Can the current screen or flow pass without this decision?

Do not ask when the answer cannot affect the current work. Do not reopen a confirmed decision without new conflicting evidence.
