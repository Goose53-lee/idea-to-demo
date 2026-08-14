# UI foundations

Use this reference when defining layout, visual language, tokens, metrics, charts, or business imagery.

## Contents

- Design principles
- Visual hierarchy and density
- Default visual system
- Mandatory typography and readability
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

### Refined admin styling

For polished admin and commerce-operation demos, refinement should come from precision, not decoration.

Use:

- a calm blue-and-white or neutral-light base when it fits the business context;
- one primary accent plus semantic status colors;
- crisp 1px borders, stable radii, subtle hover/focus states, and restrained shadows only for raised layers;
- soft tinted backgrounds for selected navigation, active filters, alerts, and priority tasks;
- icon plates or light dimensional icons only when they improve recognition of modules such as store, order, visitor, transaction, content, or risk;
- compact but breathable module spacing so the first viewport shows both summary and next action.

Avoid:

- turning every metric into an equal card with the same emphasis;
- decorative glass panels, heavy blur, glow, large gradients, or fake 3D surfaces as the main style;
- using blue everywhere without semantic contrast;
- random icon colors unrelated to business meaning;
- visual effects that make data, tables, filters, or actions harder to scan.

Polished first screens usually combine a clear shell, a dominant metric or trend area, concise status strips, and a limited supporting rail. The user should understand what changed, what is risky, and what to do next without reading explanatory marketing copy.

## Mandatory typography and readability

Apply this section to UI design decisions, design/image-generation prompts, visual specifications, CSS or Tailwind output, component-library work, and browser verification. These are mandatory constraints unless the user explicitly supplies a stricter product standard.

### Core rules

- MUST use 14px as the default for ordinary body copy, table cells, form content, and list content. Most readable page content MUST be 14px or larger.
- MUST NOT use text smaller than 12px in an ordinary interface.
- MAY use 11px only for strongly de-emphasized, non-essential information such as chart axes, non-core timestamps, extremely minor supplementary notes, space-constrained status assistance, or annotations that do not affect the primary task.
- MUST NOT use text below 11px.
- MUST NOT shrink type merely to fit more content. MUST first improve information selection, grouping, container dimensions, spacing, wrapping, disclosure, scrolling, or responsive structure.
- MUST NOT use 12px as the broad default for body copy or primary information unless the user explicitly requests it.
- MUST create a clear hierarchy with size, weight, color, and spacing rather than assigning one size to everything.
- MUST NOT produce a small-type-led, high-density interface unless explicitly requested by the user.

### Default hierarchy

Use these as defaults with limited adjustment for the page type:

```text
Page title: 24–32px
Section title: 18–20px
Card or group title: 16px
Emphasized body or important data label: 14–16px
Body, table, list, and form content: 14px
Supporting information: 12px
Extremely minor annotation: 11px
Primary metric or display value: 24–40px
```

### Component requirements

| Component | Required typography |
| --- | --- |
| Primary button | SHOULD use 14–16px |
| Secondary button | MUST be at least 13px |
| Small button | MUST be at least 12px; 10px or 11px is forbidden for ordinary button text |
| Input value | MUST default to 14px |
| Input label | MUST default to 14px and be at least 12px |
| Placeholder | SHOULD use 13–14px |
| Validation message | MUST be at least 12px |
| Form help | MUST use 12px; only a non-essential supplement MAY use 11px |
| Table header | SHOULD use 13–14px |
| Table body | MUST default to 14px |
| Secondary table field, status tag, or row action | MUST be at least 12px |
| Main navigation | SHOULD use 14–16px |
| Side navigation | MUST default to 14px |
| Secondary navigation | MUST be at least 13px |
| Breadcrumb | MUST be at least 12px |
| Dropdown menu | MUST default to 14px |
| Card title | MUST default to 16px |
| Card body | MUST default to 14px |
| Card support text | MUST use 12px; only a non-core note MAY use 11px |

Never set an entire table to 10px or 11px for density.

### Mobile and data visualization

