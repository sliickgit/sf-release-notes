# Salesforce Connect Cross-Org Adapter

## Overview

The cross-org adapter now supports named credentials.

This gives cross-org integrations a more robust and secure authentication path.

## Official Release Note

- [Build More Secure Integrations with Cross-Org Adapter Support for Named Credentials](https://help.salesforce.com/s/articleView?id=release-notes.rn_sf_connect_xorg_named_credentials.htm&language=en_US)

## Related help

- [Create an External Client App](https://help.salesforce.com/s/articleView?id=xcloud.create_a_local_external_client_app.htm&type=5&language=en_US)
- [Define an External Data Source for Salesforce Connect Cross-Org Adapter](https://help.salesforce.com/s/articleView?id=platform.xorg_add_external_data_source.htm&type=5&language=en_US)

## What changed

- Named credentials provide a more robust and secure authentication path.
- The release intro explicitly calls out this update as part of the effort to improve cross-org authentication.
- The practical change is that cross-org data access can rely on a clearer auth boundary instead of older, less structured credential handling.
- The setup path now points you toward the named-credential and external-data-source configuration that the adapter expects.

## Notes for Agents

- This is the main integration-hardening update in the section.
- Use named credentials when you need a cleaner auth boundary for Salesforce Connect cross-org access.
- If a cross-org connector was previously hard to reason about from a security standpoint, this is the page that explains the improvement.
- The core effect is simpler, more auditable authentication for cross-org integration traffic.
