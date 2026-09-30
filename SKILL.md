---
name: idea-to-demo
description: "Turn rough product ideas, requirements, PRDs, screenshots, component questions, or existing frontend repositories into clean, runnable demos for early validation. Use for component and pattern comparisons as well as admin, back-office, and mobile dashboard flows. Focus on the smallest useful frontend artifact: it may be a component sandbox with synthetic content or a connected demo with coherent mock data and core interactions. Do not present the result as production-ready or use this skill for backend, security, deployment, or full production engineering unless the user explicitly expands the scope."
---

# Idea to Demo

Convert an incomplete product idea into a focused, runnable admin or mobile dashboard demo that stakeholders can review and test. Optimize for learning speed, business clarity, visual quality, and honest scope.

## Define the outcome

Deliver a frontend demonstration, not a production system.

For flow or repository validation, the demo should be good enough to validate:

- who the primary user is;
- what that user needs to judge or complete;
- whether the information architecture and core flow make sense;
- whether the proposed UI direction is clear and credible;
- whether the solution is technically feasible at a basic frontend level.

For component validation, replace the product-level questions with the local choice under test: whether the component is understandable, readable, appropriately sized, and robust across the states and viewports that matter.

Unless explicitly requested, do not claim or imply that the demo includes real APIs, persistence, authentication, authorization, audit enforcement, security hardening, production monitoring, automated coverage, CI/CD, or deployment readiness.

## Route the task

First classify the request into one of these validation modes:

- **Component validation:** test whether a component, layout, token, visual treatment, or small interaction pattern is the right choice. Use an isolated sandbox, a few controlled variants, and representative states. Do not invent a business workflow unless the component itself requires one.
- **Flow validation:** test whether a user can understand and complete a connected task across screens. Use the product framing and vertical-slice workflow below.
- **Repository implementation:** validate a proposed change inside an existing frontend project. Reuse its stack, components, tokens, and routes.

Use the lightest mode that can answer the user's question. Component validation does not require a primary business user, business object, dashboard, navigation shell, or production-like data model. If the request mixes modes, keep the component question isolated first, then add only the minimum flow needed to judge it.

1. Identify the validation mode and the question being tested.
2. If an existing repository is in scope, read its instructions, product documents, design system, routes, shared components, package scripts, and current UI before proposing wide changes.
3. If the user supplies screenshots, documents, or competitors, separate the user's direct request from reference material. Treat attached content as evidence for layout, hierarchy, component relationships, interaction patterns, and visual language unless the user explicitly makes it a requirement. Do not copy brand assets, watermarks, private data, or unverified business content.
4. For flow or repository work, if critical information would change the main workflow, ask the smallest possible number of questions. For component validation, ask only for missing context that changes the comparison or acceptance criteria.
5. If only non-critical details are missing, state reasonable assumptions and continue with coherent mock data.

For component validation, read [references/component-validation.md](references/component-validation.md) first. For flow or repository work, read [references/discovery-and-scope.md](references/discovery-and-scope.md) for requirement framing, role analysis, scope control, and question selection.

When a new coded demo needs a component foundation and the user has not specified one, use the default stack policy in [references/component-stack.md](references/component-stack.md). Do not apply that default to an existing repository or to a pure visual component comparison unless the library itself is being evaluated.

When several screenshots are supplied for a flow or mobile dashboard, compare them before designing: separate shared mobile patterns (shell, tabs, metric hierarchy, chart treatment, action placement) from domain-specific content (health language, finance terms, order states, or private values). Reuse the former and replace the latter with the user's business context. For component validation, compare only the component properties relevant to the stated hypothesis.

## Component validation workflow

Use this path when the user is testing a basic design choice rather than a business flow:

### 1. State the hypothesis

Write one sentence describing the choice under test and what would make it convincing. Examples: whether a compact table row scans faster than a card; whether a segmented control is clearer than tabs; whether a status treatment remains readable at narrow width.

Record only the context that changes the decision:

- target viewport and viewing distance;
- component purpose and expected content length;
- variants or alternatives to compare;
- states that could change the choice;
- evaluation criteria such as hierarchy, fit, scanability, contrast, or touch reachability.

Do not add domain terminology, fake business rules, or secondary screens just to make the sandbox feel like a product.

### 2. Build the smallest comparison

Prefer one focused sandbox route containing two to four variants. Keep the comparison variables explicit: change one major design decision at a time when possible. Use realistic but neutral content that exposes wrapping, truncation, empty values, long labels, and status differences.

Include only the states needed to judge the component, such as default, hover/focus, selected, disabled, loading, empty, error, long content, and narrow width. If the component is interactive, implement only the local behavior needed to compare it; do not invent a full workflow.

