<div align="center">

# Rishikesh Rai
### Systems & AI Infrastructure Engineer · Model Context Protocol (MCP) · Agent Sandboxing

[![GitHub Followers](https://img.shields.io/github/followers/kingroyale537?label=Follow&style=flat-square&color=238636&logo=github)](https://github.com/kingroyale537)
[![TypeScript](https://img.shields.io/badge/TypeScript-007ACC?style=flat-square&logo=typescript&logoColor=white)](https://www.typescriptlang.org/)
[![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)](https://python.org)
[![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)](https://docker.com)
[![Model Context Protocol](https://img.shields.io/badge/MCP-Anthropic_Ecosystem-8A2BE2?style=flat-square)](https://modelcontextprotocol.io/)
[![Status](https://img.shields.io/badge/Seeking-Founding_Engineer_/_Systems_SWE-00E676?style=flat-square)](#founder-tldr)

<p align="center">
  <b>Building hardened runtime infrastructure, low-latency execution proxies, and sandbox isolation layers for autonomous AI agents.</b><br>
  <i>Obsessed with high-agency shipping, sub-millisecond systems performance, and zero-trust security boundaries.</i>
</p>

[Featured Systems](#featured-systems) • [Open Source (YC Contributions)](#open-source) • [Engineering Principles](#philosophy) • [Tech Stack](#tech-stack) • [Get in Touch](#contact)

---

</div>

<a id="founder-tldr"></a>
## ⚡ Founder & Recruiter TL;DR

If you are a **YC founder, CTO, or AI Lab Engineering Lead** looking for an engineer who operates with extreme ownership:

- **High-Agency Velocity**: Zero ramp-up friction. Hand me an open technical challenge or RFC, and I ship tested, benchmarked, production-ready architecture in days.
- **Deep Systems Rigor**: Experienced in POSIX process isolation, containerization, WebSocket protocol multiplexing, and Model Context Protocol (MCP) gateways.
- **Production-Grade Craftsmanship**: 100% test coverage on critical paths, path-traversal prevention, automated credential scrubbing, and sub-millisecond execution budgets.
- **Consistent Builder**: Proven multi-year shipping history across distributed systems, agent backends, and developer platforms.

---

<a id="featured-systems"></a>
## 🛡️ Featured Systems

### 1. [MCP-Shield — Zero-Trust Security & Sandbox Gateway](https://github.com/kingroyale537/mcb-shield-)
> **High-performance security proxy, capability enforcement engine, and ephemeral sandbox for Model Context Protocol (MCP) agents.**

```
┌─────────────────┐       ┌────────────────────────────────────────────────────────┐       ┌──────────────────────┐
│  AI Host/Client │       │                   MCP-SHIELD GATEWAY                   │       │   Upstream Server    │
│ (Claude/Cursor) │ ◄───► │  [Capability Policy] ──► [HITL Approval] ──► [Sandbox]  │ ◄───► │ (FS / Shell / APIs)  │
└─────────────────┘       └─────────────────────────┬──────────────────────────────┘       └──────────────────────┘
                                                    │ Telemetry (WS)
                                                    ▼
                                       ┌──────────────────────────┐
                                       │ Real-Time Dark Dashboard │
                                       └──────────────────────────┘
```

- **Sub-Millisecond Overhead**: Benchmarked routing and capability validation overhead **< 1.0 ms** per tool call.
- **Capability Policy Engine**: Fine-grained regex and path canonicalization preventing directory traversal (`../../etc/shadow`), unauthorized network access, and privilege escalation.
- **Multi-Driver Ephemeral Sandbox**: Dual-mode execution engine supporting Docker containerization and isolated host child processes with automated secret scrubbing (`AWS_*`, `OPENAI_*`, `GITHUB_*`).
- **Human-in-the-Loop (HITL) Escalation**: Interactive approval hooks for sensitive or mutating actions (e.g. system commands, write operations) with customizable timeouts.
- **Real-Time Observability**: Built-in HTTP + WebSocket telemetry server streaming live security audits and invocation metrics to a dark-mode dashboard.
- **100% Verified**: 25/25 automated Vitest unit & integration test suite passing.

```bash
# Quickstart
git clone https://github.com/kingroyale537/mcb-shield-.git
pnpm install && pnpm test && pnpm demo
```

---

### 2. [InsForge — All-in-One Backend Platform for Agentic Coding](https://github.com/kingroyale537/InsForge)
> **Full-stack backend infrastructure designed specifically for autonomous coding agents.**

- Supplies coding agents with instantaneous database provisioning, authentication, ephemeral compute, file storage, and unified AI gateway routing.
- Eliminates context-switching for autonomous coding agents, enabling full-stack application deployment from natural language specifications.

---

### 3. [TerraSentry AI — Autonomous Physical Due Diligence Agent](https://github.com/kingroyale537/mireye-terrasentry-ai)
> **Multi-agent autonomous intelligence pipeline for geospatial risk and property due diligence (Mireye Challenge).**

- Orchestrates specialized agents for satellite imagery inspection, zoning verification, and environmental risk assessment.
- Implements deterministic tool scheduling, structured JSON validation, and automated PDF dossier generation.

---

<a id="open-source"></a>
## 🤝 Open Source & Ecosystem Contributions

### [E2B (YC S24)](https://github.com/e2b-dev/E2B) — Sandboxed Cloud Environments for AI
*Contributed to core runtime and Model Context Protocol (MCP) SDK gateway architecture.*
- **Issue Resolution (`#1899`)**: Identified and fixed camelCase vs snake_case parameter divergence (`install_cmd`/`run_cmd` vs `installCmd`/`runCmd`) between Python and TypeScript SDKs when passing custom server configs to `mcp-gateway`.
- **Cross-Language Test Harness**: Authored comprehensive unit tests in Python (Pytest) and TypeScript (Vitest) validating runtime configuration parity inside microVM containers.

---

<a id="philosophy"></a>
## 🧠 Engineering Philosophy

| Principle | How I Practice It |
| :--- | :--- |
| **Bias for Action** | I prioritize functioning prototypes over endless debate. Build $\to$ Measure $\to$ Iterate. |
| **Zero-Trust by Default** | Never trust raw LLM output. Tool execution must always be sandboxed, bounded, and audited. |
| **Type Safety & Ergonomics** | Strict TypeScript and Python type annotations. Clear APIs that fail at compile time, not in production. |
| **Relentless Testing** | Edge-case fuzzing, traversal attack simulations, and end-to-end integration flows on every commit. |
| **Deep Systems Empathy** | Understanding what happens beneath the abstraction layer—from POSIX signals and syscalls to WebSocket framing. |

---

<a id="tech-stack"></a>
## 🛠️ Technical Arsenal

<div align="center">

| Domain | Technologies & Frameworks |
| :--- | :--- |
| **Languages** | `TypeScript` `Python` `Rust` `Go` `C++` `SQL` `Bash` |
| **AI & Agent Infra** | `Model Context Protocol (MCP)` `Tool Interception Proxies` `Anthropic Claude API` `OpenAI Assistants` `LangChain` `LlamaIndex` |
| **Systems & Cloud** | `Docker` `MicroVMs / E2B` `Linux / POSIX Internals` `WebSockets` `Node.js Async I/O` `HTTP/2` `Redis` `PostgreSQL` |
| **Security & Isolation** | `Path Canonicalization` `Secret Redaction` `Capability-Based Access Control (CBAC)` `Sandbox Hardening` |
| **DevOps & Testing** | `Vitest` `Pytest` `GitHub Actions CI/CD` `pnpm / Turborepo` `Docker Compose` |

</div>

---

<a id="contact"></a>
## 📬 Let's Build Together

I am actively speaking with **YC founders, AI research labs, and early-stage infrastructure teams** looking for high-velocity engineers who can own critical systems from day zero.

- 📧 **Direct Email**: [knhtheroyaldevelopers@gmail.com](mailto:knhtheroyaldevelopers@gmail.com)
- 🐙 **GitHub**: [github.com/kingroyale537](https://github.com/kingroyale537)
- 📍 **Availability**: Open to Founding Engineer, Systems/AI Infrastructure roles (Full-time or High-impact Contract)
- 🌍 **Timezone**: Adaptable with US Pacific / US Eastern / European engineering hours

<div align="center">
  <sub>Engineered with precision · Tested with rigor · Shipped with velocity</sub>
</div>
