---
type: checklist
area: product-discovery
status: active
owner: Son
updated: 2026-05-04
tags: [saas, product, discovery, codex-ready]
---

# SaaS Product Discovery Checklist

## Purpose
Dùng trước khi code app/SaaS mới để làm rõ bài toán, người dùng, workflow, dữ liệu, quyền truy cập và tiêu chí MVP.

## Product Context
- Problem cần giải quyết là gì.
- Người dùng chính là ai: admin, operator, analyst, manager, customer, partner.
- Workflow hiện tại đang làm bằng Excel/email/manual tool nào.
- Pain point lớn nhất: tốc độ, lỗi nhập liệu, thiếu kiểm soát, thiếu báo cáo, thiếu collaboration hay thiếu audit.
- Tần suất sử dụng: hàng ngày, hàng tuần, theo chiến dịch hay ad-hoc.

## MVP Scope
- Must-have workflow đầu tiên.
- Input bắt buộc.
- Output bắt buộc.
- Role tối thiểu.
- Dashboard/report tối thiểu.
- Việc không làm trong v1.

## Success Metrics
- Thời gian xử lý giảm bao nhiêu.
- Tỷ lệ lỗi giảm bao nhiêu.
- Số workflow hoàn tất.
- Chất lượng dữ liệu hoặc audit trail cải thiện thế nào.

## Data and Compliance
- Có PII, dữ liệu khách hàng, dữ liệu tài chính, dữ liệu nội bộ hoặc secret không.
- Dữ liệu đến từ nguồn nào: upload, DB, API, manual input, third-party.
- Ai được xem/sửa/xuất dữ liệu.
- Cần retention, audit log, approval hoặc export control không.

## Agent Instruction
Trước khi implement app/SaaS:
- Đọc [[RTK Token Optimization Playbook]].
- Đọc [[App Architecture Playbook]].
- Đọc [[Auth and RBAC Playbook]] nếu có nhiều role.
- Đọc [[Web App Security Checklist]] nếu app có auth, upload, API hoặc dữ liệu thật.
- Tạo scope rõ: v1 làm gì và không làm gì.

## Related
- [[MVP Scope Template]]
- [[App Architecture Playbook]]
- [[Web App Security Checklist]]