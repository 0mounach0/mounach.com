# Mouad Mounach Portfolio - AI Memory

Last updated: 2026-09-28

## Project Status

- [x] Imported the downloaded static Framer portfolio template.
- [x] Initialized Git and created progressive homepage customization commits.
- [x] Repositioned the homepage around full-stack web, SaaS, automation, AI tools, integrations, and deployment.
- [x] Replaced homepage services, About copy, featured-work framing, working approach, FAQ framing, contact CTA, SEO metadata, and footer identity.
- [x] Removed visible Framer template promotion widgets.
- [x] Added a stable homepage copy override after Framer hydration and a desktop hero layout fix.
- [x] Added canonical AI context files and container deployment configuration.
- [/] Deploy the current review version through Dokploy and verify its public route.
- [ ] Replace fictional template projects with accurate case studies.
- [ ] Finish About, Projects, Blogs/Insights, project-detail, and error-page content.
- [ ] Replace or remove placeholder social links and confirm public contact details.
- [ ] Migrate the portfolio away from generated Framer HTML and Framer-hosted runtime/assets.

## Current Architecture

- Repository path: `/Users/mouadmounach/Documents/workspace/New portfolio mounach/mounach.com`
- Branch: `main`
- Static routes are standalone `index.html` files.
- No package install or build is required for local development.
- Local preview command: `python3 -m http.server 4173 --bind 127.0.0.1`
- Deployment image: Nginx serving the repository as static files.

## Portfolio Direction

- Owner: Mouad Mounach.
- Initial language: English; French may be added later.
- Positioning: full-stack Web and SaaS developer building complete web products, automation systems, AI-powered tools, dashboards, integrations, and production-ready deployments.
- Angular is evidence of technical depth, not the only market-facing identity.
- E-commerce is an application area within broader product engineering and automation work.
- Preserve the current visual direction until major redesigns are reviewed and approved.

## Approved Public Details Currently Rendered

- Name: Mouad Mounach.
- Email: `me.mounach@gmail.com`.
- Phone: `+33 6 59 09 32 36`.

These values came from the existing customized homepage. Reconfirm them before a final production launch.

## Decisions Log

- 2026-06-09: Use the downloaded Framer template as the initial visual base and customize it progressively.
- 2026-06-09: Keep the first version in English.
- 2026-06-10: Use JSON-driven DOM copy overrides because Framer hydration restored template wording after initial HTML replacements.
- 2026-06-10: Use a dedicated desktop hero overlay because the generated Framer text boxes did not accommodate the new positioning reliably.
- 2026-09-28: Use `AGENTS.md` as the single AI operating guide and `.ai/memory.md` as the living project record.
- 2026-09-28: Deploy the present export as an interim review version, not as proof of Framer independence.
- 2026-09-28: Remove the Framer dependency through a controlled rebuild into maintainable locally owned source code and assets; do not treat opaque mirrored Framer bundles as the long-term solution.
- 2026-09-28: Serve the interim static export from an unprivileged Nginx container in Dokploy.

## Framer Dependency Audit

- All 19 HTML pages contain Framer markers or Framer-hosted references.
- The export contains 2,547 `framerusercontent.com` URL occurrences.
- The homepage loads a remote Framer entry bundle plus React, Motion, Framer runtime, shared libraries, fonts, images, and search-index files.
- The HTML and inline CSS are stored locally, so some static content can render without Framer, but the current experience is not fully self-contained and can lose assets, hydration, animation, or interactive behavior if Framer resources change or become unavailable.

## Known Issues

- Secondary pages still contain template identity, fictional projects, placeholder descriptions, or unfinished metadata.
- Project cards currently point to template-derived project detail routes.
- Blog routes are still template-derived and need a keep/remove/replace decision.
- Some social links are placeholders or still reference the template author.
- The contact form has not been validated as a working, independently owned submission flow.
- Current production-readiness is limited by the remaining Framer CDN/runtime dependency.

## Open Questions

- Which real projects and measurable outcomes should become case studies?
- Which public social profiles should remain?
- Should the blog become an Insights section or be removed?
- What exact market-facing hero title should be used?
- Which implementation stack should replace the generated Framer export: a small static/Vite application, Astro, or Next.js?
- Should French be a second locale after the English version is complete?
