---
type: domain-note
domain: non-life-insurance
country: Vietnam
status: draft
updated: 2026-05-04
tags: [non-life-insurance, vietnam, actuarial, data-analytics, codex-ready]
---

# Non-Life Insurance Vietnam Overview

## Scope
Bảo hiểm phi nhân thọ tại Việt Nam bao gồm các nghiệp vụ như xe cơ giới, tài sản, cháy nổ, hàng hải, kỹ thuật, trách nhiệm, sức khỏe/người, du lịch, nông nghiệp và các sản phẩm thương mại/cá nhân khác tùy giấy phép và quy định hiện hành.

## Analyst View
Một data/actuarial analyst thường xử lý các nhóm bài toán:
- Premium and exposure analysis.
- Claims frequency, severity, loss ratio, combined ratio.
- Pricing and rate adequacy.
- Reserving/IBNR and claim development.
- Portfolio monitoring by product, channel, region, branch, customer segment.
- Reinsurance and retention analysis.
- Data quality, reconciliation and reporting automation.

## Key Metrics
- Written premium: phí ghi nhận theo hợp đồng/phụ lục.
- Earned premium: phí được hưởng theo thời gian bảo hiểm đã qua.
- Unearned premium reserve: phần phí chưa được hưởng.
- Paid claims: bồi thường đã chi trả.
- Outstanding claims: ước tính còn phải trả cho claim đã phát sinh/báo cáo.
- Incurred claims: paid + outstanding, tùy policy kế toán và data cut-off.
- Loss ratio: incurred claims / earned premium.
- Expense ratio: expenses / earned premium hoặc written premium tùy mục đích.
- Combined ratio: loss ratio + expense ratio.

## Product Dimensions
- Product line / class of business.
- Coverage / risk type.
- Channel: direct, agent, broker, bancassurance, digital, partner.
- Geography: region, province, branch.
- Customer segment: individual, SME, corporate, fleet, affinity.
- Policy term, endorsement, cancellation, renewal.

## Data Risks
- Không đồng nhất product code qua thời gian.
- Policy endorsement làm thay đổi premium, exposure và coverage.
- Claim reopen/recovery/subrogation làm biến động incurred.
- Cut-off giữa core insurance system, finance và reporting không khớp.
- PII xuất hiện trong claim notes hoặc policy/customer extracts.

## Related
- [[Policy Data Contract]]
- [[Claim Data Contract]]
- [[Loss Ratio Analysis Playbook]]
- [[Pricing Pack Playbook]]
- [[Insurance Law Analyst Notes]]