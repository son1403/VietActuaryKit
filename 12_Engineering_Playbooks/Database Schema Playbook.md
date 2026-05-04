---
type: playbook
area: database-schema
status: active
owner: Son
updated: 2026-05-04
tags: [database, schema, saas, codex-ready]
---

# Database Schema Playbook

## Purpose
Thiết kế schema cho app/SaaS sao cho rõ grain, query được, migrate được và bảo vệ dữ liệu tốt hơn.

## Entity Design
- Define entity purpose and owner.
- Define grain: one row means what.
- Use stable primary keys.
- Add tenant/org/workspace key for multi-tenant data.
- Separate lookup/config tables from transactional data.
- Track important status transitions.

## Standard Columns
- `id`.
- `tenant_id` / `organization_id` / `workspace_id` when multi-tenant.
- `created_at`, `updated_at`.
- `created_by`, `updated_by` for user-driven data.
- `deleted_at` for soft delete when audit matters.
- `status` for workflow entities.

## Migration Rules
- Backward-compatible migration first when possible.
- Separate schema change from destructive cleanup.
- Never drop important columns without backup/rollout plan.
- Seed/reference data should be versioned.

## Related
- [[Data Retention and Audit Log]]
- [[Web App Security Checklist]]