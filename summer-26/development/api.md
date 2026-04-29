# API

## Overview

API version 67.0 introduces security, sharing, and GraphQL-related changes.

## Official Release Note

- [API](https://help.salesforce.com/s/articleView?id=release-notes.rn_api.htm&language=en_US)
- [Hosted MCP Servers](https://help.salesforce.com/s/articleView?id=release-notes.rn_api_hosted_mcp_servers_ga.htm&language=en_US)
- [Context MCP Server](https://help.salesforce.com/s/articleView?id=release-notes.rn_api_context_mcp_server_beta.htm&language=en_US)
- [Named Query API](https://help.salesforce.com/s/articleView?id=release-notes.rn_api_named_query_ga.htm&language=en_US)
- [SOAP JWT](https://help.salesforce.com/s/articleView?id=release-notes.rn_api_soap_jwt.htm&language=en_US)
- [SOQL WHERE](https://help.salesforce.com/s/articleView?id=release-notes.rn_api_soql_where.htm&language=en_US)
- [OpenAPI for sObjects REST API](https://help.salesforce.com/s/articleView?id=release-notes.rn_api_rest_openapi_spec_beta.htm&language=en_US)

## What changed

- Version 67.0 introduces support for the new Apex access-mode defaults and removes `WITH SECURITY_ENFORCED` from classes compiled at 67.0 and later.
- REST API calls now validate that custom Apex classes used as invocable action parameters have visible no-argument constructors in API version 66.0 and later.
- SOAP API `login()` is being retired in versions 31.0 through 64.0 for Summer '27 and later.
- GraphQL API adds support for new item-level capabilities in the development section and is referenced alongside updated LWC wire-adapter modules.

## Notes for Agents

- If you are versioning API-dependent code, verify sharing behavior, constructor visibility, and authentication flows before upgrading.
