# Other Security Changes

## Overview

Additional security cleanup changes were called out in the release notes.

## Official Release Note

- [Security, Identity, and Privacy](https://help.salesforce.com/s/articleView?id=release-notes.rn_security.htm&language=en_US)

These are the smaller but still operationally important security adjustments that do not fit the larger security subsections.

## What changed

- Malformed trusted URLs can be identified and removed.
- Smaller Content Security Policy headers reduce failures when other sites serve content from your org.
- The release notes call out these changes as cleanup items for org hardening.

## Notes for Agents

- These changes help reduce edge-case configuration problems.
- If external sites are embedding or consuming your org, this page is worth checking for compatibility issues.
