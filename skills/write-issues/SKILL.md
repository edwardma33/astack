---
name: write-issues
description: Break a PRD or agreed feature description into local, ordered implementation issue drafts with observable acceptance criteria.
---

# Write issues

Read the PRD or agreed requirements and inspect enough of the project to identify existing capabilities and meaningful dependencies. If the source is unclear or lacks a consequential product decision, ask the user rather than inventing a requirement. A PRD is helpful but not required when the user has provided sufficient context.

Create a small set of ordered issues that an agent can work on individually. Prefer complete, user-visible slices where practical. For each issue include a descriptive title, the outcome and why it matters, observable acceptance criteria, and dependencies or relevant project context when needed. Keep implementation suggestions subordinate to the outcome and avoid prescribing a particular stack without evidence.

Use the user's requested location or an established project convention. Otherwise write one Markdown file per issue in `docs/astack/issues/`, with numbered descriptive filenames. Inspect existing drafts first. Preserve unrelated files and update matching drafts rather than creating duplicates when practical. If a filename belongs to unrelated work, choose a distinct name. Link to the source PRD when one exists.

Report the issue locations and suggested starting issue. These are local drafts; do not create or update tracker issues unless the user explicitly asks.
