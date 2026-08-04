# UI foundations

Use this reference when defining layout, visual language, tokens, metrics, charts, or business imagery.

## Contents

- Design principles
- Visual hierarchy and density
- Default visual system
- Layout selection
- Metrics and charts
- Images and industry expression

## Design principles

1. Prioritize the user's task over decorative impact.
2. Make business priority visible through position, area, density, and interaction.
3. Set one primary visual center per major screen.
4. Use medium-to-high information density for desktop administration work.
5. Keep the visual language simple, restrained, and credible.
6. Design failure and edge states as part of the product.
7. Reuse components, data formats, terminology, and state semantics.
8. Choose structures according to the task instead of applying one dashboard template.

## Visual hierarchy and density

Use grouping, alignment, typography, spacing, and progressive disclosure to make dense information readable.

Avoid:

- giant titles and cards used only to create hierarchy;
- large empty regions without business purpose;
- every module wrapped in a separate floating card;
- equal-size modules with equal visual weight;
- decorative imagery that competes with work content;
- excessive gradients, glass effects, glow, particles, or looping motion.

Main content commonly occupies 6–9 columns of a 12-column grid. Supporting content commonly occupies 3–6 columns. Adjust the ratio to the task rather than forcing exact symmetry.

## Default visual system

Use project tokens first. If none exist, begin with the following restrained defaults.

### Color

```text
Page background: #F5F7FA or #F7F8FA
Content background: #FFFFFF
Primary text: #111827 or #1F2329
Secondary text: #646A73 or #667085
Muted text: #98A2B3
Border: #E5E7EB or #E8EAED
Disabled background: #F2F3F5
Brand: one clear project-appropriate accent
```

Use green for success, blue for active or processing, orange for attention, red for risk or failure, and gray for inactive or unavailable. Determine positive and negative meaning from the business metric; a rising complaint or refund rate is negative.

### Typography

```text
Page title: 20–24px / 600
Section title: 16–18px / 600
Body: 14px
Table: 13–14px
Supporting text: 12–13px
Primary metric: 24–32px / 600
```

Do not use text smaller than 12px without a clear reason.

### Spacing and surfaces

Use a 4px spacing grid: `4 / 8 / 12 / 16 / 20 / 24 / 32 / 40 / 48`.

```text
Desktop page padding: 24–32px
Module gap: 16–24px
Card padding: 16–24px
Mobile page padding: 16–20px
Normal desktop radius: 4–8px
Normal mobile radius: 8–12px
Border: 1px light gray
Shadow: none by default; light shadow for floating layers
```

Use one consistent icon library. Keep size, stroke, and visual weight consistent. Colored icon plates may aid recognition, but do not assign random colors without meaning.

## Layout selection

Select among:

- sidebar + top utility bar + content;
- top navigation + wide content;
- main workspace + persistent right rail;
- wide process, timeline, or Gantt center;
- business object, map, plan, device, or preview center.

Use side navigation for stable multi-module systems. Use top navigation when horizontal width is critical. Use a right rail for short todos, alerts, and quick actions, not for complex comparison tables.

Place global search, organization scope, notifications, and account controls in the global shell. Keep page filters and business actions in the content area.

## Metrics and charts

Metrics help users judge totals, change, exceptions, and available actions. A metric should include a label, primary value, unit, period, comparison context, and semantic interpretation when relevant.

Keep the primary value dominant. Use neutral card borders; do not differentiate metric cards with colored edge strips. Limit a metric region to three or four semantic colors.

Choose charts by data relationship:

- line for change over time;
- vertical bars for category comparison;
- horizontal bars for many or long category names;
- pie or ring only for a small number of whole-part categories;
- funnel for stage conversion;
- timeline for ordered events;
- Gantt for duration and dependency;
- stepper for a limited stable process;
- progress for goal completion;
- table for precise and actionable records.

Every chart needs a title, time range, unit, legend where necessary, definition, active filters, and update time. Provide loading, no-data, failure, delay, and permission states. One failed chart must not block the full dashboard.

Use the drill-down sequence when appropriate:

```text
Metric → trend or category → filtered records → object detail
```

Avoid 3D charts, decorative gauges, too many pies, and charts with no decision or action attached.

## Images and industry expression

Express industry character through real objects, fields, workflows, evidence, and data relationships.

Use project photos, product images, plans, maps, device images, or site records only when they support identification, comparison, progress evidence, spatial understanding, or a decision. Pair images with structured titles, states, fields, and actions.

Do not use supplied brand assets, people, watermarks, or private content in the final demo without authorization.
