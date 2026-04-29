---
name: sf-apex
description: Use when building Apex for current Salesforce release changes such as user-mode defaults, sharing defaults, removed WITH SECURITY_ENFORCED, elastic async limits, String.template(), and integration tests.
---

# SF Apex

Use this skill when writing Apex that must fit the current Salesforce runtime and security model.

## Build With These Defaults

- Treat user mode as the default shape for user-facing code.
- Put `with sharing` or `inherited sharing` on the public boundary.
- Use `WITH USER_MODE` for SOQL and `AccessLevel.USER_MODE` for DML when the user should only see what they can access.
- Keep triggers thin and move logic into services.
- Prefer typed `@AuraEnabled` request and response DTOs for LWC-facing Apex.
- Query only the fields the code actually uses.

## Release Guardrails

- Do not rely on `WITH SECURITY_ENFORCED`; use user mode instead.
- Remember that triggers still run in system mode, so handlers must enforce any access boundary they need.
- If the code must touch package-owned or internal data, isolate that in the smallest possible service boundary.
- If you need an async increase, use the elastic limit intentionally and only for work that can actually scale with it.

## Quick Patterns

- For an LWC controller, accept one DTO request object, call one service method, and return one DTO response object.
- For a user-facing query, keep the `WITH USER_MODE` clause near the query so the boundary is obvious.
- For user-facing DML, decide once whether the operation is `as user` or `as system` and keep that choice in the service layer.
- For strings, use multiline literals and `String.template()` instead of concatenation-heavy formatting.
- For integration coverage, use real callouts only when the feature depends on Agentforce or Data 360 connectivity.

## Test It

- Add non-admin `System.runAs` coverage when sharing, permissions, or user-mode behavior matter.
- Cover both positive and negative access paths.
- Add bulk coverage when the code operates on collections or trigger contexts.
- Add callout or integration tests only when the feature actually depends on them.
- Include at least one test that proves the default access mode is the one you intended.
