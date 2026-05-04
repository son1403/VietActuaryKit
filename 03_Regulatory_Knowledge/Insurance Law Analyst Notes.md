---
type: regulation-note
jurisdiction: Vietnam
area: insurance-business
status: draft
updated: 2026-05-04
tags: [insurance-law, non-life-insurance, pricing, claims, compliance, codex-ready]
---

# Insurance Law Analyst Notes

## Why It Matters
Luật Kinh doanh bảo hiểm và văn bản hướng dẫn ảnh hưởng trực tiếp đến cách analyst hiểu sản phẩm, hợp đồng, kênh phân phối, biểu phí, dự phòng, bồi thường, báo cáo và kiểm soát nội bộ trong doanh nghiệp bảo hiểm phi nhân thọ.

Note này dùng cho phân tích nghiệp vụ và kiểm tra rủi ro ban đầu. Không dùng để thay thế tư vấn pháp lý.

## Affected Workflows
- Pricing: cần hiểu phạm vi sản phẩm, điều khoản, exclusions, mức trách nhiệm, phí bắt buộc nếu có.
- Claims analytics: cần phân biệt incurred, paid, outstanding, rejected, reopened, subrogation, salvage, recovery.
- Reserving: cần nhất quán data cut-off, claim development, case reserve, IBNR và reconciliation với finance.
- Product monitoring: cần theo dõi loss ratio, expense ratio, combined ratio, profitability theo sản phẩm/kênh/khu vực.
- Mandatory insurance: motor TPL, fire/explosion, construction phải kiểm tra quy định riêng.

## Core Sources
- [[Regulatory Source Register]]
- Luật Kinh doanh bảo hiểm 08/2022/QH15.
- Nghị định 46/2023/NĐ-CP và Nghị định 97/2026/NĐ-CP.
- Thông tư 67/2023/TT-BTC.
- Nghị định 67/2023/NĐ-CP cho bảo hiểm bắt buộc.

## Data Impact
- Product code, coverage, sum insured, limit, deductible, premium, commission, channel và policy wording cần versioning.
- Claim data cần trạng thái nghiệp vụ rõ ràng: reported, accepted, paid, outstanding, closed, reopened, rejected.
- Pricing output cần phân biệt recommendation phân tích và biểu phí/điều khoản đã được phê duyệt nội bộ.

## Agent Guardrails
- Không đề xuất thay đổi biểu phí/điều khoản như quyết định chính thức.
- Khi phân tích sản phẩm bắt buộc, luôn flag cần kiểm tra quy định riêng.
- Khi output dùng cho quản trị/sản phẩm, ghi assumption và nguồn dữ liệu.
- Nếu không rõ sản phẩm thuộc nhóm bắt buộc hay tự nguyện, hỏi Product/Legal/Compliance.

## Compliance Questions
- Sản phẩm đang phân tích có phải bảo hiểm bắt buộc không.
- Biểu phí/điều khoản hiện hành là version nào.
- Output là phân tích nội bộ hay tài liệu gửi regulator/khách hàng/đối tác.
- Có yêu cầu lưu vết quyết định hoặc phê duyệt không.

## Related
- [[Pricing Pack Playbook]]
- [[Loss Ratio Analysis Playbook]]
- [[Policy Data Contract]]
- [[Claim Data Contract]]