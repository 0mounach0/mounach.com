# Mouad Mounach Portfolio - AI Working Agreement

## Project Brief

This repository is Mouad Mounach's English-language professional portfolio. It began as a downloaded Framer template and is being converted progressively into a credible developer portfolio for web products, SaaS, automation, AI tooling, integrations, and production delivery.

The immediate objective is to keep a reviewable version online while replacing template content and, in a later controlled migration, removing the remaining Framer runtime and CDN dependency.

## Source of Truth

- `AGENTS.md` is the canonical project operating guide.
- `.ai/memory.md` is the living record of project status, decisions, open questions, and known issues.
- `README.md` contains human-facing setup and repository orientation.
- `DEPLOYMENT.md` contains the Dokploy deployment contract.

Read `.ai/memory.md` before making changes. Do not create parallel AI rule or memory files.

## Current Architecture

- The site is a static Framer export made of standalone `index.html` files.
- `/index.html` is the homepage.
- `/about`, `/projects`, `/blogs`, `/404`, and their nested directories are static routes.
- There is no package manager, compilation step, application server, or database.
- The generated HTML still loads Framer-hosted JavaScript modules, fonts, images, and search indexes. Dokploy hosting does not by itself make the site independent from Framer.
- Docker deployment uses Nginx to serve the repository as static files.

## Product and Content Direction

- Keep the first production version in English.
- Present Mouad as a full-stack web and SaaS developer, not only as an Angular specialist.
- Emphasize complete products, automation systems, AI-powered tools, dashboards, integrations, e-commerce tooling, deployment, and technical ownership.
- Preserve the current visual structure until Mouad approves major redesigns.
- Replace template people, projects, articles, links, and claims progressively with accurate information.
- Never invent client work, outcomes, testimonials, metrics, or personal details.
- Do not publish private contact or account information unless it is already approved for the public portfolio.

## Change Rules

1. Inspect the rendered page and the relevant HTML before editing.
2. Keep edits narrowly scoped and preserve unrelated working behavior.
3. Treat the downloaded Framer HTML as generated code: text may exist in server-rendered markup, serialized JSON, and hydrated runtime content.
4. Verify both desktop and mobile layouts after visible changes.
5. Check navigation and affected routes, not only the homepage.
6. Keep deployment configuration portable and free of secrets.
7. Use conventional commit messages such as `feat(portfolio): add project case study` or `fix(home): correct mobile hero spacing`.
8. Do not commit or push unrelated files.

## Verification

For content or layout changes, run at least:

```bash
git diff --check
python3 -m http.server 4173 --bind 127.0.0.1
```

Then verify the affected routes in a browser. For deployment changes, also build the Docker image when Docker is available and confirm the container returns HTTP 200.

## Framer Independence Policy

- Do not claim the site is Framer-independent while HTML pages reference `framerusercontent.com`, Framer runtime modules, or remotely hosted Framer assets.
- The current export may be deployed as an interim review version.
- Full independence requires migrating the design to maintainable locally owned source code and local or independently controlled assets.
- Prefer a route-by-route migration with visual comparison so the live review version stays usable.
- Do not attempt a blind bulk rewrite of generated HTML or mirror opaque Framer runtime bundles as the long-term architecture.

## Memory Protocol

Update `.ai/memory.md` when a meaningful feature begins or completes, a durable decision is made, a deployment changes, a real project replaces template content, or a blocker/known issue is discovered. Use dated, concise, factual entries. Preserve prior decisions unless explicitly superseded.
