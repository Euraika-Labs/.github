# Euraika-Labs

> A European AI research lab building **sovereign-by-default** AI systems.

[euraika-labs.net](https://www.euraika-labs.net) — the editorial surface where we write about what we build.
[euraika.net](https://www.euraika.net) — the parent organisation.

Euraika-Labs builds AI infrastructure for organisations whose data, compliance posture, or jurisdiction makes US-cloud LLM stacks a non-starter. The systems run end-to-end inside the customer's own infrastructure under EU jurisdiction. This GitHub organisation hosts the open-source side of that work.

## What "sovereign-by-default" means

A workload is *sovereign* under our definition when an organisation can run it end-to-end without any of its data, prompts, model weights, vector indices, or operational metadata leaving its jurisdiction, its network, or its legal control — and when this is the **default** configuration, not an enterprise tier.

This rules out major US hyperscalers as substrate; it does not rule out US-headquartered software shipped on-prem. The full definition lives at [euraika-labs.net/engineering/2026-04-15-on-sovereign-by-default](https://www.euraika-labs.net/engineering/2026-04-15-on-sovereign-by-default).

## Open-source projects

| Project | Status | Stack | What it does |
|---|---|---|---|
| **[pan-agent](https://github.com/Euraika-Labs/pan-agent)** | stable | Go + Tauri + React | AI desktop agent. Full PC control behind an explicit approval system. Single static binary. |
| **[pan-ui](https://github.com/Euraika-Labs/pan-ui)** | stable | Next.js + TypeScript | Web UI for chat, skills, extensions, memory, profiles, and runtime controls. |
| **[pan-desktop](https://github.com/Euraika-Labs/pan-desktop)** | stable | Tauri + Rust | Native Windows desktop wrapper for the Hermes Agent. |
| **[pan-office](https://github.com/Euraika-Labs/pan-office)** | experimental | Godot | 3D engine for Pan's spatial layer. |
| **[hermes-agent](https://github.com/Euraika-Labs/hermes-agent)** | beta | Python | Long-running, memory-aware, schedulable agent framework. |
| **[ai-slopcheck](https://github.com/Euraika-Labs/ai-slopcheck)** | stable | Python | Deterministic scanner for AI-style code failures. 72 rules. `pip install ai-slopcheck`. |
| **[omi-regolo-integration](https://github.com/Euraika-Labs/omi-regolo-integration)** | beta | Swift + Python | EU-privacy-mode patch package for [BasedHardware/omi](https://github.com/BasedHardware/omi). |

The Pan family is composed of four sibling repositories shipped on independent cadences: `pan-agent` (the binary), `pan-ui` (the workspace UI), `pan-desktop` (the Windows wrapper), and `pan-office` (the spatial layer). The agent itself lives at `hermes-agent`. *Pan is the workspace; hermes-agent is the worker.*

## Commercial products

The commercial products ship under commercial licences but are designed to run end-to-end inside the customer's own infrastructure:

- **Aegis** — AI-powered compliance command center. Single-tenant SaaS for SOC 2, ISO 27001, NIS2, and EU AI Act compliance.
- **Hermes** (gateway) — Production LLM gateway. Multi-runtime, with a model catalogue, governance hooks into Aegis, and routing that respects EU jurisdiction by default.
- **Vane (Camiel)** — Privacy-focused AI answering engine with verified synthesis and citations.

More on each at [euraika-labs.net/about](https://www.euraika-labs.net/about).

## Editorial

We post in a single institutional voice. The writing is at [euraika-labs.net](https://www.euraika-labs.net) — engineering posts about how we built things, position pieces that make our terms precise, and the occasional research item with methodology and a result. There are no per-author bylines; credibility, if it accrues, accrues to the lab.

The team behind it: Bert Colemont, Andrei Lavrenov, Laurence Bedoret, Corey Stables, Amin Zakkane.

## Contact

- Email: [hello@euraika.net](mailto:hello@euraika.net)
- Website: [euraika-labs.net](https://www.euraika-labs.net)
- Parent organisation: [euraika.net](https://www.euraika.net)
