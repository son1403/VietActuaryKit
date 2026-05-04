<div align="center">

# VietActuaryKit

### A public Obsidian knowledge-base template for Vietnam non-life insurance actuaries, data analysts, and AI agents

[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Obsidian Compatible](https://img.shields.io/badge/Obsidian-compatible-7C3AED.svg)](https://obsidian.md/)
[![AI Agent Ready](https://img.shields.io/badge/AI%20Agent-ready-blue.svg)](#agent-workflow)
[![Vietnam Non-Life Insurance](https://img.shields.io/badge/Vietnam-Non--Life%20Insurance-red.svg)](#regulatory-foundation)

<img width="1122" height="642" alt="VietActuaryKit preview" src="https://github.com/user-attachments/assets/5109aac5-4c49-4c05-a2a0-bf3f455f6d7d" />

</div>

---

VietActuaryKit is a Markdown-first knowledge base for actuaries and analytics teams working with Vietnam non-life insurance workflows. It gives human analysts and AI coding/data agents a shared operating layer: domain notes, actuarial playbooks, data contracts, privacy guardrails, regulatory source references, and app/SaaS engineering checklists.

Use it as an Obsidian vault, copy selected folders into your existing vault, or adapt the templates into your own private agent brain.

## Why VietActuaryKit?

Most actuarial and insurance analytics work lives across Excel files, SQL snippets, dashboards, policy/claim extracts, regulatory notes, and undocumented assumptions. AI agents can help, but only if they are given reliable guardrails.

VietActuaryKit helps you make those guardrails explicit:

- What an agent must check before touching policy, claim, or customer data.
- How to define earned premium, incurred claims, loss ratio, exposure, and data cut-off.
- Which Vietnam regulatory sources should be reviewed before insurance/data workflows.
- How to structure pricing, loss ratio, reserving, dashboards, and internal app/SaaS work.
- What must stay private when publishing templates or using AI tools.

## Quick Start

```powershell
git clone https://github.com/son1403/VietActuaryKit.git
cd VietActuaryKit
```

Then choose one workflow:

| Workflow | What To Do |
|---|---|
| Use as an Obsidian vault | Open the cloned folder directly in Obsidian. |
| Merge into an existing vault | Copy the numbered folders into your private Obsidian vault. |
| Use with Codex/AI agents | Start with `AGENTS.md`, `RTK.md`, and `07_Agent_Instructions/`. |
| Build project-specific guidance | Copy `10_Templates/Project AGENTS.md Template.md` into your repo as `AGENTS.md`. |

Start here:

```text
01_Dashboard/VietActuaryKit Home.md
```

## What You Get

| Area | Included Notes |
|---|---|
| Insurance domain | Vietnam non-life insurance overview, product/claim/policy context |
| Regulatory references | Insurance law, personal data protection, cybersecurity, consumer protection, digital transactions |
| Actuarial analytics | Loss ratio and pricing pack playbooks |
| Data contracts | Policy and claim data contract templates |
| Data privacy | PII/sensitive data checklist and agent guardrails |
| Agent operations | Codex operating guide, RTK token optimization, skills index pattern |
| App/SaaS engineering | Product discovery, architecture, API, database, auth/RBAC, billing, deployment |
| Security and governance | Secret management, audit log, retention, web app security checklist |
| Templates | Playbook, regulation note, data contract, project `AGENTS.md` |

## Repository Structure

```text
VietActuaryKit/
  00_Inbox/
  01_Dashboard/
  02_Glossary/
  03_Regulatory_Knowledge/
  04_Business_Domain/
  05_Actuarial_Playbooks/
  06_Data_Analytics/
  07_Agent_Instructions/
  08_Project_Knowledge/
  09_Decision_Log/
  10_Templates/
  11_Product_SaaS/
  12_Engineering_Playbooks/
  13_UI_UX_System/
  14_Security_Compliance/
  15_Deployment_Operations/
```

`08_Project_Knowledge` and `09_Decision_Log` are intentionally empty in the public template. Keep private project context and decision logs in a private vault or private repository.

## Agent Workflow

VietActuaryKit is designed to be readable by coding and data agents. The intended flow is:

1. Read `AGENTS.md`.
2. Read `01_Dashboard/VietActuaryKit Home.md`.
3. For coding or repo exploration, use `RTK.md` and `12_Engineering_Playbooks/RTK Token Optimization Playbook.md`.
4. For insurance/data work, read `03_Regulatory_Knowledge/Data Privacy Checklist.md`.
5. For pricing/loss ratio work, read the relevant playbook in `05_Actuarial_Playbooks/`.
6. For app/SaaS work, read product, architecture, auth/RBAC, security, and deployment playbooks.

The key rule: agents should not jump directly into code or analysis before checking data privacy, business assumptions, data grain, and regulatory context.

## Regulatory Foundation

The regulatory section keeps public source references for Vietnam insurance and data/privacy topics, including:

- Law on Insurance Business.
- Decrees and circulars guiding insurance business.
- Mandatory insurance rules.
- Personal data protection rules.
- Data governance and cybersecurity references.
- Digital transactions and consumer protection references.

These notes are intentionally source-linked and checklist-oriented. They are not a substitute for official legal interpretation.

## Public-Safety Boundaries

This repository is a public template. It intentionally excludes:

- Customer, policy, claim, employee, agent, broker, hospital, garage, or beneficiary identifiers.
- Company-specific pricing logic, reserving assumptions, commission structures, reinsurance terms, profitability views, or underwriting rules.
- Internal workflows, internal dashboards, private project notes, decision logs, and production configuration.
- Secrets, credentials, API keys, tokens, connection strings, private keys, and `.env` files.

When adapting this template, keep sensitive project material in your private vault.

## Suggested Use Cases

- Build a private actuarial operating manual.
- Standardize loss ratio and pricing review workflows.
- Create consistent data contracts for policy and claim analytics.
- Give AI agents guardrails before they work with insurance datasets.
- Bootstrap internal app/SaaS requirements for actuarial or analytics teams.
- Maintain a regulatory source register with practical analyst checklists.

## Roadmap Ideas

- Reserving/IBNR playbook.
- IFRS 17 analyst notes.
- Reinsurance analytics playbook.
- Power BI semantic model checklist.
- SQL analytics pattern library.
- Synthetic sample datasets for demonstrations.
- Vietnamese glossary of actuarial and non-life insurance terms.

## Contributing

Contributions are welcome if they keep the repository generic, public-safe, and useful for actuaries and AI agents. See [CONTRIBUTING.md](CONTRIBUTING.md).

Before contributing, do not include customer data, claim data, policy data, secrets, internal company workflows, or proprietary assumptions.

## Disclaimer

VietActuaryKit is a knowledge-base template for AI coding/data agents and actuarial/data workflows. It is not legal, actuarial, insurance, security, privacy, tax, financial, or compliance advice. Validate all regulatory content with official sources and qualified professionals.

## License

MIT License. See [LICENSE](LICENSE).
