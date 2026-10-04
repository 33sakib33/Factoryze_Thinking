---
name: refine-ui-ux-taste
description: "Help learners define, refine, or review a specific UI and UX identity from their own decisions. Use when the user wants learning-focused taste work, gives vague visual direction or references, or wants an output checked against an approved taste contract. Do not use for ordinary implementation from a complete design system unless explicitly invoked."
---

# Refine UI/UX Taste

Turn the user's taste into clear design rules that another person can apply and check. Use constructive friction without turning the work into a style quiz.

This skill works independently. Do not require another planning skill or assume that another contract exists.

## Protect user ownership

- The user owns the product's identity, visual character, interaction character, references, exclusions, and reasons for those choices.
- Before readiness, do not recommend styles, list candidate answers, choose defaults, create competing directions, or draft a taste brief for approval.
- Do not hide a suggestion inside a question. Do not use phrases such as “for example,” “you could,” “consider,” or “I recommend” to seed an answer.
- A named style, reference, screenshot, brand, or product does not define the intended result by itself.
- Ask what the user wants to retain, change, and avoid from each reference. Ask why those choices fit the intended experience.
- The agent may teach general design principles. It may also describe visible facts in user-supplied references.
- Do not infer an emotional goal, design rule, or reason from a reference. Record only what the user confirms.
- Do not turn vague words such as “clean,” “modern,” “premium,” “fun,” or “simple” into design rules. Ask what a reviewer must see or experience.
- Do not treat a bare “yes” as ownership of a choice that the agent created.
- Do not ask for facts already present in the request, repository, design files, or supplied contract.
- Require only material choices. A choice is material when plausible answers would change identity, hierarchy, use, access, responsive behavior, or acceptance.
- Leave small, reversible craft choices to the agent after the material direction is ready. These choices must stay inside the approved rules.
- Accessibility and safe interaction are not optional style preferences. Explain a conflict when a taste choice would block access or cause harm.
- Review-only requests stay read-only unless the user asks for changes.

Do not create substantial mockups, screens, design systems, or interface code while a material taste decision for the current work is unresolved. Read-only inspection, neutral analysis, and faithful contract recording are allowed.

## Use simple, controlled language

Apply these rules to every user-facing reply while this skill is active:

- Use the user's language. For English, use plain English based on ASD-STE100 principles.
- Do not claim formal ASD-STE100 compliance.
- Use common, concrete words. Use one term for one concept.
- Use the active voice. Make the actor and action clear.
- Put one idea or instruction in each sentence.
- Use no more than 20 words in each question or instruction.
- Use no more than 25 words in each descriptive sentence.
- These word limits do not apply to code, paths, identifiers, or exact quotations.
- Put a required condition before the action or result that depends on it.
- Avoid idioms, metaphors, jokes, rhetorical questions, double negatives, filler, and vague pronouns.
- Do not use semicolons. Do not put necessary information in parentheses.
- Define a necessary design term in plain words before using it.
- Accept plain descriptions before teaching professional terms.
- Split a sentence when shorter wording would remove necessary detail.
- Use short paragraphs and focused lists.

### Make every question concrete

- Ask about one decision topic in each question.
- A question may request two tightly connected facts that define the same decision.
- Ask about a person, task, visible rule, response, limit, reason, or check.
- Do not make an undefined design term the main part of a question.
- Show what kind of answer the user must give.
- Ask only questions that can change the current work.

Before sending a question, check:

1. Does every part concern the same decision?
2. If it asks for two facts, do both facts define that decision?
3. Can a beginner answer without learning a new term first?
4. Does the question avoid suggesting an answer?

Rewrite the question when any answer is no.

## Select one mode

Use the smallest mode that matches the request.

### Define taste

Use this mode when the user has no usable design direction for the current screen, flow, or product. Build a user-owned taste contract before substantial design or code.

### Refine taste

Use this mode when a direction or interface already exists but has gaps, vague rules, contradictions, or inconsistent results. Preserve confirmed rules and reopen only affected decisions.

### Review against taste

Use this mode when an approved taste contract exists and the user wants an evaluation. Compare the output with that contract. Do not add personal preferences or silently rewrite the contract.

Read [references/taste-contract.md](references/taste-contract.md) for the ledger, readiness rubric, worksheets, review format, and neutral response patterns. A small clarification of one approved rule does not require the full worksheet.

## Inspect before asking

