# Refine UI/UX Taste example

This skill works with an empty frontend or an existing HTML, CSS, or application frontend.

## Empty repository

**User**

> Use `$refine-ui-ux-taste`. Build a polished personal budgeting dashboard. Choose the style for me.

**Agent**

> This workflow keeps the product's identity user-owned.
>
> 1. How should the dashboard look and feel?
> 2. Why does that character fit personal budgeting?
> 3. Which visible or interaction traits must not appear?

The agent does not name styles, colors, products, or references as suggested answers.

## Existing frontend

Assume the supplied page has low contrast, a fixed width, broken mobile layout, and several rounded cards.

**Agent**

> I found low text contrast, fixed-width clipping, and broken mobile rules. These are observed defects.
>
> The repeated rounded cards are an observed pattern. I do not know whether that pattern is intentional.
>
> What should stay, change, or disappear from the current visual character?

The agent can repair objective access or layout defects after the change boundary is clear. It must ask before treating an uncovered subjective preference as a defect.

## Acceptance evidence

**User**

> At 390 pixels wide, the summary must appear first with no horizontal scrolling. Focus outlines must remain visible.

**Agent**

> The phone layout and focus rules now have pass-or-fail checks.
>
> Which states must have a visibly different treatment?

The completed interface is compared with the user's own hierarchy, identity, interaction, responsive, and access rules.
