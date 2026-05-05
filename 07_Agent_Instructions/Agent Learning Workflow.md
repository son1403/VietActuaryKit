---
type: agent-instruction
status: active
owner: Son
updated: 2026-05-05
tags: [agent-learning, harness-engineering, codex-ready, verification]
---

# Agent Learning Workflow

## Purpose
This note defines how an AI agent should learn from VietActuaryKit while working. The goal is not to make the agent memorize everything. The goal is to make it follow a repeatable loop: orient, clarify, act narrowly, verify, and preserve reusable learning.

This workflow is inspired by practical agent guidelines such as think-before-coding, simplicity first, surgical changes, and goal-driven execution.

## The Loop

```text
1. Orient
2. Clarify
3. Choose the smallest useful action
4. Execute surgically
5. Verify
6. Capture reusable learning
```

## 1. Orient
Before acting, identify the task type and read the minimum relevant context.

| Task Type | Read First |
|---|---|
| Any large task | [[VietActuaryKit Home]], [[Codex Operating Guide]], [[RTK Token Optimization Playbook]] |
| Insurance analytics | [[Non-Life Insurance Vietnam Overview]], relevant actuarial playbook |
| Policy/claim/customer data | [[Data Privacy Checklist]], [[Policy Data Contract]], [[Claim Data Contract]] |
| Pricing or loss ratio | [[Pricing Pack Playbook]] or [[Loss Ratio Analysis Playbook]] |
| Legal/regulatory question | [[Regulatory Source Register]], relevant regulatory note |
| App/SaaS engineering | [[SaaS Product Discovery Checklist]], [[App Architecture Playbook]], [[Web App Security Checklist]] |

## 2. Clarify
Do not silently pick an interpretation when the task is ambiguous.

The agent should state assumptions or ask when unclear about:

- Data grain.
- Data cut-off.
- Metric definition.
- Product scope.
- User role and permissions.
- Whether data contains PII or sensitive fields.
- Whether the output is internal analysis, production code, public documentation, or regulatory-facing material.

## 3. Choose The Smallest Useful Action
Prefer the minimum change or analysis that solves the user request.

Avoid:

- Speculative features.
- Broad refactors.
- New abstractions for one-off work.
- Extra frameworks or tools that the project does not already use.
- Large generated documents when a focused checklist or patch is enough.

## 4. Execute Surgically
Touch only the relevant files, notes, or analysis steps.

Rules:

- Match existing structure and style.
- Do not rewrite unrelated content.
- Do not remove pre-existing material unless the user asks.
- Do not weaken privacy, legal, security, or RTK token-control rules.
- Clean up only artifacts created by the current change.

## 5. Verify
Every non-trivial task should end with a check.

Examples:

| Work Type | Verification |
|---|---|
| Markdown/template update | Link check, local path scan, sensitive pattern scan |
| Coding change | Relevant tests, type check, lint, build, or focused smoke test |
| Data workflow | Reconciliation, data quality check, metric definition check |
| Legal/regulatory note | Source URL, effective date, Legal/Compliance caveat |
| Agent workflow update | Confirm `AGENTS.md`, dashboard, and linked playbooks stay consistent |

## 6. Capture Reusable Learning
After a task, decide whether anything should become reusable knowledge.

Capture only generic, public-safe, reusable material:

- New checklist item.
- Better template wording.
- New data quality rule.
- New agent behavior rule.
- New verification scenario.
- New regulatory source link.

Do not capture:

- Raw customer data.
- Claim notes.
- Policy IDs.
- Internal pricing assumptions.
- Company-specific process details.
- Secrets or production configuration.

## Learning Output Format
When preserving a lesson, write it like this:

```markdown
## Lesson
What changed in the workflow?

## When To Apply
What future task should trigger this lesson?

## Guardrails
What must the agent not do?

## Verification
How do we know the lesson is applied correctly?
```

## Success Criteria
The workflow is working if:

- The agent asks clarifying questions before making risky assumptions.
- Diffs are smaller and easier to review.
- The agent links to the relevant playbook/checklist before acting.
- Verification is explicit.
- Reusable improvements land in templates or playbooks, not scattered chat history.

## Related
- [[Codex Operating Guide]]
- [[RTK Token Optimization Playbook]]
- [[AgentBrain Test Scenarios]]
- [[Project AGENTS.md Template]]
