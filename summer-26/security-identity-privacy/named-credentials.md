# Named Credentials

## Overview

Named credentials now use the org's My Domain name when creating an external auth identity provider.

## Official Release Note

- [Named Credentials](https://help.salesforce.com/s/articleView?id=release-notes.rn_sf_connect_xorg_named_credentials.htm&language=en_US)

That makes the callback and auth setup more consistent with the org's branded domain.

## What changed

- Callback URLs are constructed using My Domain.
- The behavior helps standardize external auth setup across branded orgs.

## Notes for Agents

- This is a small but important integration hardening change.
- If an integration relies on a callback URL, verify the My Domain value before migrating or regenerating the auth provider.