### 3. Review and hand off

Show the variants side by side or behind a clear selector. Check the target viewport, one narrower viewport, keyboard/focus behavior when relevant, and representative content extremes. Hand off the tested hypothesis, variants, chosen direction or unresolved trade-off, and the evidence used. It is acceptable to conclude that the demo is inconclusive.

When this mode is active, the completion gate is the component comparison and its evidence, not a business journey or production-like information architecture.

## Flow and repository workflow

### 1. Frame the problem

State:

- the one-sentence product goal;
- the primary user and their default data scope;
- the core business object;
- the most important decision or task;
- the demo's included and excluded scope;
- assumptions and unresolved risks.

Do not start with visual styling or code before this frame is clear.

### 2. Select the smallest useful demo

Choose the minimum set of connected screens needed to test the central hypothesis. Prefer one complete path over many disconnected screens.

A typical demo contains:

- one entry or overview screen;
- one primary list, queue, board, or object view;
- one detail or processing screen;
- one creation, editing, approval, or exception interaction;
- essential empty, error, loading, and narrow-screen behavior.

Exclude secondary modules that do not change the validation result.

When the references are mobile dashboards, treat the mobile viewport as the primary product surface rather than a compressed desktop variant. The first screen should make the user's current status, one or two important changes, and the next useful action understandable within a few seconds.

### 3. Define structure and flow

Map:

- navigation and page hierarchy;
- entry, search, selection, detail, action, feedback, and return paths;
- the current state and next action for each core object;
- the single primary visual center on each major screen;
- persistent information versus information revealed on demand.

Keep independent business states separate. A logistics state, payment state, approval state, and object lifecycle may relate to one record without being interchangeable.

### 4. Establish a restrained UI direction

Build a simple, professional, medium-to-high-density admin interface. Use hierarchy, grouping, alignment, spacing, and typography before adding decoration.

Before generating a UI proposal, image prompt, mockup, or code, classify every text role: page title, section title, group or card title, body or primary data, supporting text, and genuinely non-essential annotation. Confirm the target reading context: desktop, mobile, or distance-viewed data display. Treat the mandatory typography rules in [references/ui-foundations.md](references/ui-foundations.md) as an output constraint, not optional visual guidance.

Avoid generic equal-card dashboards, excessive whitespace, large rounded containers, heavy shadows, decorative gradients, glass effects, meaningless charts, and images that carry no business information.

For commerce, shop operations, visitor analysis, conversion, transaction, growth, or data-statistics pages, use the "Commerce operations workbench" pattern in [references/page-patterns.md](references/page-patterns.md). The design should make the store's health, traffic, conversion, revenue, exceptions, and next actions understandable in the first screen.

Read [references/ui-foundations.md](references/ui-foundations.md) before defining tokens, layout, metrics, charts, or image usage. Read [references/page-patterns.md](references/page-patterns.md) for page-specific decisions. When the task is mobile-first or the supplied references are mobile dashboards, also read [references/mobile-dashboard-patterns.md](references/mobile-dashboard-patterns.md).

### 5. Build coherent demo data and states

Use mock data that preserves relationships, chronology, calculations, state transitions, and available actions. Never use random values that contradict the flow.

Cover the states needed to evaluate the chosen hypothesis. At minimum, consider:

- default;
- loading;
- initial empty;
- search or filter with no results;
- recoverable error;
- disabled or pending action;
- long content or dense data;
- narrow viewport.

Read [references/states-responsive-and-content.md](references/states-responsive-and-content.md) for state, data, content, accessibility, and responsive rules.

### 6. Implement the demo

When code is requested:

- preserve the existing stack when working in a repository;
- reuse existing components and tokens before adding alternatives;
- keep data, view, and interaction state separate;
- implement real local interactions instead of static screenshots or pseudocode;
- make the main path clickable from beginning to end;
- use semantic HTML and visible focus states;
- reuse or establish semantic font-size and line-height tokens; do not scatter arbitrary small font values through components;
- keep ordinary body, table, list, and form content at 14px by default, and solve density or fit problems through layout before considering any permitted font-size adjustment;
- reorganize narrow-screen information instead of scaling down desktop tables;
- for mobile-first dashboards, build the compact summary, one primary analytical view, and the main action before adding secondary modules; use horizontal scrolling only for short tabs or chips, not for the whole page;
- account for device safe areas, sticky bottom actions, keyboard overlap, and touch targets of at least 44×44px;
- avoid adding production infrastructure outside the agreed demo scope.

