---
type: playbook
area: billing-subscription
status: active
owner: Son
updated: 2026-05-04
tags: [billing, subscription, saas, payments, codex-ready]
---

# Billing and Subscription Playbook

## Purpose
Hướng dẫn thiết kế billing/subscription cho SaaS theo hướng an toàn, idempotent và audit được.

## Billing Model
- Free, trial, paid, enterprise/manual invoice.
- Seat-based, usage-based, tiered, flat subscription hoặc hybrid.
- Billing owner khác với workspace admin không.
- Grace period, cancellation, downgrade, failed payment.

## Guardrails
- Payment/webhook actions must be idempotent.
- Do not trust client-side price or entitlement.
- Entitlements should be derived from trusted billing state.
- Webhook signature verification is mandatory.
- Billing changes need audit log.

## Agent Instruction
- Read provider docs from official source before implementing billing.
- Identify environment variables and secret management.
- Add tests for webhook replay/duplicate events.
- Keep billing state changes server-side.

## Related
- [[Secret Management]]
- [[API Design Playbook]]