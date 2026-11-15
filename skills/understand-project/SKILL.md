---
name: understand-project
description: Explain how an existing app and its parts fit together to a nontechnical project owner, based on evidence from the project.
---

# Understand the project

Inspect the relevant project files and configuration before explaining what exists. Adapt the depth to the user's question. Start with what the app does for its users, then describe the parts involved and how information moves between them. Name the files or configuration that support important claims so the user or another agent can find them again.

Use plain language and define a technical term when it helps the explanation. If useful, connect a capability to a concrete example from this app, such as where a user's saved information goes or how sign-in works. A short diagram is useful when it makes the relationships clearer.

Next.js, Better Auth, Postgres, Drizzle, Vercel, and shadcn/ui are possible parts of a project, not assumptions about it. Confirm what the project actually uses. Distinguish evidence from inference and say when configuration, deployment state, or behavior cannot be verified. Do not expose secrets. For a narrow question about an issue or a term, follow [explain-this](../explain-this/SKILL.md).