- Mobile body text MUST default to 14–16px. Mobile input text SHOULD be at least 16px to avoid browser auto-zoom. Text in a touch target MUST be at least 12px; top and bottom navigation SHOULD use 12–14px. MUST NOT compress all typography because the screen is smaller.
- Data-display typography MUST reflect actual viewing distance. Chart titles SHOULD be at least 14px; legends, axes, and data labels SHOULD use 11–13px; core chart data MUST be at least 12px. Core metrics MUST have sufficient visual weight and SHOULD use 24–40px rather than inheriting ordinary desktop-admin sizes.

### Line height

Use consistent semantic line-height tokens. Do not enlarge font size without checking vertical rhythm.

```text
11px type: at least 16px line height
12px type: at least 18px line height
14px type: 20–22px line height
16px type: about 24px line height
18px type: about 26px line height
Multiline body: 1.5–1.7 line height
```

MUST NOT use cramped line height, near-single-line leading for multiline body copy, overly loose leading around tiny text, or inconsistent size/leading for the same semantic role across modules.

### Font tokens

Use existing semantic project tokens first. If the project has no typography system, establish equivalent tokens before styling individual components:

```css
--font-size-caption: 11px;
--font-size-helper: 12px;
--font-size-body: 14px;
--font-size-body-emphasis: 16px;
--font-size-section-title: 18px;
--font-size-page-title: 24px;
--font-size-display: 32px;

--line-height-caption: 16px;
--line-height-helper: 18px;
--line-height-body: 22px;
--line-height-body-emphasis: 24px;
--line-height-section-title: 26px;
--line-height-page-title: 32px;
--line-height-display: 40px;
```

For Tailwind CSS:

- MUST NOT use `text-[9px]` or `text-[10px]`.
- MAY use `text-[11px]` only for an extremely minor annotation.
- MUST NOT use `text-xs` for broad body, table, form, list, or button text.
- SHOULD use `text-sm` for ordinary body content and `text-base` when additional readability is needed.
- SHOULD map headings to their hierarchy with `text-base`, `text-lg`, `text-xl`, or larger utilities instead of arbitrary undersized values.

### Handling insufficient space

When text does not fit, resolve the problem in this order:

1. Remove invalid, duplicate, or non-essential information.
2. Improve content grouping and hierarchy.
3. Increase the container width or height.
4. Adjust padding and component spacing without harming touch or scan targets.
5. Allow sensible wrapping.
6. Use truncation with Tooltip, expansion, or a detail interaction.
7. Use horizontal scrolling or a responsive restructuring.
8. Only then make a small font adjustment within the allowed limits.

MUST NOT reduce ordinary 14px content directly to 11px or 10px.

### Typography preflight and final audit

Before generating a UI, image prompt, or code, identify page titles, section titles, body and primary data, supporting information, and the rare annotations eligible for 11px. Check whether density is driving inappropriate small type and whether the sizes match desktop, mobile, or distance-viewed display conditions. Encode these roles and sizes explicitly in generated prompts and implementation plans.

Before final output, MUST inspect the design or computed styles and correct failures first:

1. No font size is below 11px.
2. 11px is not used broadly and appears only on genuinely non-essential annotations.
3. Ordinary body content is primarily 14px.
4. Table body content is 13–14px, with 14px as the default.
5. Form input content is at least 14px.
6. Button labels meet the 12–14px minimum appropriate to their size and priority.
7. Titles, body, and support text form a clear hierarchy.
8. Equivalent components use consistent sizes and line heights across pages.
9. No layout problem was hidden by shrinking text.
10. The page is comfortably readable at normal display zoom and the intended viewing distance.

If any check fails, MUST adjust the layout or typography and repeat the audit before handoff.

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

For commerce and shop-operation metrics, prefer relationships that explain the business funnel:

```text
Traffic → product views → clicks → orders → paid amount → refunds or after-sales → repeat purchase
```

Keep visitor, transaction, conversion, fulfillment, content, and risk metrics distinguishable. Do not merge them into one vague "growth" score unless the source product defines that score. Pair every comparison with direction and meaning, such as whether an increase is good, bad, or needs attention.

## Images and industry expression

Express industry character through real objects, fields, workflows, evidence, and data relationships.

Use project photos, product images, plans, maps, device images, or site records only when they support identification, comparison, progress evidence, spatial understanding, or a decision. Pair images with structured titles, states, fields, and actions.

Do not use supplied brand assets, people, watermarks, or private content in the final demo without authorization.
