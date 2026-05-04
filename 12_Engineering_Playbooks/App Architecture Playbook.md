---
type: playbook
area: app-architecture
status: active
owner: Son
updated: 2026-05-04
tags: [architecture, saas, webapp, codex-ready]
---

# App Architecture Playbook

## Purpose
Dùng để định hình app/SaaS trước khi implement: boundaries, data flow, auth, API, persistence, jobs, observability và deployment.

## Architecture Questions
- App phục vụ single tenant hay multi-tenant.
- Có auth không, auth provider nào.
- Backend là API riêng hay full-stack framework.
- Data source chính là DB, file upload, external API hay manual input.
- Có background jobs, queue, scheduler hoặc webhook không.
- Có dashboard/report/export không.
- Có audit log hoặc approval workflow không.

## Recommended Baseline
- Separate UI, domain logic, data access and external integrations.
- Keep validation close to boundaries: forms, API handlers, service layer.
- Use typed schemas where possible.
- Keep secrets out of code and Obsidian.
- Prefer explicit error states over silent failure.
- Add logging for business-critical actions.

## Multi-Tenant Guardrails
- Every tenant-scoped table needs tenant/org/workspace key.
- Authorization must filter by tenant before returning records.
- Background jobs and exports must carry tenant context.
- Admin tools must prevent cross-tenant data leakage.

## Agent Instruction
- Use [[RTK Token Optimization Playbook]] for repo exploration and tests.
- Inspect existing stack and conventions before coding.
- Do not introduce a new framework if existing stack already solves the problem.

## Related
- [[API Design Playbook]]
- [[Database Schema Playbook]]
- [[Auth and RBAC Playbook]]