# Canonical Time Zones

## Overview

Salesforce supports additional canonical time zones in Summer '26.

This helps orgs stay aligned with standardized IANA time zone names instead of relying on older or org-specific representations.

## What changed

- 27 additional canonical time zones are supported.
- The time zones align with IANA standards.
- The change is especially useful for orgs with global teams, scheduled automations, or integrations that need consistent time-zone behavior.

## Notes for Agents

- This matters most for orgs with global users and date-sensitive automations.
- If you see a scheduling issue or a time-zone mismatch, check whether a canonical time zone now exists for the region.
