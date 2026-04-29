# Identity and Access Management

## Overview

Identity and access management gets stronger SSO visibility and retirement updates.

## Official Release Note

- [Security, Identity, and Privacy](https://help.salesforce.com/s/articleView?id=release-notes.rn_security.htm&language=en_US)

## Related help

- [Upgrade Einstein Activity Capture Authentication from EWS to Microsoft Graph](https://help.salesforce.com/s/articleView?id=sales.eac_ews_graph.htm&type=5&language=en_US)
- [Move from Lightning Sync to Einstein Activity Capture](https://help.salesforce.com/s/articleView?id=sales.lightning_sync_move_parent.htm&type=5&language=en_US)

## What changed

- Login history and login events expose Authentication Context Class Reference values from SSO providers.
- The OAuth 2.0 username-password flow for connected apps is being retired.
- The multiple-configuration SAML framework replaces the older single-configuration framework.
- Triple DES is no longer supported for SAML single sign-on.
- The net result is stricter and more observable identity plumbing across SSO and connected-app auth.
- Identity changes here are mostly about better auditability and retiring older authentication patterns.

## Notes for Agents

- This is the main SSO and auth subsection to monitor.
- Use this page when the change affects authentication protocols, login telemetry, or connected-app sign-in behavior.
- The related help is mainly useful when you need the migration path off older email-sync or auth approaches.
