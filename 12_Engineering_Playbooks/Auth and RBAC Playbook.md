---
type: playbook
area: auth-rbac
status: active
owner: Son
updated: 2026-05-04
tags: [auth, rbac, permissions, saas, codex-ready]
---

# Auth and RBAC Playbook

## Purpose
Hướng dẫn thiết kế đăng nhập, phân quyền và kiểm soát truy cập trong app/SaaS.

## Checklist
- Chọn auth provider hoặc existing auth stack.
- Xác định tenant/org/workspace boundary.
- Thiết kế role matrix trước khi code.
- Protect server-side endpoints, không chỉ hide UI.
- Filter data by tenant and permission at query/service layer.
- Add audit log for admin, export, delete, approval, permission changes.

## Common Risks
- UI ẩn nút nhưng API vẫn cho gọi.
- User đổi ID trên URL để xem record khác.
- Admin tenant này xem được data tenant khác.
- Export endpoint bỏ qua permission.
- Webhook/job chạy không có tenant context.

## Test Cases
- Anonymous cannot access protected route.
- Authenticated user cannot access other tenant data.
- Viewer cannot mutate.
- Editor cannot approve if approval role required.
- Export requires explicit permission.

## Related
- [[User Roles and Permissions]]
- [[Web App Security Checklist]]