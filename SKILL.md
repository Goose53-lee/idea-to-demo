---
name: idea-to-demo
description: Turn rough product ideas, requirements, PRDs, screenshots, or existing frontend repositories into clean, runnable, interactive admin and back-office demos for early validation. Use for workbenches, dashboards, ERP, CRM, management consoles, lists, details, forms, and related responsive demo flows when the user wants a concise, feasible UI direction rather than a production delivery. Focus on frontend demos with coherent mock data and core interactions; do not present the result as production-ready or use this skill for backend, security, deployment, or full production engineering unless the user explicitly expands the scope.
---

# Idea to Demo

Convert an incomplete product idea into a focused, runnable admin demo that stakeholders can review and test. Optimize for learning speed, business clarity, visual quality, and honest scope.

## Define the outcome

Deliver a frontend demonstration, not a production system.

The demo should be good enough to validate:

- who the primary user is;
- what that user needs to judge or complete;
- whether the information architecture and core flow make sense;
- whether the proposed UI direction is clear and credible;
- whether the solution is technically feasible at a basic frontend level.

Unless explicitly requested, do not claim or imply that the demo includes real APIs, persistence, authentication, authorization, audit enforcement, security hardening, production monitoring, automated coverage, CI/CD, or deployment readiness.

## Route the task

1. Inspect the supplied inputs.
2. If an existing repository is in scope, read its instructions, product documents, design system, routes, shared components, package scripts, and current UI before proposing wide changes.
3. If the user supplies screenshots or competitors, extract layout, hierarchy, component relationships, interaction patterns, and visual language. Do not copy brand assets, watermarks, private data, or unverified business content.
4. If critical information would change the main workflow, ask the smallest possible number of questions.
5. If only non-critical details are missing, state reasonable assumptions and continue with coherent mock data.

Read [references/discovery-and-scope.md](references/discovery-and-scope.md) for requirement framing, role analysis, scope control, and question selection.

## Follow the workflow

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

Avoid generic equal-card dashboards, excessive whitespace, large rounded containers, heavy shadows, decorative gradients, glass effects, meaningless charts, and images that carry no business information.

Read [references/ui-foundations.md](references/ui-foundations.md) before defining tokens, layout, metrics, charts, or image usage. Read [references/page-patterns.md](references/page-patterns.md) for page-specific decisions.

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
- reorganize narrow-screen information instead of scaling down desktop tables;
- avoid adding production infrastructure outside the agreed demo scope.

For a new demo, choose the smallest stack that can provide a reliable runnable result. Do not introduce a framework solely to make the implementation look sophisticated.

### 7. Verify proportionately

Do not treat a successful build as complete acceptance.

For code demos, verify:

- installation or the existing dependency state;
- production build;
- the main interaction path in a browser;
- relevant desktop and narrow viewports;
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
- Preserve unrelated user work in existing repositories.
- Distinguish clearly between demo acceptance and production readiness.

## Completion gate

Consider the demo complete only when:

- the primary user and validation goal are explicit;
- the main path is understandable and operable;
- the major screens have a clear visual center;
- mock data and states are coherent;
- the UI is consistent and responsive enough for the scoped review;
- the runnable result has been checked in a browser when code exists;
- the handoff states what is real, mocked, assumed, verified, and not production-ready.
