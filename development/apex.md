# Apex

## Overview

Apex gets a major security and runtime behavior update in Summer '26.

## What changed

- Database operations now run in user mode by default instead of system mode.
- SOSL, SOQL, DML, and Database methods enforce sharing rules, field-level security, and object permissions unless you explicitly switch to system mode.
- Apex classes without an explicit sharing declaration now default to with sharing in API version 67.0 and later.
- Apex triggers always run in system mode, so trigger handlers need to carry any sharing or access-mode logic.
- SOQL and SOSL code that still uses WITH SECURITY_ENFORCED must move to WITH USER_MODE.
- Integration Apex tests can make real callouts to Agentforce and Data 360.
- Queueable and future method jobs can now go up to an elastic limit that is twice the org's licensed daily async limit.
- Multiline strings are supported without repeated string concatenation.
- String interpolation now uses String.template() instead of String.format() for regular and multiline strings.
- Managed-package anonymous Apex execution is blocked by the Block Apex Anonymous Code Execution from Managed Packages release update.

## Security model details

- Explicit access modes are now the safest way to make Apex database behavior obvious.
- Use WITH USER_MODE or WITH SYSTEM_MODE for SOQL and SOSL.
- Use as user or as system for DML.
- Use the accessLevel parameter with Database.query() and Search methods.
- If you omit a sharing declaration on an Apex class, API 67.0 and later classes default to with sharing.

## Notes for Agents

- User-mode-by-default is the biggest breaking-change risk in this area.
- The string feature change is specifically about String.template() and multiline literals, not a general interpolation overhaul.
