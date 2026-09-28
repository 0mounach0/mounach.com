# Mouad Mounach Portfolio

Personal portfolio for Mouad Mounach, focused on full-stack web products, SaaS, automation, AI-powered tools, integrations, and production delivery.

## Current State

This repository currently contains a downloaded static Framer export that has been partly customized. It is useful as a visual review version, but it still loads runtime modules and assets from Framer's CDN. The long-term plan is to migrate the design to maintainable, independently hosted source code.

Project operating rules are in `AGENTS.md`; durable status and decisions are in `.ai/memory.md`.

## Local Preview

No dependencies or build step are required:

```bash
python3 -m http.server 4173 --bind 127.0.0.1
```

Open [http://127.0.0.1:4173](http://127.0.0.1:4173).

## Routes

- `/` - homepage
- `/about/` - About page
- `/projects/` - project index and project-detail routes
- `/blogs/` - article index and article-detail routes
- `/404/` - static error page

## Container

Build and run the static site with Docker:

```bash
docker build -t mounach-portfolio .
docker run --rm -p 8080:8080 mounach-portfolio
```

Open [http://127.0.0.1:8080](http://127.0.0.1:8080).

See `DEPLOYMENT.md` for the Dokploy contract.
