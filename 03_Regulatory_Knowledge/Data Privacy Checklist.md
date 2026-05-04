---
type: checklist
area: personal-data-protection
jurisdiction: Vietnam
status: draft
updated: 2026-05-04
tags: [privacy, pii, data-governance, compliance, codex-ready]
---

# Data Privacy Checklist

## Purpose
Checklist cho agent trước khi xử lý dữ liệu policy, claim, customer, agent, garage, hospital, beneficiary hoặc dữ liệu nội bộ có thể định danh cá nhân/tổ chức.

## Quick Classification
- Dữ liệu có định danh trực tiếp không: họ tên, số điện thoại, email, CCCD, MST cá nhân, địa chỉ, biển số xe, số hợp đồng, số claim.
- Dữ liệu có định danh gián tiếp không: ngày sinh, giới tính, tỉnh/huyện, nghề nghiệp, mã khách hàng, lịch sử bồi thường, thời điểm tổn thất.
- Có dữ liệu nhạy cảm không: sức khỏe, y tế, tài chính cá nhân, vị trí, sinh trắc học, trẻ em, thông tin đặc biệt khác.
- Có dữ liệu nội bộ hoặc bí mật kinh doanh không: biểu phí, loss cost, treaty reinsurance, reserve, profitability theo kênh/sản phẩm.

## Before Analysis
- Mục đích xử lý đã rõ chưa.
- Dữ liệu tối thiểu đã đủ chưa; bỏ cột không cần thiết.
- Có thể dùng dữ liệu tổng hợp, masking, hashing hoặc pseudonymization không.
- Người yêu cầu có quyền truy cập dữ liệu không.
- Output sẽ chia sẻ cho ai, trong nội bộ hay bên ngoài.
- Có cần approval từ Legal/Compliance/Data Owner không.

## Agent Guardrails
- Không paste raw PII vào prompt hoặc note Obsidian.
- Không tạo sample data giống dữ liệu thật đến mức có thể tái định danh.
- Không xuất danh sách cá nhân/claim detail nếu chỉ cần metric tổng hợp.
- Khi viết SQL/Python, ưu tiên select cột tối thiểu và aggregate trước khi export.
- Khi tạo dashboard, tránh drill-through xuống thông tin định danh nếu chưa có quyền.

## Red Flags
- Dữ liệu sức khỏe trong bảo hiểm con người/health/travel accident.
- Claim notes có mô tả tai nạn, bệnh án, hình ảnh, giấy tờ tùy thân.
- Dữ liệu motor có biển số xe, số khung, số máy, địa chỉ chủ xe.
- Dữ liệu export ra Excel gửi qua email/chat.
- Dữ liệu dùng để train model hoặc đưa vào dịch vụ AI bên ngoài.

## Minimum Output Standard
Mọi phân tích có dữ liệu cá nhân nên ghi:
- Data source:
- Data period:
- Data granularity:
- PII handling:
- Access scope:
- Legal/Compliance review needed: Yes/No/Unknown

## Related
- [[Regulatory Source Register]]
- [[Policy Data Contract]]
- [[Claim Data Contract]]
- [[Codex Operating Guide]]