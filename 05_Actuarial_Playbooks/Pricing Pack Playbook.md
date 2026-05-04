---
type: playbook
area: pricing
status: draft
owner: Son
updated: 2026-05-04
tags: [pricing, actuarial, glm, gbdt, rate-adequacy, codex-ready]
---

# Pricing Pack Playbook

## Purpose
Chuẩn hóa đầu ra pricing review hoặc pricing model cho bảo hiểm phi nhân thọ: từ data quality, assumptions, model diagnostics đến recommendation phân tích.

## When To Use
- Review rate adequacy.
- Xây dựng rating factors hoặc model frequency/severity/pure premium.
- So sánh GLM, GBDT hoặc model khác.
- Chuẩn bị tài liệu nội bộ cho Product/Actuarial/Management.

## Inputs
- Policy and exposure data.
- Claims data by accident/underwriting period.
- Product/coverage/limit/deductible/channel/region variables.
- Current rate, discount/loading, commission nếu được phép dùng.
- Regulatory and business constraints.

## Method
1. Define objective: monitoring, repricing, segmentation, or model build.
2. Confirm product scope and regulatory status.
3. Build data mart at agreed granularity.
4. Run data quality checks and reconciliation.
5. Create target: frequency, severity, burning cost, pure premium or loss ratio.
6. Fit baseline model before complex model.
7. Compare model performance and interpretability.
8. Produce pricing pack with assumptions, diagnostics, limitations and recommendation.

## Suggested Pack Sections
- Summary.
- Data Scope and Cut-off.
- Portfolio Overview.
- Data Quality.
- Claims and Loss Ratio Experience.
- Model Methodology.
- Rating Factors / Feature Importance.
- Diagnostics and Backtesting.
- Recommendation and Caveats.
- RunInfo / Versioning.

## Agent Instruction
Khi agent dùng playbook này:
- Đọc [[Insurance Law Analyst Notes]] trước khi đề xuất pricing/product action.
- Đọc [[Data Privacy Checklist]] nếu dùng customer/policy/claim-level data.
- Không gọi pricing recommendation là biểu phí chính thức.
- Ghi rõ model limitations, assumptions và data cut-off.
- Ưu tiên output có thể audit: config, feature list, model version, metric, run timestamp.

## Checks
- Product scope rõ ràng.
- Exposure definition nhất quán.
- Large loss treatment được ghi rõ.
- Train/test split không leak theo thời gian nếu bài toán cần temporal validation.
- Model interpretability đủ cho business review.
- Kết quả reconcile được với premium/claim totals.

## Related
- [[Insurance Law Analyst Notes]]
- [[Policy Data Contract]]
- [[Claim Data Contract]]
- [[Data Privacy Checklist]]