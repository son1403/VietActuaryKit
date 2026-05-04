---
type: dashboard
status: active
owner: Son
updated: 2026-05-04
tags: [agentbrain, codex-ready, non-life-insurance, actuarial, data-analytics, saas, webapp]
---

# VietActuaryKit Home

## Mục tiêu
VietActuaryKit là kho tri thức Obsidian để Codex và các agent hỗ trợ công việc data analyst, actuarial analyst, app builder và SaaS builder.

Kho này lưu tri thức nghiệp vụ, playbook phân tích, data contracts, guardrails pháp lý, engineering playbooks, UX checklist, security checklist và prompt vận hành agent. 

## Highest Priority
- [[RTK Token Optimization Playbook]]
- [[Available Codex Skills Index]]

## Start Here
- [[Codex Operating Guide]]
- [[Regulatory Source Register]]
- [[Data Privacy Checklist]]
- [[Insurance Law Analyst Notes]]
- [[Non-Life Insurance Vietnam Overview]]

## Insurance / Data / Actuarial
- [[Loss Ratio Analysis Playbook]]
- [[Pricing Pack Playbook]]
- [[Policy Data Contract]]
- [[Claim Data Contract]]

## App / SaaS
- [[SaaS Product Discovery Checklist]]
- [[MVP Scope Template]]
- [[User Roles and Permissions]]
- [[App Architecture Playbook]]
- [[API Design Playbook]]
- [[Database Schema Playbook]]
- [[Auth and RBAC Playbook]]
- [[Billing and Subscription Playbook]]
- [[SaaS Admin Panel UX Checklist]]

## Security / Ops
- [[Web App Security Checklist]]
- [[Secret Management]]
- [[Data Retention and Audit Log]]
- [[Deployment and Environment Strategy]]

## Templates
- [[Playbook Template]]
- [[Regulation Template]]
- [[Data Contract Template]]
- [[Project AGENTS.md Template]]

## Agent Rules
1. Dùng [[RTK Token Optimization Playbook]] trước mọi task coding/debugging/repo exploration/test/build/lint nếu RTK có sẵn.
2. Đọc [[Codex Operating Guide]] trước khi dùng các note khác.
3. Với dữ liệu policy, claim, customer hoặc dữ liệu cá nhân, chạy [[Data Privacy Checklist]] trước.
4. Với pricing, reserving, claim analytics hoặc reporting, link về playbook và regulatory note liên quan.
5. Với app/SaaS, đọc [[SaaS Product Discovery Checklist]], [[App Architecture Playbook]], [[Auth and RBAC Playbook]] và [[Web App Security Checklist]] nếu có auth/API/dữ liệu thật.
6. Không kết luận một phân tích là tuân thủ pháp luật nếu chưa có nguồn, ngày hiệu lực và xác nhận Legal/Compliance.
7. Không lưu secrets, production credentials hoặc dữ liệu khách hàng thật trong vault.

## Maintenance
- Review regulatory source register theo quý.
- Khi có dự án mới, tạo note trong `08_Project_Knowledge` và link về playbook liên quan.
- Khi có quyết định phân tích/kiến trúc quan trọng, ghi vào `09_Decision_Log`.
