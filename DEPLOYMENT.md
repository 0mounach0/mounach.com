# Dokploy Deployment

## Runtime Contract

- Build method: Dockerfile
- Container port: `8080`
- Health endpoint: `/healthz`
- Persistent volumes: none
- Environment variables: none
- Secrets: none
- Runtime user: unprivileged Nginx user provided by the base image

## Deployment Flow

1. Commit and push the reviewed repository state.
2. Build the root `Dockerfile` in Dokploy.
3. Route the intended hostname to container port `8080`.
4. Confirm `/healthz` returns HTTP 200.
5. Confirm `/`, `/about/`, `/projects/`, and one nested detail route render successfully.
6. Check the browser console and network panel for failed Framer resources.

## Important Limitation

This deployment hosts the HTML on Dokploy but does not yet eliminate Framer dependencies. The current pages still request Framer-hosted JavaScript, images, fonts, and indexes. Track the independent rebuild separately and do not describe this interim deployment as self-contained.

## Rollback

Redeploy the last known-good Git commit or image. The site has no database or persistent application state.
