---
name: scaffold
description: Create a Next.js app with the shadcn/ui Maia style, Better Auth, Drizzle, and PostgreSQL. Use when the user wants to scaffold this starter app.
---

# Scaffold a project

Create a working starting point for the user's app with Next.js, shadcn/ui, Better Auth, Drizzle ORM, and PostgreSQL. Use the conversation and any existing PRD to pick the project name and destination. Explain setup and remaining steps in plain language.

## Create the app

Inspect the target directory and project instructions first. Preserve existing files, including plans and issue drafts. If it already contains an app, do not run a generator over it. Work within the existing app only if the user requests that; otherwise ask for a different destination. If a generator requires an empty directory, create the app in a separate directory and preserve the existing project files.

Use the shadcn CLI to create a Next.js app with the named Maia preset. For example, run `npx shadcn@latest init --name <app-name> --template next --base base --preset maia --no-monorepo -y` from the parent directory. Adapt the name and destination to the user's project. Use the CLI's current documented options if they change. Do not use the default preset in place of Maia. Use the generated app's package manager and conventions for subsequent setup.

## Configure the included services

- Install and configure Drizzle ORM, Drizzle Kit, and the `pg` Node.js PostgreSQL driver. Add a PostgreSQL database client, schema location, and Drizzle configuration. Use `DATABASE_URL` for the connection string; do not tie the app to a database provider.
- Install Better Auth and its Drizzle adapter. Configure email and password authentication and Google social sign-in. Add the Better Auth tables to the Drizzle schema, the Next.js authentication route handler, and the client needed to call authentication. Provide minimal sign-up and sign-in UI for both methods and a way to sign out. Do not add other authentication methods or unrelated product features.
- Create `.env` with `DATABASE_URL=postgresql://USER:PASSWORD@HOST:5432/DATABASE` as a placeholder, `BETTER_AUTH_URL=http://localhost:3000`, and placeholders for `GOOGLE_CLIENT_ID` and `GOOGLE_CLIENT_SECRET`. Generate a unique high-entropy `BETTER_AUTH_SECRET` locally without displaying it. Keep `.env` out of version control. Provide an `.env.example` with placeholders, never real secrets.
- Generate the Drizzle migration for the authentication schema without connecting to or changing a database. Do not run migrations against a database until the user supplies a connection and authorizes any required external changes.

Use the current official [shadcn CLI](https://ui.shadcn.com/docs/cli), [Better Auth installation](https://www.better-auth.com/docs/installation), [Drizzle adapter](https://www.better-auth.com/docs/adapters/drizzle), [Google provider](https://www.better-auth.com/docs/authentication/google), and [Drizzle PostgreSQL](https://orm.drizzle.team/docs/get-started-postgresql) instructions to resolve version-specific details. Do not require the user to provide credentials during scaffolding or paste secrets into the conversation. Do not provision services, deploy, or add other infrastructure unless requested.

## Verify and hand off

Install dependencies and run the generated app's appropriate build and checks. Verify the Maia configuration, auth routes, schema, and environment placeholders. Where practical, start the app and inspect the sign-in UI. Do not claim database-backed sign-in or Google OAuth works until it has been tested with a configured database and valid credentials.

Tell the user what was created and how to run it. Explain that they need to add a PostgreSQL connection string, apply the generated migration, and configure Google credentials and its callback URL before those integrations can work. Report which checks ran and any blockers. Do not expose secrets.

If the user needs to settle the product idea first, follow [shape-idea](../shape-idea/SKILL.md). For an explanation of the resulting app, follow [understand-project](../understand-project/SKILL.md). For planned implementation work, follow [work-on-issue](../work-on-issue/SKILL.md).
