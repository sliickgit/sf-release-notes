---
name: sf-lwc
description: Use when building Lightning Web Components for current Salesforce release changes such as Live Preview, API version shifts, Lightning Web Security updates, accessibility updates, base component changes, and large-list behavior.
---

# SF LWC

Use this skill when building or refactoring Lightning Web Components against the current Salesforce feature set.

## Build With These Defaults

- Pin the component API version when behavior matters.
- Use Live Preview or Single Component Live Preview to verify changes quickly.
- Keep state explicit and local unless you truly need shared orchestration.
- Prefer base components before custom markup.
- Design with accessibility and right-to-left behavior in mind.

## Release Guardrails

- Watch for Lightning Web Security distortion changes when code depends on browser APIs or DOM assumptions.
- Expect base component updates such as `lightning-combobox`, `lightning-file-upload`, `lightning-input`, `lightning-dual-listbox`, and `lightning-tree-grid`.
- Use the new dynamic list behavior only when the UI needs to handle large collections without blocking.
- Keep file uploads and form patterns aligned with the updated component limits and states.
- Use grouped `<details>` behavior only when you need mutually exclusive expanders.

## Quick Patterns

- For a component that must behave the same in release preview and production, test it at the pinned API version before you ship.
- For data-heavy UIs, prefer the dynamic list pattern instead of hand-rolled DOM rendering loops.
- For forms, use updated base component states before building custom input behavior.
- For browser API access, re-check any code that depends on native DOM details after LWS changes.
- For long lists, file uploads, or tree grids, test keyboard flow and screen-reader behavior in addition to visual rendering.

## Test It

- Verify component behavior in preview and local build paths.
- Check accessibility, keyboard flow, and RTL rendering.
- Re-test any browser API or DOM assumptions after enabling LWS-sensitive code paths.
- Recheck base component edge cases whenever you move the component API version.
