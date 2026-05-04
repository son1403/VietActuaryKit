---
type: checklist
area: admin-panel-ux
status: active
owner: Son
updated: 2026-05-04
tags: [admin, ux, saas, codex-ready]
---

# SaaS Admin Panel UX Checklist

## Purpose
Pattern cho admin panel của SaaS: quản lý user, role, billing, settings, audit log và operational controls.

## Common Sections
- Overview / health.
- Users and roles.
- Teams / organizations / workspaces.
- Billing and plan.
- Integrations and API keys.
- Data import/export.
- Audit log.
- Security settings.

## Safety Rules
- Dangerous actions need confirmation.
- Role/permission changes need audit log.
- API keys/secrets should be shown once or masked.
- Export should require permission and log event.
- Admin tools must be tenant-scoped.

## Agent Instruction
- Do not expose super-admin controls to tenant admins.
- Hide and protect actions by server-side permission.
- Include empty/error/no-permission states.
- Add audit trail for high-impact actions.

## Related
- [[User Roles and Permissions]]
- [[Auth and RBAC Playbook]]