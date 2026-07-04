# Microsoft Copilot Studio — Progressive Agent Mastery Portfolio (2026)

A component-by-component Copilot Studio project portfolio: nine hands-on projects spanning **Beginner → Intermediate → Advanced → Expert**, plus a **capstone** that unifies every capability into one governed enterprise mesh. Each project isolates one Copilot Studio building block — knowledge grounding, web/anonymous publishing, Power Automate actions, structured Dataverse/SharePoint data, custom APIs & MCP servers, generative orchestration, multi-agent systems, and governance — so you can learn (and demonstrate) each piece deliberately instead of copying one tutorial that vaguely touches everything.

> **Kept current as of July 4, 2026.** Copilot Studio's licensing model changed materially in the last year (messages → Copilot Credits, September 2025; Agent Pre-Purchase Plan added February 2026; multi-agent orchestration GA April 2026; New Orchestrator/Agentic Reasoning Loop and computer-using agents GA May 2026). Every project below reflects that current state — see the licensing primer below before you build anything.

---

## 📂 Projects by difficulty

| Tier | # | Project | Core capability | Preview |
|---|---|---|---|---|
| 🟢 Beginner | 1 | [KB-Agent-101](./projects/01-beginner-knowledge-base-agent/README.md) | Knowledge sources, generative answers | [🔗 Preview](https://rahul7387.github.io/copilot-studio-agent-mastery-projects/projects/01-beginner-knowledge-base-agent/index.html) |
| 🟢 Beginner | 2 | [WebGround-Agent](./projects/02-beginner-web-data-agent/README.md) | Public website grounding, anonymous channel | [🔗 Preview](https://rahul7387.github.io/copilot-studio-agent-mastery-projects/projects/02-beginner-web-data-agent/index.html) |
| 🟡 Intermediate | 3 | [FlowConnect-Agent](./projects/03-intermediate-power-automate-agent/README.md) | Power Automate actions, agent flows, Adaptive Cards | [🔗 Preview](https://rahul7387.github.io/copilot-studio-agent-mastery-projects/projects/03-intermediate-power-automate-agent/index.html) |
| 🟡 Intermediate | 4 | [DataLink-Agent](./projects/04-intermediate-sharepoint-dataverse-agent/README.md) | Dataverse MCP tool, SharePoint lists, code interpreter | [🔗 Preview](https://rahul7387.github.io/copilot-studio-agent-mastery-projects/projects/04-intermediate-sharepoint-dataverse-agent/index.html) |
| 🟠 Advanced | 5 | [APIBridge-Agent](./projects/05-advanced-custom-api-mcp-agent/README.md) | Custom connectors, self-hosted custom MCP server | [🔗 Preview](https://rahul7387.github.io/copilot-studio-agent-mastery-projects/projects/05-advanced-custom-api-mcp-agent/index.html) |
| 🟠 Advanced | 6 | [OrchestrAI-Agent](./projects/06-advanced-generative-orchestration-agent/README.md) | New Orchestrator, Skills, Bring Your Own Model | [🔗 Preview](https://rahul7387.github.io/copilot-studio-agent-mastery-projects/projects/06-advanced-generative-orchestration-agent/index.html) |
| 🔴 Expert | 7 | [MultiAgentMesh](./projects/07-expert-multi-agent-orchestration/README.md) | Embedded/connected agents, A2A interoperability, Fabric | [🔗 Preview](https://rahul7387.github.io/copilot-studio-agent-mastery-projects/projects/07-expert-multi-agent-orchestration/index.html) |
| 🔴 Expert | 8 | [GovernOps-Agent](./projects/08-expert-governance-cost-agent/README.md) | Admin governance, credit monitoring, an agent that governs agents | [🔗 Preview](https://rahul7387.github.io/copilot-studio-agent-mastery-projects/projects/08-expert-governance-cost-agent/index.html) |
| ⭐ Capstone | 9 | [Unified Copilot Mesh](./projects/09-capstone-unified-copilot-mesh/README.md) | All eight capabilities, one governed system | [🔗 Preview](https://rahul7387.github.io/copilot-studio-agent-mastery-projects/projects/09-capstone-unified-copilot-mesh/index.html) |

> Live previews are static HTML/CSS mockups approximating each project's real Copilot Studio look & feel (chat UI, activity map, orchestration canvas, admin dashboards). They are visual references only, not functional agents.

---

## 🧭 How to use this repo

- **New to Copilot Studio?** Build Projects 1 → 8 in order. Each one deliberately depends on lessons from the previous tier — Project 3's action-safety pattern assumes you understand Project 1's grounding; Project 7's multi-agent security assumes Project 4's data-security lessons.
- **Want one project to demo to leadership?** Go straight to **Project 9 (Capstone)** — it references every pattern below it and closes on the cost/governance story that actually gets budget approved.
- **Only care about one capability?** Every project is self-contained enough to build independently if you already understand the prerequisites called out in its README.

---

## 💳 Copilot Credits & Licensing Primer (current as of July 2026)

Read this before building anything — it's the single biggest source of surprise bills and the thing every project in this repo explicitly reasons about.

### The core model
- Since **September 1, 2025**, Copilot Studio's metered unit is the **Copilot Credit** (it replaced the older "messages" unit — same underlying meter, new name and framing).
- A Copilot Credit measures the **work an agent does per turn** — retrieving information, grounding on knowledge, calling a tool/action, running a flow, or invoking generative/reasoning AI. Different activities cost different numbers of credits, and a single turn can stack multiple charges (e.g., a grounded answer that also triggers an action might cost 2 + 5 = 7 credits).
- Rough reference rates used throughout this repo's projects: generative answer ≈ 2 credits; tenant-graph grounding ≈ 10 credits; a standard action/tool call ≈ 5 credits; premium/advanced-reasoning tools cost meaningfully more; **autonomous/proactive triggers cost a flat 25 credits — even for Microsoft 365 Copilot licensed users**, since autonomous triggers are never zero-rated.

### What's free vs. what's metered
- If your users hold **Microsoft 365 Copilot** licenses ($21/user/month standard, promotional $18/user/month for ≤300 users through June 30, 2026 for Business; $30/user/month for Enterprise) and the agent runs **inside Microsoft 365** (Copilot Chat, Teams, SharePoint) for **authenticated, licensed users only** — usage is **largely zero-rated**, subject to fair-use limits. This covers classic answers, generative answers, tenant-graph grounding, agent actions, and agent flows.
- The moment an agent is published to an **external/anonymous channel** (public website, WhatsApp, a custom app) or used by **unlicensed users**, it requires a **standalone Copilot Studio license** and consumes metered Copilot Credits regardless of your M365 Copilot entitlements. This exact boundary is the focus of Project 2.

### The four ways to pay for Copilot Credits
1. **Pay-as-you-go** — $0.01/credit, billed monthly through a linked Azure subscription. No upfront commitment; best for unpredictable or pilot-stage usage.
2. **Prepaid Copilot Credit capacity packs** — $200/month for 25,000 credits. Unused credits **do not roll over**. Best for predictable, steady volume.
3. **Copilot Credit Commit Units (CCCU) pre-purchase plan** — a one-year upfront pool; each CCCU = $1 of consumption (100 credits), with volume discounts from 5% at 3,000 CCCUs up to 20% at 3,000,000 CCCUs. Falls back to PAYG automatically once exhausted.
4. **Microsoft Agent Pre-Purchase Plan (Agent Commit Units / ACUs)** — added February 2026; works like CCCUs but draws down across **Copilot Studio, Microsoft Foundry, and increasingly Fabric and GitHub agentic services**, for organizations standardizing spend across Microsoft's whole agentic stack.

### Things every project in this repo explicitly accounts for
- **Bring Your Own Model (Foundry-hosted)** usage incurs Copilot Credits for the Copilot Studio orchestration **and** separate Azure OpenAI/Foundry per-token charges for the model itself — two invoices, not one (see Project 6).
- **Managed Environments**, if enabled, require every active user to be covered by a proper license or PAYG meter — limited Power Platform rights bundled in Dynamics 365/M365 licenses do not satisfy this (see Project 8).
- **AI Builder credits are being folded into the Copilot Credit model** — seeded AI Builder credits end and Power Apps/Power Automate AI Builder usage shifts to Copilot Credit billing rates. Budget for this transition if your agents touch AI Builder-adjacent capabilities (see Projects 3, 4, and the Capstone).
- **Credits don't roll over** on prepaid capacity packs — don't over-buy against optimistic volume forecasts.
- Use the official **Copilot Studio agent usage estimator** (agent type, traffic, orchestration mode, knowledge, tools) to forecast cost *before* you scale traffic — every project's "Token / Copilot Credit utilization" section in this repo is designed to feed directly into that estimator.

*(Prices and mechanisms above are US list rates as published mid-2026; Microsoft updates these regularly — always confirm current figures on Microsoft's live Copilot Studio pricing and licensing pages before committing budget.)*

---

## 🏗️ Common practices applied across every project

1. **Confirm-before-act** on any state-changing action (Projects 3, 4, 6, 7) — no agent in this repo silently executes a write, a cancellation, or an approval without checking with a human first.
2. **Security inherits from the data layer, not the LLM** — Dataverse security roles and SharePoint permissions are the enforcement mechanism (Project 4); the agent never becomes the thing deciding who can see what.
3. **External/non-Microsoft integrations carry explicit accountability documentation** — Project 5 and 7 both call out, in writing, who owns vetting an external MCP server or A2A partner agent.
4. **Cost is a design input, not an afterthought** — every project's architecture includes at least one decision (agent flow vs. cloud flow action, embedded vs. connected agent, deep reasoning on/off) made partly *because of* its Copilot Credit implications.
5. **Governance scales with capability** — the more autonomous and powerful an agent becomes (Project 6's Agentic Reasoning Loop, Project 7's multi-agent mesh), the more explicit its guardrails and consumption caps must be.

---

## 🔧 Platform & tooling baseline (as of July 2026)

- Copilot Studio on the **Copilot Credits** consumption model (replacing "messages" since September 2025)
- **New Orchestrator / Agentic Reasoning Loop** generally available (multi-step autonomous planning within a single agent)
- **Multi-agent orchestration** generally available (April 2026) — embedded/child agents, connected agents, and **Agent2Agent (A2A)** interoperability with non-Copilot-Studio agents
- **Model Context Protocol (MCP)** generally available for both consuming external MCP servers and publishing your own
- **Immersive Prompt Builder** (GA) embedded directly in the agent's Tools tab
- **Bring Your Own Model** via deep Microsoft Foundry integration (11,000+ models, including GPT, Llama, DeepSeek, and fine-tuned custom models)
- **Code interpreter** (GA) for Python-powered data analysis directly inside agent conversations
- **Fabric Data Agents** for governed, audited grounding on enterprise analytics data
- **Microsoft Agent Pre-Purchase Plan (ACUs)**, added February 2026, spanning Copilot Studio, Foundry, and (increasingly) Fabric/GitHub agentic services
- AI-powered **governance agents** in the Power Platform admin center for tenant-wide real-time risk assessment

---

## 📌 Suggested presentation order

1. Start with the **Capstone (Project 9)** for a manager/leadership audience — one coherent story across every difficulty tier, closing on cost governance.
2. Use **Projects 1-8** as deep-dive appendices when a specific stakeholder (security, finance, a particular business team) wants to go deeper on exactly one capability.

---

## 📄 License

This repository is provided as a personal learning/portfolio and internal proof-of-concept reference. Adapt freely for your own organization's Copilot Studio POC and training needs. Licensing and pricing figures cited throughout are informational summaries of Microsoft's published rates as of mid-2026 — always verify current terms on Microsoft's official Copilot Studio licensing and pricing pages before making purchasing decisions.
