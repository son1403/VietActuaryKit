---
type: playbook
area: loss-ratio
status: draft
owner: Son
updated: 2026-05-04
tags: [loss-ratio, claims, earned-premium, actuarial, codex-ready]
---

# Loss Ratio Analysis Playbook

## Purpose
Tạo phân tích loss ratio cho danh mục bảo hiểm phi nhân thọ theo sản phẩm, kênh, khu vực, branch, customer segment hoặc underwriting year.

## When To Use
- Theo dõi profitability định kỳ.
- So sánh loss ratio giữa các sản phẩm/kênh/khu vực.
- Chuẩn bị pricing review hoặc renewal strategy.
- Phát hiện bất thường claims hoặc premium/exposure.

## Inputs
- Policy/premium data: policy_id, product, coverage, channel, branch, effective_date, expiry_date, written_premium, earned_premium, exposure.
- Claim data: claim_id, policy_id, accident_date, reported_date, paid_amount, outstanding_amount, recovery, status.
- Calendar and cut-off: valuation date, accounting period, data refresh timestamp.

## Method
1. Xác định cohort: accident year, underwriting year, policy year hoặc accounting period.
2. Reconcile premium: written, earned, refund/cancellation/endorsement.
3. Reconcile claims: paid, outstanding, recovery, reopened, rejected.
4. Tính incurred claims theo definition đã chốt.
5. Tính loss ratio = incurred claims / earned premium.
6. Drill-down theo product/channel/region/branch/segment.
7. Kiểm tra outlier: large loss, low exposure, negative premium, claim reopened.

## Checks
- Earned premium không âm trừ trường hợp reversal/correction có giải thích.
- Claim amount không double count giữa paid và outstanding.
- Closed claim có outstanding hợp lý hoặc bằng 0 theo quy tắc hệ thống.
- Loss ratio cực cao/thấp phải kiểm tra exposure và large loss.
- Output có ghi valuation date và data cut-off.

## Agent Instruction
Khi agent dùng playbook này:
- Đọc [[Data Privacy Checklist]] trước nếu có policy/claim/customer-level data.
- Link [[Policy Data Contract]] và [[Claim Data Contract]].
- Không export PII nếu chỉ cần aggregate.
- Nêu rõ định nghĩa incurred claims và earned premium.
- Nếu dùng cho pricing/product decision, link [[Insurance Law Analyst Notes]].

## Output
- Summary table: earned premium, paid, outstanding, incurred, loss ratio.
- Breakdown table by selected dimensions.
- Large loss impact view nếu có.
- Data quality notes and assumptions.

## Related
- [[Non-Life Insurance Vietnam Overview]]
- [[Policy Data Contract]]
- [[Claim Data Contract]]
- [[Data Privacy Checklist]]