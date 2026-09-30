# Component validation

Use this reference when the user wants to test a small design choice without inventing a complete product, business workflow, or information architecture.

## When to use it

Activate this mode for questions such as:

- Which table row, card, toolbar, tab, filter, status, or empty state is clearer?
- Does a layout hold together at the target width?
- Which typography, spacing, radius, border, or color treatment is more readable?
- Does a component handle long content, loading, error, selected, or disabled states?
- Is a small interaction pattern understandable without building the surrounding product?

## Define the test

Write a compact test brief:

```text
Hypothesis: <design choice being tested>
Context: <viewport, platform, viewing distance, and component purpose>
Variants: <the alternatives being compared>
Criteria: <what would make one option better>
States: <only the states that can change the decision>
```

Do not require a primary business user, business object, product name, navigation shell, or realistic domain data unless the user says those affect the choice.

## Design the sandbox

- Prefer one route or one canvas with two to four variants.
- Keep the compared variants close enough that the decision is obvious, but not so close that the difference is imperceptible.
- Change one major variable at a time when possible.
- Use neutral, plausible content that exposes the real layout: short and long labels, missing values, status changes, large numbers, and multiple lines.
- Show the variant name and the tested difference outside the component itself; do not add explanatory copy inside the product UI.
- Use a selector only when side-by-side comparison would make the components too small.
- Avoid adding unrelated dashboard modules, navigation, account areas, or fake business actions.

## State coverage

Choose states based on the hypothesis. Common candidates are:

- default;
- hover and keyboard focus;
- selected or active;
- disabled or unavailable;
- loading;
- empty or no result;
- error or validation;
- long content, missing value, and extreme number;
- narrow viewport.

If the component is interactive, implement only the local behavior needed to judge it. For example, a tab comparison may switch the visible panel, but it does not need a complete application route or persistence layer.

## Review criteria

Check the component at the intended viewport and at least one narrower width. Review:

- hierarchy and first-glance comprehension;
- fit, wrapping, truncation, and overflow;
- alignment and spacing rhythm;
- contrast and status meaning;
- focus visibility and keyboard reachability when relevant;
- touch target size on touch surfaces;
- state transitions and feedback when relevant;
- whether the component still works with realistic content extremes.

Do not claim that a component sandbox validates the surrounding product flow, API behavior, permissions, or production performance.

## Handoff

Report:

- the hypothesis;
- the variants shown;
- the states and viewports checked;
- the observed trade-offs;
- the selected direction, if one is clear;
- unresolved questions and what the sandbox does not prove.

An inconclusive result is valid. Preserve the alternatives when the evidence does not support a confident choice.
