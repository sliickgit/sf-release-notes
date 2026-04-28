# API

## Overview

API version 67.0 introduces security, sharing, and GraphQL-related changes.

## What changed

- Version 67.0 introduces support for the new Apex access-mode defaults and removes `WITH SECURITY_ENFORCED` from classes compiled at 67.0 and later.
- REST API calls now validate that custom Apex classes used as invocable action parameters have visible no-argument constructors in API version 66.0 and later.
- SOAP API `login()` is being retired in versions 31.0 through 64.0 for Summer '27 and later.
- GraphQL API adds support for new item-level capabilities in the development section and is referenced alongside updated LWC wire-adapter modules.

## Notes for Agents

- If you are versioning API-dependent code, verify sharing behavior, constructor visibility, and authentication flows before upgrading.
