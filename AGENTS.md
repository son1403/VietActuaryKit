# VietActuaryKit Agent Instructions

## Highest Priority: RTK Token Control
Use RTK for token-efficient command output when it is installed. Before substantial coding, debugging, repo exploration, build/test/lint, git inspection, or app/SaaS work, check whether `rtk` is available.

If RTK is installed, prefer explicit wrappers such as `rtk git status`, `rtk git diff`, `rtk read`, `rtk grep`, `rtk find`, `rtk test`, `rtk pytest`, `rtk lint`, `rtk tsc`, and `rtk deps`.

## Purpose
This repository is a public Obsidian-compatible knowledge-base template for Vietnam non-life insurance, actuarial analytics, data workflows, app/SaaS engineering, and AI agent guardrails.

## Agent Learning Workflow
Before substantial work, follow `07_Agent_Instructions/Agent Learning Workflow.md`.

Use this loop:

1. Orient: read the minimum relevant context.
2. Clarify: surface assumptions, ambiguity, and tradeoffs before acting.
3. Simplify: choose the smallest useful action.
4. Execute surgically: touch only what the task requires.
5. Verify: run a focused check.
6. Capture reusable learning: update templates/playbooks only with generic, public-safe lessons.

This workflow is inspired by practical agent guidelines such as think-before-coding, simplicity first, surgical changes, and goal-driven execution.

## Privacy and Public-Safety Rules
Do not add secrets, credentials, API keys, production config, customer data, policy data, claim data, internal company workflows, proprietary pricing logic, reserving assumptions, commission structures, or confidential business data.

## Regulatory Guardrails
Keep regulatory content source-linked and date-aware. This repository is not legal, compliance, actuarial, insurance, security, privacy, tax, or financial advice.

## Editing Rules
- Keep notes generic and reusable.
- Keep examples synthetic.
- Prefer templates, checklists, and playbooks.
- Do not weaken privacy, data minimization, security, or compliance guardrails.
