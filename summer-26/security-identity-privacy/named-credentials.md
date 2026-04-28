# Named Credentials

## Overview

Named credentials now use the org's My Domain name when creating an external auth identity provider.

That makes the callback and auth setup more consistent with the org's branded domain.

## What changed

- Callback URLs are constructed using My Domain.
- The behavior helps standardize external auth setup across branded orgs.

## Notes for Agents

- This is a small but important integration hardening change.
- If an integration relies on a callback URL, verify the My Domain value before migrating or regenerating the auth provider.
