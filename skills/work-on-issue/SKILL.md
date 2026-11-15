---
name: work-on-issue
description: Help a nontechnical user choose and implement an existing project issue, reuse relevant capabilities, and verify the result.
---

# Work on an issue

Find the issue the user named in the conversation, local drafts, or the project's existing tracker when available. If no issue is named, inspect the available issues and their dependencies, then recommend a useful next one. Ask the user to choose when the intended work is unclear or the options represent different product priorities.

Read the issue, its acceptance criteria, relevant PRD, and the relevant project code and conventions. Identify capabilities already present before choosing how to implement the change. Do not assume the project uses a particular database, authentication provider, framework, or hosting service. Resolve implementation details within the user's stated goal; ask about consequential product decisions that cannot be inferred.

Implement the selected issue within the user's authorization and existing project constraints. Verify the user-visible behavior and acceptance criteria with suitable checks, including a real workflow when practical. Report what changed, how to see or use it, what was verified, and any remaining limitation in plain language. Update the local issue's status or checklist if the project already uses one; do not mark work complete when acceptance criteria remain unmet. Do not publish tracker changes unless the user requests them.

If the user asks what a component or decision means, pause to follow [explain-this](../explain-this/SKILL.md), then continue the issue if appropriate.
