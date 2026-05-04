---
type: data-contract
domain: claim
status: draft
owner: Son
updated: 2026-05-04
tags: [data-contract, claim, incurred, ibnr, codex-ready]
---

# Claim Data Contract

## Purpose
Mô tả dữ liệu claim dùng cho loss ratio, reserving, claims monitoring, fraud indicator review và pricing experience analysis. Contract này không chứa dữ liệu thật.

## Grain
Một dòng có thể là claim header, claim transaction, claim coverage item hoặc valuation snapshot. Phải xác nhận grain trước khi tính incurred hoặc development triangle.

## Core Fields
| Field | Meaning | Notes |
|---|---|---|
| claim_id | Mã hồ sơ bồi thường | Không đưa ID thật vào prompt/note nếu có thể định danh |
| policy_id | Mã hợp đồng liên quan | Dùng join với policy data |
| claim_status | Trạng thái claim | reported, open, closed, reopened, rejected |
| product_code | Mã sản phẩm | Nên reconcile với policy |
| coverage_code | Mã phạm vi bồi thường | Quan trọng cho analysis |
| accident_date | Ngày xảy ra tổn thất | Dùng accident period |
| reported_date | Ngày thông báo | Dùng reporting delay |
| closed_date | Ngày đóng hồ sơ | Có thể null |
| paid_amount | Số tiền đã trả | Theo valuation date hoặc transaction |
| outstanding_amount | Dự phòng hồ sơ | Theo valuation snapshot |
| recovery_amount | Thu hồi, đòi người thứ ba, salvage | Cần quy tắc trừ/không trừ |
| incurred_amount | paid + outstanding - recovery | Chỉ dùng nếu definition được xác nhận |
| loss_type | Loại tổn thất | Chuẩn hóa mapping |
| cause_of_loss | Nguyên nhân tổn thất | Có thể chứa thông tin nhạy cảm |
| large_loss_flag | Cờ large loss | Threshold phải ghi rõ |

## Data Quality Checks
- claim_id không null.
- accident_date <= reported_date, trừ case nhập sai cần điều tra.
- paid/outstanding/recovery không double count.
- Closed claim còn outstanding cần kiểm tra quy tắc hệ thống.
- Reopened claim cần xử lý theo valuation date.
- Rejected claim có được đưa vào count/frequency không phải ghi rõ.

## Privacy Notes
- Claim notes, giấy tờ y tế, ảnh tổn thất, địa chỉ, biển số xe, thông tin người bị hại có thể là PII hoặc dữ liệu nhạy cảm.
- Chỉ dùng claim-level detail khi cần; ưu tiên aggregate.
- Không lưu raw claim notes trong Obsidian.

## Agent Instruction
- Xác nhận grain và valuation date trước khi tính incurred.
- Khi viết SQL, tránh select claim notes trừ khi nhiệm vụ cần rõ ràng.
- Với reserving, xác định accident period, development period và evaluation date.
- Với loss ratio, reconcile total incurred với finance/claims report nếu có.

## Related
- [[Policy Data Contract]]
- [[Loss Ratio Analysis Playbook]]
- [[Pricing Pack Playbook]]
- [[Data Privacy Checklist]]