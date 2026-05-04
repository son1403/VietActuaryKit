---
type: guideline
area: environments
status: active
owner: Son
updated: 2026-05-04
tags: [deployment, environments, saas, codex-ready]
---

# Deployment and Environment Strategy

## Purpose
Chuẩn hóa môi trường local/dev/staging/production cho app/SaaS.

## Environment Types
- Local: developer machine, synthetic or sanitized data only.
- Development: shared dev integration environment.
- Staging: production-like, restricted access, test/sanitized data unless approved.
- Production: real users and real data.

## Rules
- Never use production secrets in local notes or prompts.
- Use separate credentials per environment.
- Keep `.env.example` updated without real values.
- Production changes should be deployable and rollback-aware.
- Migrations need review when destructive or large.

## Release Checklist
- Tests pass.
- Build passes.
- Migrations reviewed.
- Env vars configured.
- Monitoring/logging ready.
- Rollback or recovery notes known.
- Security-sensitive changes reviewed.

## Related
- [[Secret Management]]
- [[Web App Security Checklist]]