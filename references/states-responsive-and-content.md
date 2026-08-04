# States, responsive behavior, and content

Use this reference when defining UI states, mock data, text, formatting, responsive behavior, accessibility, and motion.

## Contents

- State matrix
- Recovery behavior
- Responsive rules
- Mock data
- Formatting and copy
- Accessibility and motion

## State matrix

Consider each relevant component or screen across:

| State | Question to answer |
| --- | --- |
| Default | What is visible and actionable? |
| Hover and focus | How does the user know an element is interactive? |
| Loading | What remains understandable while waiting? |
| Initial empty | How can the user create or import the first object? |
| Search no result | How can the user clear or change the query? |
| Filter no result | Which active filters caused the result? |
| Error | What failed, what was preserved, and how can the user retry? |
| No permission | What is hidden, disabled, or requestable? |
| Disabled | Why is the action unavailable? |
| Submitting | How are duplicate actions prevented? |
| Success | What changed and where can the user continue? |
| Extreme data | What happens with long text, large numbers, many rows, or missing values? |

Implement the states necessary to validate the selected flow. Do not create every theoretical state if it adds no review value, but never ignore a failure state that blocks the core path.

## Recovery behavior

Every error must provide a recovery path. Examples include retry, edit input, clear filters, return to the previous step, save a draft, contact an administrator, or inspect failure details.

Do not clear user-entered content after a failed submission. Keep unaffected modules usable when one module fails.

## Responsive rules

Do not implement mobile by shrinking the desktop canvas.

Use desktop for full management, batch operations, complex analysis, and configuration. Use mobile for quick viewing, lightweight processing, approval, field execution, and frequent creation.

For narrow screens:

- keep three to five primary navigation destinations;
- use one-column forms;
- convert wide tables into business cards or hide low-priority columns;
- allow secondary tabs to scroll horizontally;
- keep one primary fixed or prominent action;
- use touch targets of at least 44×44px;
- protect content from status bars, keyboards, and bottom safe areas;
- simplify charts to one primary series or compact progress views;
- keep one to four metrics on the first screen.

Desktop and mobile must preserve business terms, values, state meanings, and calculation rules even when their layout differs.

## Mock data

Mock data must be plausible and internally consistent.

Verify:

- object relationships;
- chronological order;
- state and permitted actions;
- totals, percentages, subtotals, and currency;
- trend direction and comparison text;
- responsible people and organization scope;
- identifiers reused across linked pages.

Use missing values intentionally. Display missing information as `--` or an explained empty state rather than converting it to zero.

State clearly that mock data does not demonstrate API, database, permission, or audit behavior.

## Formatting and copy

- Use thousands separators for amounts.
- Keep decimal places consistent within one module.
- Separate values and units.
- Use one convention for K, M, 万, or 亿 within a region.
- Include `%` for percentages.
- Use consistent date and time formats.
- Name buttons with specific actions such as Create, Save, Submit, Import, Retry, or Confirm payment.
- Avoid vague labels such as Confirm, Explore, or Try now when a precise verb exists.
- Explain the reason and recovery in error messages.
- Keep enterprise-tool copy direct and professional.

## Accessibility and motion

- Maintain sufficient text contrast.
- Never communicate state through color alone.
- Provide labels for form controls.
- Keep keyboard paths logical.
- Make focus visible.
- Give icon buttons accessible names or tooltips.
- Respect reduced-motion preferences when motion exists.
- Use motion for state change, expansion, and hierarchy transitions.
- Keep most transitions between 150 and 300ms.
- Avoid continuous floating, decorative loops, or motion that delays comprehension.
