<div align="center">

# 🇸🇦 Unified Banking Platform (UBP)

### A bilingual, Arabic-first **Open Finance** banking super-app for the Saudi market.

*Unifying 13 banking domains, 7 user roles, and an AI-native Security Operations Centre into one cohesive experience.*

[![Live Demo](https://img.shields.io/badge/Live%20Demo-ubp.aboalrejal.com-0A66C2?style=for-the-badge&logo=vercel&logoColor=white)](https://ubp.aboalrejal.com/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.8-3178C6?style=for-the-badge&logo=typescript&logoColor=white)](#tech-stack)
[![React](https://img.shields.io/badge/React-19-61DAFB?style=for-the-badge&logo=react&logoColor=black)](#tech-stack)
[![TanStack Start](https://img.shields.io/badge/TanStack%20Start-1.168-FF4F1A?style=for-the-badge&logo=reactquery&logoColor=white)](#tech-stack)
[![Supabase](https://img.shields.io/badge/Supabase-PostgreSQL-3FCF8E?style=for-the-badge&logo=supabase&logoColor=black)](#tech-stack)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind%20v4-2.2-06B6D4?style=for-the-badge&logo=tailwindcss&logoColor=white)](#tech-stack)

[📄 Design Brief (PDF)](./Hackathon-Amad-26.pdf) · [Live Site](https://ubp.aboalrejal.com/) · [Architecture](#architecture)

</div>

> 📌 **About this repository.** Per the hackathon submission requirements, the **source code was not requested** — only the design brief and a link to the live product. This public repository therefore hosts the **design brief (PDF), documentation, and demo access**, while the **full codebase remains private** in the live deployment. The structure and feature detail below describe that codebase to convey the project's true scope. **The fastest way to evaluate UBP is the live demo:** [ubp.aboalrejal.com](https://ubp.aboalrejal.com/).

---

---

## 📖 Overview

**UBP** is a fully interactive, production-grade prototype of a Saudi national banking platform built on the principles of **Open Banking / Open Finance**, **SAMA regulatory compliance**, and **Zero-Trust security**. It collapses what is traditionally a dozen disconnected banking apps into a single, role-aware experience — from retail dashboarding to corporate SME payroll, from AI-assisted fraud investigation to phygital (physical + digital) branch operations.

The platform serves **7 distinct roles**, is driven by **realistic Saudi market data**, speaks **Arabic-first (RTL)** with full English support, and ships with a live **AI Security Operations Centre (SOc)** powered by a Model Context Protocol (MCP) tool server and streaming LLM chat.

> 🟢 **Live demo:** [ubp.aboalrejal.com](https://ubp.aboalrejal.com/) — sign in with the demo credentials below.

---

## 🧠 The Core Idea — A Cyber Omni-Agent for Saudi Banking

UBP is not just another banking app. Its beating heart is an **autonomous cyber Omni-Agent** — a team of AI agents designed to run 24/7 on dedicated servers, continuously probing, testing, and defending the unified banking surface.

**The inspiration:** Recent frontier AI models have demonstrated the ability to *independently discover* real-world vulnerabilities (e.g., a Linux kernel flaw surfaced by an autonomous model). UBP turns that same capability inward — harnessing generative AI as a permanent, autonomous red-and-blue team for the Saudi financial sector.

**How it works:**
1. **Unify** — Every bank's data flows into one platform via Open Banking connectors.
2. **Understand** — The Omni-Agent ingests newly-disclosed CVEs and threat intel, and checks whether our banks' systems are vulnerable.
3. **Attack + Protect** — It simulates real attacks (penetration testing) and recommends or applies fixes *before* attackers exploit them.
4. **Alert** — Because the agent sees all banks through one API, it detects cross-bank fraud and money-laundering patterns invisible to any single bank, and alerts the relevant cyber team in real time.

> 📍 **Implementation status:** The platform UI, the connectors framework, the **MCP server (95 tools)**, the AML/fraud/SIM-swap modules, and the AI chat are **built and live**. The 24/7 autonomous agent farm and live ATM camera analysis are **designed and on the roadmap** — the architecture is ready, pending bank sandbox access.

---

## ❓ The Problem

**Saudi banks operate as isolated silos, and their defense against fraud and cyber threats is reactive rather than proactive.**

| # | The Gap | Why it matters |
|---|---------|----------------|
| 1 | **Technological isolation between banks** | Each bank runs its own API and ledger. Laundered or stolen funds are scattered across institutions, making cross-bank tracking impossible for any single bank. |
| 2 | **Physical security disconnected from digital** | Fraud systems monitor *numbers only* — they fail to detect deepfakes or a customer under physical coercion at an ATM. |
| 3 | **Slow, complex regulatory compliance** | Matching millions of daily transactions against SAMA's evolving rules is slow and consumes enormous human resources. |
| 4 | **Reactive, not proactive defense** | New CVEs, SIM-swap fraud, and bot attacks surface daily, but banks respond only *after* the loss. |

## ✅ The Solution

| Problem | How UBP solves it |
|---------|-------------------|
| **Bank isolation** | Smart connectors (Connectors) pull data from every bank into one unified schema — with a **cross-bank AML Tracker** that traces laundered money in real time across an interactive cluster map. |
| **Physical ↔ digital gap** | A **Smart Branch (Phygital)** module ingests live ATM camera feeds for AI analysis of micro-expressions and body language, freezing disbursement the moment coercion or a deepfake is detected. |
| **Slow compliance** | A **SAMA Autopilot** engine reads every operation in real time, matches it against SAMA regulations, auto-generates compliance reports, and freezes violating transactions. |
| **Reactive defense** | The **Omni-Agent** team runs 24/7 to hunt, test, and patch threats proactively across the unified surface. |

---

## ✨ Highlights

- **13 deeply-featured screens**, each independently demonstrable with live micro-interactions.
- **AI-native SOc** — a streaming copilot backed by **12 MCP tool groups** that query real platform data.
- **Bilingual & RTL-first** — Arabic is the primary language; every string flows through an i18n layer.
- **Saudi-grade compliance** — SAMA rules, SAR currency, valid SA IBANs, Open Banking connectors.
- **Mock-first architecture** — runs with zero backend, swappable to live Supabase (Auth + RLS) with no page-code change.
- **Design-system purity** — built entirely on the Saudi **National Design System (NDS/DGA)** UI registry and the official Saudi Riyal currency icon.

---

## 🖥️ The 13 Modules

| # | Module | Route | What it does |
|---|--------|-------|--------------|
| 1 | **Dashboard** | `/dashboard` | Unified balance overview across all banks, multi-bank cards, transaction drawer, instant refresh. |
| 2 | **Analytics** | `/analytics` | Personal-finance forecasting with a live salary slider — liquidity forecasts update instantly. |
| 3 | **Fraud Monitoring** | `/fraud-monitoring` | Real-time fraud case queue (bots, spam, abnormal patterns), card freeze, cross-page alert toasts, "Simulate Attack" demo. |
| 4 | **AML Tracker** | `/aml-tracker` | **Cross-bank Anti-Money-Laundering** — an interactive cluster map that traces laundered funds across banks, merchants, and ATMs to their final destination. |
| 5 | **Consent Management** | `/consent` | Open Finance consent ledger — grant/revoke third-party app access with a full audit timeline. |
| 6 | **Credit Score** | `/credit-score` | Accessible credit meter with actionable "How to raise my score" guidance. |
| 7 | **Investments** | `/investments` | Live market prices flashing every 5 s (pausable), portfolio tracking. |
| 8 | **Smart Escrow** | `/smart-escrow` | **Conditional contracts** — funds release only on delivery confirmation (capital held in escrow), protecting peer/merchant transactions. |
| 9 | **Compliance (SAMA)** | `/compliance` | **SAMA Autopilot** — reads every operation in real time, matches it against SAMA regulations, auto-generates compliance reports with PDF export, and freezes violating transactions. |
| 10 | **Connectors** | `/connectors` | Open Banking data-source registry — the plumbing that unifies every bank's API into one schema. |
| 11 | **SOc — Security Ops Centre** | `/soc` | AI copilot dashboard + streaming chat over 12 MCP tool groups; triages live fraud linked to the cyber agent. |
| 12 | **Zero-Trust Identity** | `/zero-trust` | **SIM-swap detection** (via telco integration) + device-fingerprint analysis + OTP step-up auth — blocks account takeover the instant a chip is swapped. |
| 13 | **Branch Ops (Phygital)** | `/branch-ops` | **Smart branches** — designed to ingest live ATM camera feeds for AI analysis of coercion, stress, or masked faces; freezes disbursement and alerts authorities. ITM stress-detection demo. |

> Plus the **SME Corporate Portal** (`/sme`) — a maker/checker payroll batch flow with **AI-driven funding** that generates tailored financing offers based on a company's real cash flow, expenses, and sector.
>
> And the **Open Finance Marketplace** — third-party apps (STC Pay, digital wallets, Tamara, etc.) and per-bank add-ons (e.g., Zakat calculator) installable on demand.

---

## 🔐 Demo Access

The live site runs in **mock mode** (no real backend). Sign in on the `/login` page with:

| Field | Value |
|-------|-------|
| **Email** | `aboalrejal.ai@gmail.com` |
| **Password** | `Aabb055@` |

You can switch between all **7 roles** at any time via the header **Role Switcher**, each landing on its own default screen.

---

## ⭐ Capabilities & Innovations

**The unique value UBP brings to the Saudi financial sector:**

1. **AI-native, not AI-bolted-on** — a real **MCP server exposing 95 tools across 12 groups**. The AI queries the *same live data layer* the UI renders — zero hallucination.
2. **Cross-bank AML mind-map** — an interactive cluster map that traces laundered funds across banks, merchants, and ATMs to their final destination, defeating silo-based laundering.
3. **Live fraud detection linked to the cyber agent** — real-time attack feeds (bots, spam, abnormal transfers) triaged by the SOc in seconds.
4. **Zero-Trust identity** — SIM-swap detection via telco integration and device-fingerprint analysis block account takeover the instant a chip is swapped.
5. **Smart conditional escrow** — funds release only on delivery confirmation, holding capital safely for peer/merchant transactions.
6. **Phygital branch ops** — AI analyzes live ATM camera feeds to detect coercion, stress, or masked faces, freezing disbursement and alerting authorities.
7. **AI-driven SME funding** — generates tailored financing offers based on a company's real cash flow, expenses, and sector — not a clerk's guess.
8. **SAMA automated compliance (RegTech)** — a regulatory engine surfacing violations, inspected operations, and key health indicators in real time.
9. **Marketplace & extensible connectors** — third-party apps (STC Pay, digital wallets, Tamara) and per-bank add-ons (e.g., Zakat calculator) installable on demand.
10. **Bilingual, Arabic-first RTL** — built entirely on the Saudi **National Design System (NDS/DGA)** with the official Saudi Riyal icon — authentically local.

---

## 🤖 AI & The Security Operations Centre

UBP is **AI-native**, not AI-bolted-on. Two real intelligence surfaces ship in this prototype, both linked to the autonomous **Omni-Agent**:

1. **SOc Streaming Chat** (`/soc`) — a conversational analyst built on the **Vercel AI SDK** + **Lovable AI Gateway**, supporting **multiple frontier models** (Gemini 3 Flash, GPT-5.4, GPT-5.5). It streams responses, honors connector mentions, and scopes searches — a live copilot for fraud and compliance analysts.
2. **MCP Tool Server** (`/api/mcp`) — a **Model Context Protocol** endpoint exposing **95 tools across 12 groups** that the model calls to read live platform state:

   `dashboard` · `analytics` · `connectors` · `security` · `soc` · `compliance` · `aml` · `escrow` · `sme` · `marketplace` · `system` · `finance`

   This means the AI doesn't hallucinate — it queries the same data layer the UI renders, and the same layer the Omni-Agent defends.

---

## 🗂️ Project Structure

UBP is a substantial, production-minded codebase — **171 TypeScript modules**, **23 routes**, **83 UI primitives**, and **95 AI tools across 12 MCP groups**. The full source tree (organized by responsibility) is shown below. This repository hosts the brief & documentation; the live, deployed codebase is summarized here to convey the project's true scale and architecture.

> **At a glance:** `171` source files · `23` routes · `83` NDS UI components · `95` MCP tools · `7` roles · `13` modules · `3` dedicated engines.

```text
ubp/
├── src/
│   ├── routes/                          # 23 routes — file-based (TanStack Router)
│   │   ├── __root.tsx                   # App shell: Sidebar + TopBar + Toaster
│   │   ├── index.tsx                    # Landing → redirects to /login or /dashboard
│   │   ├── login.tsx                    # Demo role selector (7 roles)
│   │   ├── app.tsx                      # Auth-guarded layout + role resolution
│   │   ├── api/
│   │   │   ├── mcp.ts                   # MCP tool-server endpoint (JSON-RPC)
│   │   │   └── soc-chat.ts              # AI streaming chat endpoint (Vercel AI SDK)
│   │   └── app/                         # ── The 13 feature modules ──
│   │       ├── dashboard.tsx            #   1  /dashboard          — unified balances
│   │       ├── analytics.tsx            #   2  /analytics           — PFM forecasting
│   │       ├── fraud-monitoring.tsx     #   3  /fraud-monitoring   — live fraud queue
│   │       ├── aml-tracker.tsx          #   4  /aml-tracker         — mule detection
│   │       ├── consent.tsx              #   5  /consent             — Open Finance ledger
│   │       ├── credit-score.tsx         #   6  /credit-score        — score meter
│   │       ├── investments.tsx          #   7  /investments         — live markets
│   │       ├── smart-escrow.tsx         #   8  /smart-escrow        — programmatic escrow
│   │       ├── compliance.tsx           #   9  /compliance          — SAMA reporting
│   │       ├── connectors.tsx           #  10  /connectors          — data aggregation
│   │       ├── soc.tsx                  #  11  /soc                  — AI Security Ops
│   │       ├── zero-trust.tsx           #  12  /zero-trust          — OTP step-up auth
│   │       ├── branch-ops.tsx           #  13  /branch-ops          — phygital branch
│   │       ├── sme.tsx                  #      /sme                  — SME payroll portal
│   │       └── settings.tsx + .account / .consent  — preferences
│   │
│   ├── components/                      # Composite + primitive UI layer
│   │   ├── ui/                          # 83 NDS/DGA shadcn primitives (registry-only)
│   │   ├── icons/                       # SaudiRiyalIcon + nds-icons integration
│   │   ├── layout/                      # App shell, sidebar, topbar, navigation
│   │   ├── home/                        # Landing-page marketing sections
│   │   ├── soc/                         # Security Operations Centre widgets
│   │   ├── aml/                         # Anti-money-laundering visualizations
│   │   ├── escrow/                      # Smart-escrow state visuals
│   │   └── shared/                      # Cross-cutting reusable composites
│   │
│   ├── lib/                             # Core logic, engines & data layer
│   │   ├── api/                         # Data-adapter contract (mock ↔ Supabase)
│   │   ├── mcp/                         # MCP server + registry + 12 tool groups
│   │   │   ├── server.ts · registry.ts · require-auth.ts · context.ts
│   │   │   └── tools/                   # 95 tools:
│   │   │       ├── dashboard.ts   (8)   ├── connectors.ts   (12)
│   │   │       ├── analytics.ts   (9)   ├── soc.ts           (6)
│   │   │       ├── escrow.ts      (8)   ├── compliance.ts    (12)
│   │   │       ├── sme.ts         (9)   ├── aml.ts           (7)
│   │   │       ├── marketplace.ts (6)   ├── security.ts      (4)
│   │   │       ├── system.ts      (8)   └── finance.ts       (6)
│   │   ├── mock-data.ts                 # Realistic Saudi market dataset
│   │   ├── sama-engine.ts               # SAMA compliance-rule engine
│   │   ├── escrow-state-machine.ts      # Escrow lifecycle state machine
│   │   ├── connectors-engine.ts         # Open Banking connector orchestration
│   │   ├── ai-gateway.server.ts         # Lovable AI Gateway provider
│   │   ├── ai-models.ts                 # Model registry + modes/scopes
│   │   ├── i18n.tsx                     # Bilingual strings + RTL plumbing
│   │   ├── supabase.ts                  # Client (Auth + RLS)
│   │   ├── error-capture.ts             # Error boundary + reporting
│   │   ├── types.ts · constants.ts · utils.ts
│   │   └── lovable-error-reporting.ts
│   │
│   ├── hooks/                           # use-mobile · use-theme · use-toast
│   ├── integrations/                    # External service integrations
│   ├── styles/                          # Tailwind v4 tokens (tokens.css)
│   ├── router.tsx · server.ts · start.ts
│   └── styles.css
│
├── specs/001-unified-banking-platform/  # Full specification suite
│   ├── plan.md · research.md · data-model.md · quickstart.md · spec.md · tasks.md
│   ├── contracts/                       # routes · data-layer · cross-page behaviors
│   └── checklists/                      # Phase-gate verification
├── docs/                                # Architecture, NDS specs, Deep Research corpus
└── sync/                                # Sync configuration
```

### Domain engines (the "secret sauce")

Beyond UI, UBP ships three purpose-built engines that make the data *behave* like real banking:

| Engine | Responsibility |
|--------|----------------|
| **`sama-engine`** | Encodes SAMA regulatory rules — validation, reporting logic, compliance flags. |
| **`escrow-state-machine`** | Full lifecycle for smart-escrow transactions (fund → hold → release / dispute). |
| **`connectors-engine`** | Orchestrates Open Banking data-source aggregation across institutions. |

---

## 🧰 Tech Stack

| Layer | Technology |
|-------|-----------|
| **Language** | TypeScript 5.8 |
| **UI Framework** | React 19.2 |
| **Meta-framework** | TanStack Start 1.168 (SSR/SPA) |
| **Routing** | TanStack Router 1.170 (file-based) |
| **Server State** | TanStack Query 5.101 |
| **Tables** | TanStack Table 8.21 |
| **Styling** | Tailwind CSS v4.2 (token-driven, no config file) |
| **UI Registry** | Saudi NDS / DGA — 83 shadcn primitives |
| **Icons** | `@aboalrejal/nds-icons` + `SaudiRiyalIcon` |
| **Charts** | Recharts 2.15 |
| **Forms** | react-hook-form 7 + zod 4 + @hookform/resolvers |
| **AI** | Vercel AI SDK 7 + Lovable AI Gateway — multi-model (Gemini 3 Flash, GPT-5.4/5.5) · MCP server (95 tools) |
| **Backend / DB** | Supabase (PostgreSQL, Auth, RLS) — mock-first adapter |
| **Rich Text** | TipTap 3 |
| **Testing** | Vitest + @testing-library/react · Playwright (e2e) |

---

## 📚 Data Sources & Research Methodology

This platform is grounded in real Saudi banking context. The domain knowledge, API conventions, regulatory framing, and Open Finance architecture were compiled using three complementary deep-research instruments, then synthesized:

| Instrument | Role in this project |
|-----------|----------------------|
| **Google Gemini Deep Research** | Broad sweep of Saudi Open Banking, SAMA regulation, and Open Finance standards. |
| **Perplexity Deep Research** | Verified, cited technical detail on APIs, Open Banking connectors, and security patterns. |
| **NotebookLM** | Synthesis & comprehension layer — cross-referencing sources, distilling the data model, and pressure-testing the domain understanding. |

The full deep-research corpus, data model, and technical specification underpin this prototype and are summarized in the [📄 Design Brief (PDF)](./Hackathon-Amad-26.pdf).

---

## 🏗️ Architecture

```text
        ┌──────────────────────────────────────────────┐
        │                Browser (RTL UI)                │
        │   React 19 · TanStack Router · Tailwind v4   │
        └───────────────────┬──────────────────────────┘
                            │  TanStack Query
        ┌───────────────────▼──────────────────────────┐
        │          Data Adapter (swappable)             │
        │   ┌──────────────┐      ┌─────────────────┐   │
        │   │ Mock adapter │ ◄──► │ Supabase adapter│   │
        │   │ (localStorage)│     │ (Auth + RLS)    │   │
        │   └──────────────┘      └─────────────────┘   │
        └───────────┬───────────────────┬──────────────┘
                    │                   │
        ┌───────────▼────────┐  ┌───────▼────────────────┐
        │  /api/soc-chat     │  │     /api/mcp            │
        │  (AI streaming)    │  │  (12 MCP tool groups)   │
        └────────────────────┘  └─────────────────────────┘
```

The **mock-first** adapter means every page works with zero backend. Flip one env var and the identical page code talks to live **Supabase** with row-level security — no UI rewrite.

---

## 🚀 Try It Live

The fastest way to experience UBP is the deployed demo — no setup required:

1. Open **[ubp.aboalrejal.com](https://ubp.aboalrejal.com/)**.
2. Sign in with the **demo credentials** above.
3. Use the header **Role Switcher** to explore all 7 personas.
4. Trigger the live demo actions listed in the [13 Modules](#-the-13-modules) table — e.g. *Simulate Fraud Attack* on `/fraud-monitoring`, or ask the AI on `/soc`.

<details>
<summary><b>🔧 Run locally from source</b></summary>

This repository hosts the **design brief and documentation**. The full source code is available on request. To run the codebase locally:

```bash
npm install
npm run dev        # → Vite dev server (TanStack Start)
npm run build      # production build
npm run test       # vitest unit/component tests
npm run test:e2e   # playwright e2e
```

In **mock mode** (`VITE_DATA_ADAPTER=mock`, the default) the app runs entirely on a local dataset — no backend needed.

</details>

---

## 👥 Roles

The platform is role-aware across **7 personas** — each lands on a purpose-built default screen and sees only what their role permits:

`Retail Customer` · `SME Owner` · `Finance Manager` · `Compliance Officer` · `Fraud Analyst` · `Branch Officer` · `Security Operations`

---

## 📄 Design Brief & Submission

The completed **design brief** for this submission is included in this repository as [📄 `Hackathon-Amad-26.pdf`](./Hackathon-Amad-26.pdf). It documents the full problem statement, design rationale, data model, and feature walkthrough.

---

<div align="center">

**Built with precision for the Saudi banking sector.**

*Open Finance · Zero-Trust · AI-native · Arabic-first*

</div>
