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

The initial Worker was deployed directly to the Cloudflare account while this repository was empty. This README records the current deployment and project status. The complete Worker source and subsequent application modules should be committed here before enabling Git-based automatic deployments, so the repository becomes the source of truth.

## Brand

**LENSORA** — Create · Capture · Inspire
