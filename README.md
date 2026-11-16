# LENSORA

A bilingual (Arabic/English) creative portfolio and discovery platform for photographers, videographers, editors, and visual designers.

## Live preview

- Production site: https://lensora-platform.m7njordan.workers.dev
- Health check: https://lensora-platform.m7njordan.workers.dev/health

## Current implementation

- Arabic and English interface with RTL/LTR switching
- Responsive landing page, creator discovery, category filters, and service showcase
- Account registration, sign-in, secure session cookies, and sign-out
- Public creator profiles with owner-only profile editing
- Curated profile fields: specialty, Jordanian city, experience, skills, and languages
- Profile avatar uploads and portfolio image uploads
- Free portfolio limit: 5 images; PRO limit: 10 images
- Monthly PRO plan display: 10 JOD; activation is currently manual
- Image lightbox with close and zoom controls
- Cloudflare D1 for account/profile data and R2 for uploaded media

Some directory cards, services, and showcase entries on the landing page are demonstration content; they are not real creator accounts or live service listings.

## Infrastructure

- Hosting/runtime: Cloudflare Workers
- Worker: `lensora-platform`
- Database: Cloudflare D1
- Media storage: Cloudflare R2
- Source: https://github.com/prosw-coder/lensora-platform

## Security notes

- Passwords are stored as PBKDF2 hashes with per-user salts.
- Session tokens are random, stored as hashes, and delivered in HttpOnly, Secure, SameSite=Lax cookies.
- Mutating API requests require a same-origin Origin header.
- Login and registration attempts are rate-limited and old attempt records are pruned.
- Uploaded images are size-limited, MIME-allowlisted, and checked against file signatures.
- Media object keys are restricted to generated UUID paths.
- Profile options are validated against server-side allowlists.

## Development

The Cloudflare Worker source is maintained in `worker.js`. Keep this file synchronized with the deployed Worker when making changes.

## Brand

**LENSORA** — Create · Capture · Inspire
