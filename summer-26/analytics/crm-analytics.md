# CRM Analytics

## Overview

CRM Analytics includes dashboard, lens, analytics app, and data integration updates.

The concrete release-note changes in this area are about how data is written out and how external data targets are handled.

## What changed

- Optimized append, upsert, and delete actions improve write performance when writing to existing Data Lake Objects.
- Output to Azure Data Lake is generally available through the Azure Data Lake output connector.
- Recipe results can now be written to an output connection for downstream use, which makes it easier to pass transformed data to other systems.

## Notes for Agents

- The output and write-performance changes are the concrete implementation items in this area.
- If the question is about how CRM Analytics exports or persists transformed data, this is the key page to read.
- This page is the best summary when the issue is write performance or downstream data export from CRM Analytics.
