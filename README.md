# LENSORA

A bilingual (Arabic/English) creative portfolio and discovery platform for photographers, videographers, editors, and visual designers.

## Live preview

- Production preview: https://lensora-platform.m7njordan.workers.dev
- Health check: https://lensora-platform.m7njordan.workers.dev/health

## Current status

The first public-facing landing page is deployed on Cloudflare Workers. It includes:

- Arabic and English interface with RTL/LTR switching
- Responsive navigation for mobile and desktop
- Creative disciplines and portfolio showcase sections
- Portfolio category filters and live text search
- Creator preview cards
- Black, charcoal, and gold visual identity

The creator profiles and portfolio entries currently shown are demonstration content. Account registration, authentication, real portfolio uploads, ratings, notifications, and admin verification have not been implemented yet.

## Infrastructure

- Hosting: Cloudflare Workers
- Worker name: `lensora-platform`
- GitHub repository: https://github.com/prosw-coder/lensora-platform

## Development notes

The initial Worker was deployed directly to the Cloudflare account while this repository was empty. The deployed source has now been exported and committed as `worker.js`. Keep this repository in sync with Cloudflare when making future changes, so it can become the source of truth for the application.

## Brand

**LENSORA** — Create · Capture · Inspire
