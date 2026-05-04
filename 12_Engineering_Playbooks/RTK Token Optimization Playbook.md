---
type: playbook
area: token-optimization
status: active
owner: Son
updated: 2026-05-04
priority: highest
tags: [rtk, token-optimization, codex, agent, codex-ready]
---

# RTK Token Optimization Playbook

## Purpose
RTK is the default token-control layer for agent coding sessions. It reduces token burn by filtering and compressing noisy command output before the output reaches the LLM context.

Repository: https://github.com/rtk-ai/rtk

## Decision
Use RTK as the highest-priority command-output rule for coding, debugging, repo exploration, tests, builds, linting, git inspection and long terminal output.

On native Windows/PowerShell, do not assume auto-rewrite hooks are active. Use explicit `rtk ...` commands when RTK is installed.

## Required Startup Check
At the start of a substantial coding/session-analysis task, check whether RTK is available:

```powershell
Get-Command rtk -ErrorAction SilentlyContinue
```

If installed, use RTK wrappers by default.

If not installed, state that RTK is unavailable, avoid noisy commands, and use compact native alternatives until the user approves installation.

## Mandatory Command Preferences
Prefer:

```powershell
rtk git status
rtk git diff
rtk git log -n 10
rtk ls .
rtk read path\to\file
rtk grep "pattern" .
rtk find "*.py" .
rtk pytest
rtk test npm test
rtk lint
rtk tsc
rtk deps
rtk json config.json
rtk docker ps
rtk docker logs <container>
```

Instead of raw noisy commands such as full recursive listings, full test logs, full build logs, large `cat`, large `git diff`, or verbose dependency trees.

## When Full Output Is Needed
RTK filtering is not a substitute for exact evidence. Use raw output or RTK tee/full-output recovery when:

- A failing test needs complete stack trace.
- A security review needs exact payload/diff/log line.
- A migration/build failure is hidden by summary output.
- The user explicitly asks for full raw output.

Even then, read only the smallest relevant slice.

## Windows Notes
RTK supports native Windows filtering, but auto-rewrite hooks may not rewrite PowerShell commands automatically. For best reliability in Codex desktop on Windows:

- Call `rtk` explicitly.
- Keep command output compact.
- Use WSL only if the project and user workflow already support it.

## Privacy and Security
- Do not use RTK as permission to print secrets or PII.
- Do not run `rtk env` broadly; filter only allowed prefixes.
- Do not log raw customer data, tokens, connection strings, claim notes or production credentials.

## Agent Rule
RTK is mandatory when available. If unavailable, the agent must say so and continue with compact command discipline rather than raw noisy output.

## Related
- [[Codex Operating Guide]]
- [[Web App Security Checklist]]
- [[Secret Management]]
- [[App Architecture Playbook]]