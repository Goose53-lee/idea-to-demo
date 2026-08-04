# Implementation and acceptance

Use this reference when modifying code, validating a runnable demo, or preparing the final handoff.

## Contents

- Existing repositories
- New demos
- Component structure
- Validation matrix
- Demo Definition of Done
- Production gap statement

## Existing repositories

Before changing an existing project:

1. Read the nearest project instruction files.
2. Inspect product and design documents.
3. Inspect the package manager, scripts, routing, data layer, shared components, tokens, and active styles.
4. Check the current Git state and preserve unrelated user changes.
5. Run or inspect the real UI before making broad visual decisions when practical.

Prefer narrow changes that extend the current system. Do not replace the framework, component library, routing, or visual language without explicit scope and evidence.

After changes, list the modified files and the effect of each meaningful change.

## New demos

Choose the smallest dependable frontend stack that supports the required interaction. A demo can use React, Next.js, Vite, or a simpler stack when appropriate.

Include only dependencies that materially improve delivery. Use a consistent icon library and a real chart library only when charts are needed. Avoid introducing backend infrastructure for simulated behavior.

Keep demo source understandable enough for the next team to evaluate or replace. A prototype may be temporary without being careless.

## Component structure

Separate:

- shell and navigation;
- page structure;
- reusable UI primitives;
- business components;
- mock data and types;
- interaction state;
- formatting utilities.

Common reusable components include:

```text
AppShell
Sidebar
Topbar
PageHeader
FilterBar
DataTable
MetricCard or MetricStrip
StatusTag
EmptyState
FormSection
DetailSection
ChartCard
MobileBottomNav
```

Do not create a universal abstraction before repeated structure is visible. Do not copy the same component implementation across pages when configuration would be clearer.

## Validation matrix

Select checks proportionate to the demo and record the result.

| Area | Minimum evidence |
| --- | --- |
| Build | project build or equivalent succeeds |
| Runtime | main route opens without obvious failure |
| Main flow | entry through the key action is operable |
| States | scoped empty, loading, error, or pending behavior can be seen |
| Responsive | representative desktop and narrow viewport checked |
| Visual | screenshot or browser inspection confirms hierarchy and fit |
| Console | no obvious uncaught errors on checked routes |
| Repository | unrelated changes preserved and task boundary reported |

A build alone proves packaging, not product quality. Code inspection alone does not prove responsive layout or interaction behavior.

## Demo Definition of Done

### Product

- Primary user and central task are explicit.
- The page set forms one coherent validation path.
- Upstream and downstream relationships are understandable.
- Assumptions and deferred questions are visible.

### States and interaction

- The main path is operable.
- Important state changes have feedback.
- Dangerous simulated actions use confirmation.
- Core failures have recovery paths.
- Long content and relevant edge data do not destroy the layout.

### Visual

- Each main page has one clear visual center.
- Typography, spacing, color, radius, borders, and icons are consistent.
- The UI is restrained, professional, and appropriately dense.
- Images and charts carry information rather than decoration.

### Engineering

- The demo runs using the documented command.
- Core components are reusable enough for the current demo.
- The scoped responsive behavior works.
- Obvious runtime errors are resolved.
- Existing project structure and unrelated work are preserved.

## Production gap statement

End every coded demo handoff with a concise boundary statement. Adapt this template:

```text
This deliverable is an interactive frontend demo for early product validation.
It uses mock or locally simulated data unless otherwise stated. Production work
still requires confirmed API contracts, persistence, authentication and RBAC,
audit and error handling, security and privacy review, automated tests,
performance validation, monitoring, CI/CD, and deployment acceptance.
```

Do not use phrases such as “ready to launch,” “production complete,” or “fully implemented” unless those claims were separately verified within explicit scope.