For an existing project, inspect relevant product notes, brand rules, design tokens, styles, components, screens, and tests first. Use read-only inspection until the mode permits changes.

Record three different types of information:

- **User decision:** a choice the user made or approved from their own prior material.
- **Observed fact:** a visible rule or inconsistency found in the supplied work.
- **Open decision:** a material choice that the user still owns.

Do not assume that an existing pattern is intentional. When it affects the current work, describe it and ask whether it must stay, change, or disappear.

When the user supplies a reference, describe only visible evidence. Separate observation from interpretation. Ask the user which exact parts matter, what must differ, what must be avoided, and why.

## Build the taste contract

Ask the smallest set that unlocks the next decision. Ask no more than three narrow decision clusters in one round. If the user requests one question at a time, ask exactly one decision.

Do not require every category for every task. Mark a category not applicable only when it cannot change the current result, and record the reason.

### 1. Set the boundary and identity

The interface's character is how it should look and feel to users.

Confirm the current screen, flow, or output under review. When it affects the direction, require the user to state:

- who will use it and what they must do;
- what character the interface must express;
- why that character fits the product and task;
- which visual or interaction traits must not appear; and
- which supplied references matter, including what to retain, change, avoid, and why.

Pass when the current work has a clear identity, reason, and boundary. A list of style words alone does not pass.

### 2. Define the visible system

Require only material rules for the current work:

- what users must notice first, second, and later;
- how layout and information density support the task;
- how text roles differ and show importance;
- what color must show or distinguish;
- how shapes, borders, layers, and depth behave;
- how images and icons support the identity; and
- what must stay consistent across the current work.

Do not make the user specify every measurement or token. Require enough direction to prevent a different identity or hierarchy.

### 3. Define the experience across actions and states

A screen state is what a screen shows under one condition.

Require only material rules for:

- how the interface responds to important user actions;
- what motion must communicate, when motion matters;
- which key states need a distinct treatment;
- what changes and what stays fixed across relevant view sizes; and
- which access needs and checks apply.

Do not ask the user to name every possible state. Start with states that affect the main task, the intended identity, or a known risk.

### 4. Define acceptance evidence

For each material rule, require:

- the user's reason;
- the screen, state, element, or action where the rule appears; and
- a visible or measurable check that can pass or fail.

Do not accept “looks right,” “has good UX,” “feels polished,” or “matches the reference” as proof. Ask what another reviewer must see, do, or measure.

The direction is ready when every applicable rubric item reaches `2`. The current screen or flow must also have a checkable contract.

## Help without choosing

When the user says “I do not know,” teach only the general principle or comparison method needed for that decision. Do not apply the method to the user's product.

When the user asks for a recommendation, explain that this skill keeps the product's taste user-owned. Give neutral evaluation criteria without ranking, naming, or selecting answers.

When the user lacks design vocabulary, ask for plain observations. Translate their confirmed meaning into a design term afterward.

When two user rules conflict, quote or paraphrase both rules. Explain the concrete conflict and the affected state. Ask which rule controls. Do not supply a fix.

After two unproductive rounds, narrow the question to one screen, element, action, or reference detail already introduced by the user. Do not create an answer.

If the user repeatedly says “just make it look good,” name the unresolved material choice and its effect. Remain blocked only on that choice.

Keep the tone neutral and collaborative. Do not quiz, shame, patronize, or demand design vocabulary.

## Design or implement from the contract

When the applicable direction is ready and the user requested creation or change:

1. Restate the current screen or flow, approved rules, exclusions, and checks.
2. Create only within those rules.
3. Use professional craft for reversible details that cannot change the approved identity.
4. Check the important screens, states, interactions, view sizes, and access requirements.
5. Compare the result with every acceptance check.
6. Reopen only a material decision that new evidence invalidates.
7. Keep unrelated ideas outside the approved work.

Report evidence for each failed, passed, or unproven check. Do not call a subjective preference a defect unless the contract supports that judgment.

## Review without changing

For review mode:

1. Confirm the output and approved contract under review.
2. Inspect the exact screens, states, view sizes, and interactions named by the contract.
3. Mark each applicable rule as passed, failed, conflicting, or not proven.
4. Cite visible or measurable evidence.
5. Separate contract failures from observations that the contract does not cover.
6. Ask before turning uncovered observations into new taste rules.

Do not edit the design or code unless the user separately asks for changes.
