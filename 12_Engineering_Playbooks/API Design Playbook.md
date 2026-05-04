---
type: playbook
area: api-design
status: active
owner: Son
updated: 2026-05-04
tags: [api, backend, saas, codex-ready]
---

# API Design Playbook

## Purpose
Chuẩn hóa API cho app/SaaS: predictable, secure, testable và dễ tích hợp.

## API Checklist
- Resource model rõ ràng.
- Input validation ở boundary.
- Auth and authorization trên mọi endpoint nhạy cảm.
- Pagination cho list endpoint.
- Filtering/sorting chỉ cho field được phép.
- Idempotency cho payment, webhook, import hoặc retry-prone actions.
- Consistent error shape.
- Rate limit cho endpoint public hoặc expensive.
- Audit log cho action quan trọng.

## Common Endpoint Patterns
- `GET /resources`: list with pagination.
- `POST /resources`: create.
- `GET /resources/{id}`: detail with authorization.
- `PATCH /resources/{id}`: partial update.
- `POST /resources/{id}/actions/{action}`: business action such as approve/reject/export.

## Agent Instruction
- Follow existing route conventions.
- Add tests for happy path, validation failure, unauthorized and forbidden cases.
- Avoid returning internal stack traces or secrets.
- Keep response fields intentionally scoped.

## Related
- [[Auth and RBAC Playbook]]
- [[Web App Security Checklist]]