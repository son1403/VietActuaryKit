---
type: data-contract
domain: policy
status: draft
owner: Son
updated: 2026-05-04
tags: [data-contract, policy, premium, exposure, codex-ready]
---

# Policy Data Contract

## Purpose
Mô tả dữ liệu policy/premium/exposure dùng cho phân tích bảo hiểm phi nhân thọ. Contract này không chứa dữ liệu thật.

## Grain
Một dòng nên đại diện cho một policy coverage transaction, policy period, endorsement transaction hoặc exposure record tùy data mart. Phải ghi rõ grain trong mỗi dự án.

## Core Fields
| Field | Meaning | Notes |
|---|---|---|
| policy_id | Mã hợp đồng | Không dùng số thật trong note/prompt nếu có thể định danh |
| policy_version | Version/phụ lục | Cần cho endorsement/cancellation |
| product_code | Mã sản phẩm | Cần mapping ổn định theo thời gian |
| coverage_code | Mã quyền lợi/phạm vi | Quan trọng cho pricing và claims matching |
| customer_segment | Nhóm khách hàng | Nên aggregate, tránh PII |
| channel | Kênh bán | Direct, agent, broker, bank, digital, partner |
| branch | Chi nhánh/đơn vị | Chuẩn hóa code |
| region | Vùng/khu vực | Chuẩn hóa mapping |
| effective_date | Ngày bắt đầu hiệu lực | Dùng tính exposure/earned premium |
| expiry_date | Ngày hết hiệu lực | Dùng tính exposure/earned premium |
| transaction_date | Ngày ghi nhận giao dịch | Cần reconcile accounting |
| written_premium | Phí ghi nhận | Có thể âm do hủy/sửa đổi |
| earned_premium | Phí được hưởng | Cần definition rõ |
| exposure | Đơn vị rủi ro | Vehicle-year, policy-year, sum insured-year, member-month |
| sum_insured | Số tiền bảo hiểm | Có thể cần bucket/masking |
| deductible | Mức khấu trừ | Dùng pricing/underwriting |
| limit_amount | Mức trách nhiệm | Dùng pricing/underwriting |

## Data Quality Checks
- policy_id không null.
- effective_date <= expiry_date.
- earned_premium phù hợp với exposure và written_premium.
- product_code/coverage_code có mapping.
- transaction âm có lý do: cancellation, endorsement, refund.
- Không trộn policy grain và transaction grain nếu chưa aggregate rõ.

## Privacy Notes
- policy_id, customer_id, địa chỉ, biển số xe, số điện thoại, email là dữ liệu có thể định danh.
- Khi đưa vào prompt, dùng masked ID hoặc aggregate.
- Không lưu raw customer list trong Obsidian.

## Agent Instruction
- Luôn hỏi grain trước khi viết SQL/model nếu context chưa rõ.
- Nếu chỉ cần loss ratio aggregate, không select customer identifiers.
- Link [[Data Privacy Checklist]] trong mọi phân tích policy-level.

## Related
- [[Claim Data Contract]]
- [[Loss Ratio Analysis Playbook]]
- [[Pricing Pack Playbook]]