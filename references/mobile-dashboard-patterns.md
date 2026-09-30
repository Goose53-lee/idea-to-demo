# Mobile dashboard patterns

Use this reference when the supplied screenshots or product request describe a phone-first dashboard, analytics board, health summary, finance view, transaction overview, or other data-heavy mobile surface.

When multiple reference images are available, first extract the shared composition and interaction rules, then choose only the domain pattern that matches the user's core task. Treat screenshots as visual evidence, not as a request to reproduce their brands, labels, or exact content.

## Product stance

A mobile dashboard is a decision surface, not a desktop dashboard placed on a narrow canvas. It should answer three questions quickly:

1. What is the current state?
2. What changed or deserves attention?
3. What can I do next?

Keep the first viewport intentionally small. Prefer one clear status or hero metric, one primary trend or composition, and one next action. Put secondary detail below the fold, behind a tab, or inside an expandable section.

## First-screen anatomy

Use this sequence as a starting point, then remove anything that does not support the primary decision:

```text
Safe-area shell → title and scope → tabs or time range → status summary
→ primary metric or health signal → one analytical view → next action
```

### Safe-area shell

- Respect the status bar and bottom home indicator.
- Keep back, title, search, share, favorite, and overflow actions in a stable top row.
- Use persistent bottom navigation only when the product has three to five durable destinations.
- Keep icon-only actions labeled for assistive technology and give unfamiliar icons a tooltip or accessible name.

### Scope and mode controls

- Use short segmented controls or horizontally scrollable tabs for modes such as week/month/year, overall/self-operated, domestic/overseas, or category filters.
- Keep the active state obvious through position, weight, underline, or a semantic color; do not rely on color alone.
- Place the time range, comparison basis, and location or account scope near the value they change.

### Status summary

- Show one to four primary metrics. Make the most important value visibly dominant.
- Include the unit, period, and comparison direction. State whether an increase is good, bad, or needs attention.
- Use a compact health strip, progress band, or alert summary when a status is more useful than a raw number.
- Do not make every metric a visually equal floating card.

### Primary analytical view

- Use one chart or composition that explains the most important relationship: trend, distribution, funnel, risk, or progress.
- Attach the chart to a metric or action. A chart with no interpretation or drill-down is decorative.
- Provide a readable title, unit, time range, legend when needed, and a way to inspect exact values.
- On narrow screens, simplify to one series or a compact summary before reducing type. Allow a focused chart to scroll internally only when the horizontal scale is essential.

### Next action and disclosure

- Put the most likely next action directly after the summary or chart: view details, handle an exception, buy, submit, compare, or open the full list.
- Use a sticky bottom CTA for a single high-value action, but keep it above the safe area and ensure it does not cover content.
- Use disclosure for long explanations, records, medication or product lists, and supporting calculations.

## Common mobile dashboard variants

### Consumer health or guidance

```text
Location or profile → category tabs → current stage or risk signal
→ trend or index → symptom or guidance highlights → recommended content or action
```

Keep safety language, thresholds, and escalation actions explicit. Do not present a health score without its meaning or next step.

### Operations or business analytics

```text
Account or business scope → period → pending or health summary
→ source, funnel, or trend → key records or exceptions → details
```

Prioritize orders, revenue, conversion, service, fulfillment, violations, or other action-linked measures. Use cards for short actionable records rather than reproducing a desktop table.

### Finance or investment

```text
Market or account tabs → return or risk summary → performance trend
→ risk or allocation composition → recommendation or transaction action
```

Pair returns with time basis and risk context. Distinguish personal performance, benchmark performance, allocation, and transaction history.

### Transaction or record detail

```text
Object identity → state and filter → focused trend or history
→ compact record list → fixed buy/sell/approve/resolve action
```

Keep the primary object and action visible while the user scans chronology or evidence. Avoid making the user scroll past a long chart before reaching the action.

## Responsive and interaction rules

- Design at a realistic phone width, typically 360–430 CSS px, then verify a smaller 320px viewport when practical.
- Use 16–20px page gutters and stable vertical rhythm; let cards wrap or stack rather than compressing content into unreadable columns.
- Keep body text at 14–16px, inputs at least 16px, and all touch targets at least 44×44px.
- Prevent nested vertical scroll regions unless the component is a deliberate, labeled list or chart viewport.
- Keep tabs and chips horizontally scrollable with the active item reachable; do not hide the current mode off-screen.
- Use pull-to-refresh, swipe, or gesture behavior only when it is discoverable and not required for the core path.
- Preserve loading, no-data, error, permission, and delayed-update states inside each chart or summary module. One failed module must not blank the whole screen.
- Make long values wrap, abbreviate with a clear unit, or open a detail view. Do not solve fit problems by dropping ordinary text below the skill's minimum sizes.

## Visual and data rules

- Use one primary accent plus semantic status colors. Keep positive and negative meaning consistent across numbers, charts, and labels.
- Prefer calm surfaces, light borders, and limited shadows. Do not turn every section into a floating container.
- Use realistic, reconciled mock data. Totals, percentages, comparison labels, chart endpoints, and detail records must agree.
- Always show update time or data freshness when the dashboard implies live or periodic data.
- Give each chart a drill-down path such as `metric → trend → filtered records → detail` when the user needs to investigate.
- Do not copy supplied brands, logos, watermarks, private values, or unverified claims from reference images.

## Mobile dashboard acceptance checklist

- The first viewport communicates current state, important change, and next action.
- One to four metrics are primary; secondary values are visibly subordinate.
- The main chart or composition remains legible without zooming and exposes exact values when needed.
- Tabs, filters, and actions are reachable with touch and have visible active or disabled states.
- Safe-area padding, keyboard behavior, sticky CTA clearance, and bottom navigation do not occlude content.
- Loading, empty, error, and delayed-data states preserve the surrounding context and offer recovery.
- The page does not behave like a shrunk desktop table or a grid of equal cards.
