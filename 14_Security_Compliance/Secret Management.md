---
type: guideline
area: secret-management
status: active
owner: Son
updated: 2026-05-04
tags: [secrets, security, env, saas, codex-ready]
---

# Secret Management

## Purpose
Quy định cách xử lý API keys, tokens, credentials, connection strings và signing secrets.

## Rules
- Never store secrets in Obsidian.
- Never commit secrets to git.
- Use `.env.local` or platform secret manager for local/dev, following project convention.
- Use deployment provider environment variables for production.
- Rotate exposed secrets immediately.
- Mask secrets in logs and UI.
- Do not paste production credentials into prompts.

## Agent Instruction
- Add placeholder names, not real values.
- Update `.env.example` if the repo uses one.
- Mention required env vars in final response.
- Do not infer or create fake production secrets.

## Related
- [[Web App Security Checklist]]
- [[Deployment and Environment Strategy]]