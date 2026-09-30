# Discovery and scope

Use this reference before deciding pages, flows, or implementation scope.

## Contents

- Product frame
- Role model
- Scope selection
- Flow and state contracts
- Reference design extraction
- Questions and assumptions
- Demo boundary

## Product frame

Extract the following from the user's request and available source material:

- Product name and industry context.
- Primary user and secondary stakeholders.
- Core business object, such as an order, project, refund, customer, device, or task.
- The job the primary user must complete.
- The decision they need to make within the first ten seconds.
- Success criteria for the demo review.
- Upstream and downstream objects or screens.
- Known technical, data, brand, or time constraints.

Express the result as one concise problem statement:

```text
For <primary user>, help them <complete or judge the core task>
by organizing <business objects and states>, so the team can validate
<specific product hypothesis> before production development.
```

## Role model

Do not stop at role names. Map each role to attention, frequent tasks, and default data scope.

| Role mode | Primary attention | Frequent task | Typical default scope |
| --- | --- | --- | --- |
| Decision | outcomes, risk, trend, resources | compare and decide | organization or portfolio |
| Coordination | todos, schedule, exceptions, handoffs | assign and unblock | team or active work |
| Execution | current object, next step, local evidence | process and record | personal or assigned work |

Reuse business components across roles when useful, but vary ordering, visual center, default filters, and shortcuts according to the role.

## Scope selection

Choose screens by validation value, not by product completeness.

For each proposed screen, ask:

1. What hypothesis does this screen test?
2. What decision or action occurs here?
3. Does the core path break without it?
4. Can it be represented as a state, drawer, dialog, or section instead?

Classify screens as:

- **Core:** required for the review path.
- **Supporting:** explains or completes the core path.
- **Deferred:** valuable later but not needed for the current decision.

Default to one connected vertical slice. A useful slice often includes an overview, an object list or queue, a detail, and one meaningful action.

## Flow and state contracts

Write the core flow as observable steps:

```text
Enter scope
→ find or filter an object
→ inspect context and current state
→ perform the next valid action
→ receive success or failure feedback
→ return to a predictable updated state
```

For each business object, define independently:

- state name;
- meaning;
- entry condition;
- permitted actions;
- next possible states;
- responsible role;
- time or evidence shown;
- recovery or escalation path.

Do not merge separate state dimensions merely to simplify the UI. Show relationships without erasing their semantics.

## Reference design extraction

When screenshots, live products, or competitors are supplied, extract:

- shell and navigation model;
- first-screen hierarchy and primary visual center;
- main-to-supporting area proportions;
- component relationships;
- density and spacing rhythm;
- color, border, radius, shadow, icon, and image behavior;
- interactions that can transfer to the current task;
- brand, content, or business details that must not transfer.

Treat references as structural and visual evidence, not as a requirements document.

## Questions and assumptions

Ask only questions whose answers materially change:

- the primary user;
- the core business object;
- the main flow;
- the data or permission boundary;
- the required platform;
- the validation outcome.

Group related questions and prefer one to three concise questions. Continue with explicit assumptions when missing details only affect labels, sample values, secondary filters, or non-critical styling.

Never silently invent irreversible actions, legal rules, financial calculations, permission policy, or compliance behavior.

## Demo boundary

Include only what is necessary to test the proposed direction.

The demo may include:

- runnable frontend pages;
- local interaction state;
- coherent mock data;
- simulated loading, error, success, and permissions;
- representative responsive behavior;
- basic exports or uploads that are clearly simulated.

The demo does not prove:

- API contracts or database integrity;
- real authentication, authorization, or data isolation;
- audit immutability;
- security, privacy, compliance, or accessibility certification;
- production performance and resilience;
- automated test coverage or release readiness.

Record excluded production concerns in the final handoff instead of hiding them.
