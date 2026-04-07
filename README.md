# BrightWire.ai Website

Static website for [brightwire.ai](https://brightwire.ai).

## Architecture

- **Hosting:** AWS S3 + CloudFront
- **CI/CD:** AWS CodePipeline + CodeBuild
- **DNS:** Route53

## Branches

| Branch | Deploys To | URL |
|--------|-----------|-----|
| `main` | Production | https://brightwire.ai |
| `dev` | Staging | https://dev-static.brightwire.ai |

## Pages

- `index.html` — Home
- `services.html` — Services & Case Studies
- `roadmap.html` — AI Roadmap (4-Phase Model)
- `local-ai.html` — Private AI / Secure Infrastructure
- `consultation.html` — Consultation Hub / Booking

## Deployment

Push to `main` or `dev` — CodePipeline handles the rest.

- Production deploys sync to S3 + invalidate CloudFront cache
- Dev deploys use aggressive no-cache headers for fast iteration
