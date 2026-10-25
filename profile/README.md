# Euraika-Labs

> A European AI research lab building **sovereign-by-default** AI systems, and studying how they break.

[euraika-labs.net](https://www.euraika-labs.net) — the editorial surface where we write about what we build.
[euraika.net](https://www.euraika.net) — the parent organisation.

Euraika-Labs builds AI infrastructure for organisations whose data, compliance posture, or jurisdiction makes US-cloud LLM stacks a non-starter. The systems run end-to-end inside the customer's own infrastructure under EU jurisdiction. This GitHub organisation hosts the open-source side of that work.

## Security research

Systems that handle regulated data are only as trustworthy as their failure modes, so part of our work is adversarial: we study how LLM systems fail and publish the controls that survived evaluation.

- **Prompt injection** — a vector taxonomy and the few mitigations worth the engineering. [Read](https://www.euraika-labs.net/engineering/2026-10-14-prompt-injection-vectors-and-mitigations)
- **Agent containment** — capability-scoped runtimes and approval gates for agents that can touch a filesystem, a network, or a keyboard. [Paper](https://www.euraika-labs.net/research/capability-scoped-runtimes) · [How Pan gates tool calls](https://www.euraika-labs.net/engineering/2026-08-19-the-approval-ledger)
- **Isolation and data flow** — gateways that refuse unclassified prompts, and prompt caches that cannot leak across tenants. [Gateway](https://www.euraika-labs.net/engineering/2026-06-05-why-our-gateway-rejects-unclassified-prompts) · [Cache](https://www.euraika-labs.net/engineering/2026-07-22-tenant-keyed-prompt-cache)
- **Evidence integrity** — tamper-evident yet redactable audit trails, and benchmarks that cannot be quietly re-tuned after the fact. [Hash chains](https://www.euraika-labs.net/engineering/2026-09-16-evidence-storage-redactable-chains)

## Open-source projects

### Agent safety and containment

| Project | Status | Stack | What it does |
|---|---|---|---|
| **[pan-agent](https://github.com/Euraika-Labs/pan-agent)** | stable | Go + Tauri + React | AI desktop agent. Full PC control behind an explicit approval system. Single static binary, no telemetry. |
| **[pan-ui](https://github.com/Euraika-Labs/pan-ui)** | stable | Next.js + TypeScript | Self-hosted web workspace for chat, skills, extensions, memory, profiles, and runtime controls. |
| **[pan-desktop](https://github.com/Euraika-Labs/pan-desktop)** | stable | Tauri + Rust | Native Windows desktop app for the Pan workspace. Hard fork of `fathah/hermes-desktop` (MIT). |
| **[personal-assistant](https://github.com/Euraika-Labs/personal-assistant)** | beta | JavaScript | Safety-reviewed Agent Skill for Claude Code and Codex. Intent gate, explicit authorisation for consequential actions, no telemetry. |
| **[personal-assistant-memory-routing](https://github.com/Euraika-Labs/personal-assistant-memory-routing)** | beta | JavaScript | Privacy-first memory recall across providers. Read-only, bounded, and marked as untrusted data. No automatic writes. |

### Evaluation and assurance

| Project | Status | Stack | What it does |
|---|---|---|---|
| **[open-grc-benchmark](https://github.com/Euraika-Labs/open-grc-benchmark)** | alpha | Python | Synthetic regression fixtures for source-grounded GRC assistants. Offline, frozen and hashed, no combined score. |
| **[ai-slopcheck](https://github.com/Euraika-Labs/ai-slopcheck)** | stable | Python | Deterministic scanner for AI-style code failures, including error-swallowing and leftover mocks. 72 rules. `pip install ai-slopcheck`. |
| **[benchforge](https://github.com/Euraika-Labs/benchforge)** | alpha | Rust | macOS workbench for reproducible benchmarks of local and cloud LLMs, with inspectable artifacts. |

## Commercial products

The commercial products ship under commercial licences but are designed to run end-to-end inside the customer's own infrastructure:

- **Aegis** — AI-powered compliance command center. Single-tenant SaaS for SOC 2, ISO 27001, NIS2, and EU AI Act compliance.
- **Hermes** (gateway) — Production LLM gateway. Multi-runtime, with a model catalogue, governance hooks into Aegis, and routing that respects EU jurisdiction by default.
- **Vane (Camiel)** — Privacy-focused AI answering engine with verified synthesis and citations.

More on each at [euraika-labs.net/about](https://www.euraika-labs.net/about).

## What "sovereign-by-default" means

A workload is *sovereign* under our definition when an organisation can run it end-to-end without any of its data, prompts, model weights, vector indices, or operational metadata leaving its jurisdiction, its network, or its legal control — and when this is the **default** configuration, not an enterprise tier. [Full definition](https://www.euraika-labs.net/engineering/2026-04-15-on-sovereign-by-default).

## Reporting a vulnerability

Found a security issue in one of our repositories? Please report it privately — see [SECURITY.md](https://github.com/Euraika-Labs/.github/blob/master/SECURITY.md). Do not open a public issue.

## Contact

- Email: [hello@euraika.net](mailto:hello@euraika.net)
- Website: [euraika-labs.net](https://www.euraika-labs.net)
- Parent organisation: [euraika.net](https://www.euraika.net)

The team: Bert Colemont, Andrei Lavrenov, Laurence Bedoret, Corey Stables, Amin Zakkane.
