---
type: guideline
area: data-retention-audit
status: active
owner: Son
updated: 2026-05-04
tags: [audit-log, retention, compliance, saas, codex-ready]
---

# Data Retention and Audit Log

## Purpose
Hướng dẫn retention và audit log cho app/SaaS có dữ liệu nghiệp vụ, dữ liệu khách hàng hoặc hành động quan trọng.

## Audit Events
- User invite, role change, deactivation.
- Create/update/delete/archive critical records.
- Approve/reject workflow action.
- Export/download sensitive data.
- Billing/subscription changes.
- API key create/revoke.
- Integration connection changes.

## Audit Fields
- Event type.
- Actor id.
- Tenant/workspace id.
- Resource type and id.
- Timestamp.
- Summary of change, avoiding raw sensitive payload.

## Agent Instruction
- Avoid logging full before/after payloads if sensitive.
- Prefer structured event summaries.
- Flag Legal/Compliance review for regulated or personal data.

## Related
- [[Data Privacy Checklist]]
- [[Auth and RBAC Playbook]]