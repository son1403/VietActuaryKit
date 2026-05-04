---
type: skill-index
status: active
owner: Son
updated: 2026-05-04
tags: [codex, skills, agentbrain, codex-ready]
---

# Available Codex Skills Index

## Purpose
This public template cannot know which Codex skills are installed on another user's machine. Use this note as a generic index pattern for documenting local skills in a private vault.

## Highest Priority
- [[RTK Token Optimization Playbook]]
- `rtk-token-optimization`: use for coding, debugging, repository exploration, git inspection, tests, builds, linting, or any task that may produce long terminal output.

## Recommended Skill Categories
| Skill Category | When To Use | Example Private Path |
|---|---|---|
| RTK token optimization | Any coding-agent task with shell output | `<YOUR_CODEX_HOME>/skills/rtk-token-optimization/SKILL.md` |
| Document/PDF/PPTX processing | Reading, creating, or reviewing office documents | `<YOUR_CODEX_HOME>/skills/<doc-skill>/SKILL.md` |
| Spreadsheet analysis | Excel/CSV/data QA workflows | `<YOUR_CODEX_HOME>/skills/<spreadsheet-skill>/SKILL.md` |
| Security review | Security scans, threat modeling, secure coding | `<YOUR_CODEX_HOME>/skills/<security-skill>/SKILL.md` |
| UI/UX/frontend | App, dashboard, SaaS, landing page, or component UI work | `<YOUR_CODEX_HOME>/skills/<frontend-skill>/SKILL.md` |
| Deployment | Cloud deployment, CI/CD, environment setup | `<YOUR_CODEX_HOME>/skills/<deploy-skill>/SKILL.md` |
| Power BI / analytics | BI model/report review and analytics development | `<YOUR_CODEX_HOME>/skills/<analytics-skill>/SKILL.md` |

## Private Vault Checklist
When adapting this note to your own private vault:
- Generate the list from your local `skills` folder.
- Keep machine-specific paths private unless you intentionally publish placeholders.
- Do not publish proprietary plugin details, credentials, tokens, or internal connector names.
- Keep RTK as the highest-priority skill for token control.

## Agent Rule
- When a user invokes a skill by name, read that skill's `SKILL.md` before acting.
- Do not use skills to bypass privacy, security, legal, or compliance guardrails.
- For long terminal output, prefer RTK before raw commands when available.
