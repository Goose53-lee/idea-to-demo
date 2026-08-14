# Page patterns

Use this reference when selecting or implementing common admin page structures.

Apply the mandatory type hierarchy and component minimums in [ui-foundations.md](ui-foundations.md) to every pattern below. Density MUST come from column priority, grouping, disclosure, and responsive transformation rather than undersized text.

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

### Commerce operations workbench

Use this pattern for shop homepages, platform seller consoles, visitor analysis, transaction statistics, search analysis, growth centers, and data-statistics pages.

The first screen should answer:

- Is the store healthy today?
- Where did traffic come from?
- Which step of the funnel is improving or leaking?
- What transactions, after-sales, violations, or tasks need attention?
- Which action should the operator take next?

Common structure:

```text
Global shell and search
Store or account scope, time range, and update time
Top KPI strip for pending work, traffic, conversion, orders, revenue, after-sales, or risk
Main analytics area: funnel, trend, ranking, or comparison
Operational queue: todos, warnings, campaign tasks, growth suggestions, or service exceptions
Detailed records or drill-down list
```

Use the module set according to the user's goal:

- **Store overview:** pending orders, shipment, after-sales, violations, rating, guarantee/deposit, active campaigns, and next actions.
- **Visitor analysis:** visitors, page views, source channels, product views, search words, new versus returning visitors, and retention or revisit signals.
- **Transaction statistics:** paid orders, paid amount, conversion rate, customer unit price, refund or after-sales rate, unpaid risk, and period comparison.
- **Search or content analysis:** search terms, hot keywords, ranking changes, video or content exposure, click-through, and related products.
- **Growth tasks:** current level, gap to target, recommended action, reward or impact, due date, and completion state.

Design rules:

- Put four to six critical KPIs at the top; make one or two primary values visibly stronger than secondary values.
- Keep time range, comparison basis, and metric definitions close to the chart or KPI they affect.
- Use tabs or segmented controls for business modes such as overall transaction, self-operated transaction, cooperative transaction, hot keywords, or hot videos.
- Use line charts for trend, bars for ranking or distribution, progress for goal completion, and tables for actionable records.
- Show comparison direction with both color and text; a rising refund, complaint, violation, or timeout rate is negative.
- Attach actions to insights: view details, handle after-sales, publish content, register campaign, optimize product, download details, or clear filters.
- Keep right rails for short todos, risk alerts, campaign reminders, and growth tasks. Move complex analysis into the main area.
- Use realistic platform data relationships instead of random dashboard numbers. Totals, percentages, and trend labels must reconcile.
- On mobile, keep the top health summary and one primary action first, then convert charts to compact summaries and records to cards.

Avoid:

- a static "data wall" that has metrics but no decision or next action;
- unrelated charts that do not connect to traffic, conversion, transaction, service, content, or risk;
- copying platform names, logos, watermarks, or exact private values from references;
- hiding important metric definitions or update times;
- using visual polish to obscure low contrast, tiny text, cramped tables, or unclear state meaning.

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

Keep table body text at 14px by default, table headers at 13–14px, and secondary fields, status tags, and row actions at 12px or larger. When columns do not fit, prioritize, wrap, disclose, or scroll before adjusting type.

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

Keep input values and labels at 14px by default, validation and help text at 12px or larger, and button text within the component minimums. On mobile, prefer 16px input text and restructure the form instead of shrinking it.

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
