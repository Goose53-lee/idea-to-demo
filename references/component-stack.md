# Component stack policy

Use this reference when a new coded demo needs a component foundation.

## Default preset

Prefer:

```text
shadcn/ui + Base UI + Tailwind CSS + Lucide
```

Use shadcn/ui as the project-owned visual and component-code layer. Use Base UI for unstyled accessible interaction primitives such as dialogs, popovers, menus, selects, tabs, and tooltips. Use Tailwind CSS for local styling and tokens, and Lucide for consistent interface icons.

This preset is a default for new flow demos and repository-free prototypes, not a mandatory dependency for every task.

## Installation scope

- Do not require users to install these libraries globally on their computer.
- Install required packages in the specific demo project's local dependency set.
- A usable Node.js runtime and package manager such as npm, pnpm, yarn, or bun are sufficient prerequisites.
- `shadcn/ui` is project-owned component source rather than a global runtime library; initialize or add its components inside the project.
- Existing repositories should use their current lockfile and package manager. Do not add a second package manager or reinstall dependencies unnecessarily.
- If the environment can install dependencies, the demo setup may do so during project initialization. Report what was installed locally and how to run the project.

## Selection rules

- **Existing repository:** preserve its component library, primitives, tokens, and icon system. Do not migrate to this preset only for visual preference.
- **Component validation:** do not add a full component library by default. Use the smallest local primitives that let the comparison answer the question. Use shadcn/ui when its visual language is the thing being tested; use Base UI primitives when behavior and accessibility are the thing being tested.
- **New flow demo:** use the preset when forms, tables, dialogs, menus, filters, or repeated states would otherwise be rebuilt several times.
- **Custom visual system:** Base UI alone is acceptable when the purpose is to establish a bespoke visual language and the extra styling work is part of the test.
- **Existing Radix project:** keep Radix and its surrounding conventions. Do not mix Base UI and Radix for the same primitive family.

## Boundaries

- Do not introduce a component library only to make a tiny sandbox appear more sophisticated.
- Do not mix multiple full component libraries in one demo.
- Keep the source understandable and editable; do not hide important behavior behind opaque wrappers.
- If a library default conflicts with the tested visual hypothesis, change or replace the local component instead of treating the library default as a requirement.

## References

- [shadcn/ui](https://ui.shadcn.com/docs)
- [Base UI](https://base-ui.com/react/overview/about)
