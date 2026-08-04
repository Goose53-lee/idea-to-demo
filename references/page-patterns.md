# Page patterns

Use this reference when selecting or implementing common admin page structures.

## Contents

- Workbench and dashboard
- Lists and tables
- Details
- Forms
- Authentication
- Upload and import
- Dialogs and drawers
- Empty and result states

## Workbench and dashboard

A workbench combines what the current user must judge and handle. It is not a collection of charts.

For decision roles, prioritize outcomes, risks, trends, and resources. For coordination and execution roles, prioritize todos, exceptions, active objects, schedules, and next actions.

Useful compositions include:

```text
Metrics + main business area + right-side todos or risks
Range filters + wide process or timeline + risk summary
Central business object + attributes, state, evidence, and actions
```

Limit top metrics to four to six useful values. Keep one dominant flow, object, or analytical view. Place short alerts and quick actions in a side rail; keep complex comparison in the main region.

A data dashboard supports judgment and analysis. Organize it as title and range, core metrics, exceptions, primary trend or process, composition, rankings, detail, and data definitions. Do not confuse it with a shortcut-heavy workbench.

## Lists and tables

Use the stable sequence:

```text
Page title or breadcrumb
High-frequency filters
Toolbar and primary action
Table or business-card list
Pagination or loading control
```

Show high-frequency filters by default and place low-frequency conditions behind an advanced control. Keep active filters visible. Support Enter to search when appropriate.

Prioritize columns as:

1. primary identifier;
2. core business attributes;
3. state;
4. time;
5. owner;
6. actions.

Make the primary column wider. Truncate long values with a reliable way to inspect the full content. Keep the action column stable. If more than three row actions exist, expose the most important ones and group the rest.

Dangerous actions need confirmation. Batch actions should appear only after selection.

On narrow screens, replace wide tables with business cards containing the title, identifier or time, essential fields, state, key number, and main action.

## Details

The detail header must answer:

- What object is this?
- What state is it in?
- What can the user do next?

A common structure is:

```text
Back or breadcrumb
Object identity, state, owner, time, and primary action
Compact summary
Process or important status context
Tabs or anchors
Business sections
Related records, attachments, and audit history
```

Use inline expansion for small information, a drawer for medium detail that benefits from retaining list context, and a full page for complex information or multi-step operations.

Keep read-only and editable regions visually distinct. Use stable business identifiers across related modules.

## Forms

Choose the container by complexity:

- dialog for a single goal with few fields;
- drawer for medium editing while retaining context;
- full page for many groups, conditional fields, uploads, nested tables, drafts, or multi-step work.

Prefer one column for simple forms. Use two columns only when related fields remain visually adjacent. Group forms beyond six to eight fields.

Validate lightly during input, validate individual fields after blur, and validate the full form on submit. Place errors near the field and preserve entered content after failure. Scroll long forms to the first error.

Use Cancel plus one primary action. Fix the action bar for long forms. Warn before leaving unsaved work.

## Authentication

Use a restrained centered or split layout. Keep one primary action. Label third-party sign-in methods with names, not icons alone.

Consider password login, code login, countdown, forgotten password, agreement consent, pending state, wrong credentials, missing or frozen account, no permission, and network failure.

Treat authentication in a demo as simulated unless real identity integration is explicitly in scope.

## Upload and import

An upload area should show allowed formats, size and count limits, files, progress, success, failure, replacement, deletion, and retry.

For spreadsheet import, provide a template, field rules, progress, success and failure counts, and a way to inspect or export errors. Clearly label local simulation when no backend exists.

## Dialogs and drawers

Use specific action titles. Keep headers and footers fixed when content scrolls. Explain the target and consequence of dangerous actions.

Use tooltips for short explanations, popovers for lightweight controls, and drawers for medium-complexity detail or editing. Avoid opening multiple nested floating layers.

## Empty and result states

Distinguish:

- first-use or initial empty;
- search with no results;
- filters with no results;
- an empty subsection;
- no permission;
- network failure;
- successful completion;
- processing or delayed results.

Use a specific title, explanation, and recovery action. Preserve table headers for table empty states. Do not use generic copy such as “No data” when the user needs to know what is missing and how to proceed.
