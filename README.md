# Salesforce Release Notes

This repository contains agent-friendly Markdown extracts of Salesforce release notes.

The structure is intentionally flat and searchable so an agent can parse the Markdown here instead of navigating the official Salesforce release notes UI, which relies on embedded frames and layered navigation.

## Structure

- Each Salesforce release lives in its own top-level folder, such as `summer-26/`.
- Each release folder contains concise Markdown summaries organized by product area and topic.
- New releases should be added as new sibling folders at the repository root.

## Current Release

- [Summer '26](summer-26/README.md)

## Purpose

The goal of this repo is to make Salesforce release notes easier for agents and developers to browse, search, and reuse without parsing the original source documents.

If a topic looks sparse, check the linked release folder first and then the release-note-changes page. Those entries usually carry the extra context needed to tell whether a note is a new capability, a correction, or an availability update.

## Conventions

- Keep release content focused, concise, and Markdown-first.
- Prefer one folder per release.
- Add a short README in each release folder that points to the release-specific summaries.
- Use descriptive file names that match the Salesforce product or topic they summarize.
