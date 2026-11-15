# Astack

Astack helps you build an app with an AI agent without needing to learn programming. It helps you shape an idea, write a product requirements document (PRD), break that plan into issues, and work on those issues. You can change the app's theme or ask what a part of your app does and why it matters to an issue.

The skills inspect your project before describing its tools. They can work with an existing app or an early idea, regardless of its stack or agent provider. The optional scaffold skill creates a Next.js starter with shadcn/ui Maia, Better Auth, Drizzle, and PostgreSQL.

## Add Astack to a project

Copy the entire `skills` directory from this repository into the location where your agent discovers project-local skills. Keep all skill folders together so their relative links work. Add them to each project where you want to use Astack; no global installation is required.

For Codex, copy the folders into the project's `.agents/skills/` directory. For example, from the root of a local checkout of Astack, replace the example path with your project's path and run:

```sh
mkdir -p /path/to/your-project/.agents/skills
cp -R skills/. /path/to/your-project/.agents/skills/
```

If any destination folders already exist, inspect them before copying so you do not overwrite local changes. Open a new agent session in the project if the skills do not appear in the current session.

Other agents may use a different project-local directory or require additional configuration. Follow your agent's instructions for discovering project skills. If an agent cannot discover skills, give it the path to the relevant `SKILL.md` and ask it to follow those instructions. Keep the companion folders together in either case.

## Use Astack

Ask your agent to use `astack`, then describe what you want to do. You can also ask for a companion skill by name or point to its `SKILL.md`.

- "Use astack to help me turn my idea for a community garden app into a plan."
- "Use scaffold to create a new app."
- "Use shape-idea to help me decide what the first version needs."
- "Use write-plan to create a PRD and issues for what we discussed."
- "Use write-prd to document this feature." Or, "Use write-issues to break this PRD into work."
- "Use change-theme to make my app warm brown, using a TweakCN theme."
- "Use change-theme to apply this TweakCN theme: [paste theme link]."
- "Use understand-project to show me how this app saves my customers' information."
- "Use explain-this: what does the database have to do with this issue?"
- "Use work-on-issue to help me build the first issue."

By default, the plan goes in `docs/astack/PRD.md` and issue drafts go in `docs/astack/issues/` inside your project. You can ask for another location. The agent keeps these as local files unless you ask it to publish them to an issue tracker.
