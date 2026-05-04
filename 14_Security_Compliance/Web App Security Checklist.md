---
type: checklist
area: web-security
status: active
owner: Son
updated: 2026-05-04
tags: [security, webapp, saas, owasp, codex-ready]
---

# Web App Security Checklist

## Purpose
Minimum security checklist for app/SaaS work. Use before shipping auth, APIs, uploads, payments, dashboards, admin tools or external integrations.

## Core Checks
- Authentication required for protected routes.
- Authorization checked server-side.
- Tenant isolation enforced in queries and services.
- Input validation on API boundaries.
- Rate limiting for public or expensive endpoints.
- Secrets stored in environment/secret manager, not code or Obsidian.
- File uploads validate type, size and storage access.
- Logs do not contain secrets or raw PII.

## Sensitive Features
- Admin panel.
- Export/download.
- Payment/billing.
- Webhook processing.
- API keys/integrations.
- Background jobs with external side effects.
- AI features using user/customer data.

## Agent Instruction
- Add authz tests.
- Add validation tests.
- Review logging and error responses.
- Flag open security questions before completion.

## Related
- [[Secret Management]]
- [[Auth and RBAC Playbook]]
- [[API Design Playbook]]