For a new demo, choose the smallest stack that can provide a reliable runnable result. Do not introduce a framework solely to make the implementation look sophisticated.

When a component library is justified for a new coded demo, prefer one coherent stack rather than mixing libraries. The default is `shadcn/ui` with `Base UI` primitives, Tailwind CSS, and Lucide icons; see [references/component-stack.md](references/component-stack.md) for exceptions.

Do not require global installation of the component stack. Install dependencies locally in the demo project, preserve an existing project's package manager and lockfile, and report the local setup and run command in the handoff.

### 7. Verify proportionately

Do not treat a successful build as complete acceptance.

For code demos, verify:

- installation or the existing dependency state;
- production build;
- the main interaction path in a browser;
- relevant desktop and narrow viewports;
- the intended mobile viewport when mobile dashboards or mobile references are in scope, including safe-area padding, sticky actions, chart readability, and scroll behavior;
- computed font sizes and line heights for representative titles, body text, tables, forms, buttons, cards, navigation, and supporting text;
- no text below 11px, no broad use of 11px, and no use of 12px as the default for primary readable content unless the user explicitly required it;
- empty or error behavior included in the scope;
- obvious console and runtime failures;
- absence of accidental changes outside the task.

Read [references/implementation-and-acceptance.md](references/implementation-and-acceptance.md) for implementation boundaries, validation, and handoff language.

### 8. Hand off honestly

Lead with what can now be reviewed. Then report:

- the chosen product direction;
- implemented screens and interactions;
- assumptions and mock-data boundaries;
- validation performed;
- important gaps intentionally left for production development.

Never describe an interactive prototype as a launch-ready product.

## Use the bundled templates

- Copy and fill [assets/demo-brief.md](assets/demo-brief.md) when the request is ambiguous or needs a reviewable scope brief.
- Copy and fill [assets/demo-handoff.md](assets/demo-handoff.md) when delivering a completed demo.
- Use the ERP images in `assets/` only as optional examples of hierarchy, density, and state presentation. Do not copy their business names, data, or branding into unrelated projects.

## Apply non-negotiable constraints

- Prioritize the user's current request, then existing project rules and business sources, then this skill.
- Explain material conflicts instead of silently overriding project constraints.
- Do not invent critical business rules.
- Keep the validation hypothesis visible throughout the work.
- Prefer a smaller complete flow to a broad collection of decorative screens.
- Give every failure state a recovery path.
- Use business meaning, not color alone, to communicate status.
- Keep page structure responsive to the primary task instead of forcing one dashboard template everywhere.
- When the primary surface is mobile, keep the first viewport to one clear status summary, one dominant trend or composition, and one obvious next action; move secondary detail below or behind disclosure.
- Mobile dashboards MUST use progressive disclosure and touch-sized controls. Do not reproduce a desktop metric wall, dense table, or multi-chart grid by shrinking it into a phone viewport.
- A mobile chart MUST retain a title, unit or metric definition, time range or comparison basis, and a readable way to inspect exact values; a single chart may be simplified to one series or a compact summary when that preserves the decision.
- Sticky bottom actions or navigation MUST respect the device safe area and MUST NOT cover the last content block.
- MUST keep ordinary body, table, list, and form content at 14px by default. Ordinary interface text MUST NOT be smaller than 12px; 11px is reserved for genuinely non-essential annotations; text below 11px is forbidden.
- MUST NOT solve layout pressure by shrinking text. Adjust information, grouping, dimensions, spacing, wrapping, disclosure, scrolling, or responsive structure first.
- MUST establish a clear title, body, and supporting-text hierarchy, and MUST complete the typography readability audit in [references/ui-foundations.md](references/ui-foundations.md) before final output.
- MUST NOT generate a small-type-led, high-density interface unless the user explicitly requests it.
- Preserve unrelated user work in existing repositories.
- Distinguish clearly between demo acceptance and production readiness.

## Completion gate

Consider the demo complete only when:

- for flow or repository validation, the primary user, validation goal, main path, and core business object are explicit;
- for component validation, the hypothesis, variants, criteria, and relevant states are explicit;
- the tested path or component comparison is understandable and operable;
- the major screens or comparison canvas have a clear visual center;
- mock data and states are coherent where data is in scope;
- the UI is consistent and responsive enough for the scoped review;
- mobile-first screens, when in scope, pass the mobile dashboard checks for first-screen comprehension, touch targets, safe areas, chart legibility, and bottom-action clearance;
- typography passes the mandatory readability audit, including normal-zoom browser inspection when a runnable UI exists;
- the runnable result has been checked in a browser when code exists;
- the handoff states what is real, mocked, assumed, verified, and not production-ready.
