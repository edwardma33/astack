---
name: write-prd
description: Write or update a local product requirements document for an app or feature from a user's idea and project context.
---

# Write a PRD

A PRD is a product requirements document: a shared description of what to build and why. Use the conversation and inspect relevant project material before writing. If essential product decisions are missing, ask focused questions or follow [shape-idea](../shape-idea/SKILL.md). Do not invent user decisions and present them as facts.

Write for a nontechnical project owner and an agent that will implement the work. Describe the problem, intended users, desired outcome, main user journeys, first-version requirements, what is outside that version, and how success can be observed. Include constraints, dependencies, and open questions only where relevant. Separate confirmed decisions from assumptions. Describe technical details only when they affect the product or constrain the work.

Use the user's requested path or an established project convention. Otherwise use `docs/astack/PRD.md` relative to the project root. Inspect an existing file first and update it in place without erasing unrelated content. Do not overwrite an unrelated document. If the target conflicts with another artifact, choose a descriptive neighboring path and report it.

Report the file location, important assumptions, and decisions that still need the user's input. Create issue drafts only if requested or when following [write-plan](../write-plan/SKILL.md).
