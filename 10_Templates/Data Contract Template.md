---
type: template
template_for: data-contract
status: active
tags: [template, data-contract, codex-ready]
---

# Data Contract Template

```markdown
---
type: data-contract
domain:
status: draft
owner: Son
updated: YYYY-MM-DD
tags: [data-contract, codex-ready]
---

# Dataset Name

## Purpose
Dataset dùng để làm gì.

## Grain
Một dòng đại diện cho điều gì.

## Core Fields
| Field | Meaning | Type | Nullable | Notes |
|---|---|---|---|---|
| id | | | | |

## Business Rules
- Rule 1:
- Rule 2:

## Data Quality Checks
- Check 1:
- Check 2:

## Privacy Notes
- PII fields:
- Sensitive fields:
- Masking/aggregation requirements:

## Agent Instruction
Agent cần tuân thủ gì khi dùng dataset này.

## Related
- [[Data Privacy Checklist]]
```