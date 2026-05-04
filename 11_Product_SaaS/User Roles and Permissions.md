---
type: playbook
area: roles-permissions
status: active
owner: Son
updated: 2026-05-04
tags: [saas, rbac, permissions, codex-ready]
---

# User Roles and Permissions

## Purpose
Chuẩn hóa cách thiết kế role/permission cho app/SaaS để tránh cấp quyền quá rộng hoặc thiếu audit.

## Minimum Role Model
- Owner: quản lý workspace/org, billing, cấu hình bảo mật, user management.
- Admin: quản lý dữ liệu và cấu hình nghiệp vụ.
- Editor: tạo/sửa workflow hoặc record nghiệp vụ.
- Reviewer/Approver: phê duyệt, reject, comment.
- Viewer: chỉ xem dashboard/report/record được phép.
- External/Partner: quyền hẹp, theo scope hợp đồng hoặc task.

## Design Rules
- Deny by default.
- Role nhỏ nhất đủ dùng.
- Export/download thường nhạy cảm hơn view.
- Delete nên là soft delete hoặc archive nếu cần audit.
- Admin action phải có audit log.
- External users không được thấy dữ liệu ngoài scope.

## Agent Instruction
- Không hard-code role logic rải rác.
- Tách authentication, authorization và business rules.
- Viết test cho permission edge cases.

## Related
- [[Auth and RBAC Playbook]]
- [[Data Retention and Audit Log]]
- [[Web App Security Checklist]]