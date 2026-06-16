<p align="center">
  <img src="assets/hero-banner.svg" alt="TriangleAI — AI work for Triangle small businesses, matched by AI and approved by a human." width="100%">
</p>

<h1 align="center">TriangleAI</h1>

<p align="center">
  <strong>Matchmaking — not a job board — that pairs Triangle small businesses with vetted university
  students who do real AI &amp; automation work at student rates.</strong><br>
  <em>Matched by AI. Approved by a human.</em>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/React_18-20232A?style=flat&logo=react&logoColor=61DAFB" alt="React 18">
  <img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat&logo=typescript&logoColor=white" alt="TypeScript">
  <img src="https://img.shields.io/badge/Vite-646CFF?style=flat&logo=vite&logoColor=white" alt="Vite">
  <img src="https://img.shields.io/badge/Supabase-3FCF8E?style=flat&logo=supabase&logoColor=white" alt="Supabase">
  <img src="https://img.shields.io/badge/Claude_API-C17D4A?style=flat&logo=anthropic&logoColor=white" alt="Claude API">
  <img src="https://img.shields.io/badge/AWS_S3_·_CloudFront-232F3E?style=flat&logo=amazonwebservices&logoColor=FF9900" alt="AWS S3 + CloudFront">
  <br>
  <img src="https://img.shields.io/badge/status-work_in_progress-C17D4A?style=flat" alt="Status: work in progress">
  <img src="https://img.shields.io/badge/region-Raleigh·Durham·Chapel_Hill-8A7B6B?style=flat" alt="Region: the Triangle">
  <img src="https://img.shields.io/badge/built_by-Claude_Builder_Ambassador-A5683C?style=flat" alt="Built by a Claude Builder Ambassador">
</p>

<p align="center">
  <a href="#what-it-is">What it is</a> ·
  <a href="#see-it">See it</a> ·
  <a href="#how-it-works">How it works</a> ·
  <a href="#under-the-hood">Under the hood</a> ·
  <a href="#tech-stack">Tech stack</a> ·
  <a href="#status--roadmap">Status</a> ·
  <a href="#about">About</a>
</p>

> **About this repository.** This is a **public showcase** of TriangleAI for fellow developers —
> what it does, why it exists, and how it's engineered. It contains **no application source code**;
> everything here is documentation, diagrams, and screenshots of the work-in-progress app running locally.

> 🚧 **Project status — early work in progress.** TriangleAI is a large, actively-developed project: a
> **working scaffold, not a finished or fully-functioning website yet.** The architecture, AI interview,
> matching engine, and operator console run end-to-end in local demo mode, but features are at different
> stages of completion, several integrations are still being wired up, and things will change. In
> particular, **university `.edu` verification (SSO + SheerID) is a work in progress right now** — see
> [Status &amp; roadmap](#status--roadmap). Treat this as a snapshot of an evolving build, not a launched product.

---

## What it is

Small businesses in the Research Triangle keep hearing *"AI could do that for you"* — and every
conversation ends on the same unanswered question: **okay, but who actually builds it?** Agencies are
expensive and slow. Freelancer marketplaces are noisy and unvetted. The owner doesn't have time to
learn the tools themselves.

Meanwhile, UNC, Duke, and NC State are full of capable CS / data / design students who want real,
résumé-grade project work and income — with no trusted channel to local businesses.

**TriangleAI closes that gap.** Both sides complete a short, adaptive **AI interview** instead of
writing job posts or browsing listings. A matching engine ranks the best pairings, **a human operator
approves every introduction**, and the work gets done — typically at **~20% of agency cost, in days
rather than weeks.**

The defining difference: **businesses never write a job posting, and students never browse listings.**
Both sides are interviewed into *structured data*, which is what makes ranking and human review fast
and high-signal.

---

## See it

> Screenshots of the work-in-progress app running locally (zero-config demo mode — seeded data, mock backend). It's an evolving scaffold, so expect rough edges.

### The landing page
<p align="center">
  <img src="assets/screenshots/landing-hero.png" alt="TriangleAI landing page" width="90%">
</p>

<details>
  <summary><strong>↳ See the full landing page</strong></summary>
  <br>
  <p align="center">
    <img src="assets/screenshots/landing-full.png" alt="The full TriangleAI landing page funnel" width="62%">
  </p>
</details>

### The AI interview — no forms, no job posts
A friendly, adaptive chat captures what a business *needs* (or what a student is *great at*) and turns
it into a structured brief. Text by default, with an optional voice mode.

<p align="center">
  <img src="assets/screenshots/interview.png" alt="The conversational AI interview" width="90%">
</p>

### The operator's match queue — AI ranks, a human approves
For each business need, the engine surfaces a ranked shortlist of candidates with a **fit score** and
a plain-English **"why this match"** rationale. Nothing is introduced until a human approves it.

<p align="center">
  <img src="assets/screenshots/admin-queue.png" alt="Admin match queue with AI-ranked candidates" width="90%">
</p>

---

## How it works

Three steps for the customer. Matchmaking, not a board.

```mermaid
flowchart LR
    A["1 · Make an account<br/><small>email · university SSO (WIP)</small>"] --> B["2 · Talk to the<br/>AI interviewer"]
    B --> C["Structured record<br/><small>need / profile</small>"]
    C --> D["AI-ranked match"]
    D --> E{"Human<br/>approval"}
    E -->|approved| F["3 · Introduction"]
    F --> G["Both accept"]
    G --> H["Engagement<br/><small>delivered · paid</small>"]

    classDef accent fill:#C17D4A,stroke:#A5683C,color:#fff;
    classDef soft fill:#F5EFE8,stroke:#E8E0D8,color:#3D2B1A;
    class A,B,F accent;
    class C,D,G,H soft;
```

1. **Make an account.** Businesses sign up with a work email. Students will sign in with their
   **university Google / Microsoft account** to prove a `.edu` identity — **this verification flow is a
   work in progress**, so an interim email sign-up is used today. No long forms.
2. **Talk to the AI interviewer.** A short, adaptive chat captures the need or the skill set — no
   postings, no applications.
3. **Get matched & introduced.** The engine ranks the best fits, **a person reviews and approves**, and
   TriangleAI makes the introduction. On accept, the work begins.

---

## What we build

High-leverage AI / automation work a student can deliver quickly. The menu is a starting point, not a
fence — anything that can be sped up by AI likely fits, and gets scoped in the interview.

| Service | What it covers |
|---|---|
| **Data cleanup** | Messy spreadsheets, dedup, format normalization, enrichment. |
| **Workflow automation** | Stitch tools together; replace manual copy-paste with a one-click pipeline. |
| **Chatbots & assistants** | Internal Q&A bots and customer-facing FAQ bots, scoped to your docs. |
| **Document processing** | Pull structured data out of contracts, invoices, intake forms, PDFs. |
| **Internal tool prototyping** | A working v1 of the dashboard or admin tool you keep meaning to build. |

---

## Under the hood

> The part for fellow developers. TriangleAI is a single-page React app with a **swappable backend**, an
> **AI layer that never exposes a key to the browser**, and a **deterministic fallback for every AI path**
> so it degrades gracefully. For the full write-up, see **[ARCHITECTURE.md](ARCHITECTURE.md)**.

### System at a glance

```mermaid
flowchart TB
    subgraph Client["Browser · React 18 + TypeScript (Vite)"]
        UI["Marketing site + app<br/><small>hand-rolled CSS-variable design system</small>"]
        IV["Interview chat<br/><small>text · optional voice</small>"]
        MATCH["Match views<br/><small>operator queue · status</small>"]
    end

    subgraph Server["Server-side only · keys never reach the browser"]
        PROXY["Claude proxy<br/><small>Vite dev API (local) · Supabase Edge Functions (prod)</small>"]
    end

    subgraph Supabase["Supabase"]
        AUTH["Auth<br/><small>university SSO · email OTP</small>"]
        PG[("Postgres<br/>+ Row-Level Security")]
    end

    CLAUDE["Claude API"]
    SHEERID["SheerID<br/><small>enrollment check</small>"]

    UI -->|"Backend interface"| PG
    UI --> AUTH
    MATCH --> PG
    IV --> PROXY
    PROXY --> CLAUDE
    AUTH --> SHEERID

    classDef accent fill:#C17D4A,stroke:#A5683C,color:#fff;
    classDef soft fill:#F5EFE8,stroke:#E8E0D8,color:#3D2B1A;
    classDef data fill:#FFFFFF,stroke:#C17D4A,color:#3D2B1A;
    class PROXY,CLAUDE accent;
    class UI,IV,MATCH,AUTH,SHEERID soft;
    class PG data;
```

### 1 · Swappable backend behind one interface

Every data operation goes through a single `Backend` interface. A **localStorage mock** implements it
for zero-config local development (seeded with demo data); a **Supabase** implementation backs
production. The app code never knows which is active — switching is a config flag, not a refactor.

```mermaid
flowchart LR
    APP["App code<br/><small>pages · context · services</small>"] --> IFACE[["Backend interface"]]
    IFACE -. "local / dev" .-> MOCK["Mock backend<br/><small>localStorage · seeded · zero-env</small>"]
    IFACE -. "production" .-> SUPA["Supabase backend<br/><small>Postgres · Auth · RLS</small>"]

    classDef accent fill:#C17D4A,stroke:#A5683C,color:#fff;
    classDef soft fill:#F5EFE8,stroke:#E8E0D8,color:#3D2B1A;
    class IFACE accent;
    class MOCK,SUPA soft;
```

The same pattern is used for the **AI interview provider** (scripted mock · Claude · voice) and the
**identity / enrollment** services — each is an interface with a dev implementation and a production
implementation, so the whole product runs end-to-end with **zero external dependencies** during
development.

### 2 · The AI layer keeps keys server-side — and always has a fallback

The conversational interview, structured extraction, and match ranking all run on the **Claude API**,
called **only from the server** (a Vite dev API locally, Supabase Edge Functions in production). The
browser never sees a key. Critically, **every AI path has a deterministic fallback**, so an outage or a
missing key degrades the experience instead of breaking it.

```mermaid
sequenceDiagram
    autonumber
    participant B as Browser
    participant P as Server proxy<br/>(Edge Function)
    participant C as Claude API
    B->>P: interview turn / rank request<br/>(no API key in browser)
    P->>C: prompt + server-side key
    alt Claude available
        C-->>P: structured response
        P-->>B: next question / ranked matches
    else unavailable, error, or rate-limited
        P-->>B: signals unavailable
        Note over B: falls back to the<br/>deterministic script / local scorer
    end
```

### 3 · How fit is scored

For each business need, the engine scores every candidate across weighted dimensions and surfaces a
ranked shortlist with rationale. **The same weights drive both the Claude ranker and the deterministic
fallback scorer**, so the two stay aligned and the output is explainable either way.

<p align="center">
  <img src="assets/matching-weights.svg" alt="Matching engine scoring weights" width="80%">
</p>

A minimum candidate pool is surfaced before the geography filter is widened, so a thin local pool never
produces an empty queue.

### 4 · Trust, vetting & security

- **Real identities (🚧 work in progress).** Students will authenticate with **university SSO** (Google /
  Microsoft) for a verified `.edu` identity rather than a self-asserted email. The flow is built but
  **currently feature-flagged off while it's being finished** — an interim email sign-up is active today.
- **Independent enrollment check (🚧 work in progress).** **SheerID** is integrated to confirm active
  enrollment before a student is matchable — **server-confirmed and bound to the verified account** so a
  student cannot self-certify. It ships with the SSO verification above and is part of the same in-progress work.
- **Row-Level Security everywhere.** Postgres RLS governs who can read or write each row. Cross-table
  authorization checks run in `SECURITY DEFINER` helper functions to keep policies non-recursive and
  auditable. Sensitive columns (e.g. verification flags) are writable **only** by a service-role function.
- **Rate limiting, inbound and outbound.** A database-backed atomic limiter protects every Edge Function;
  outbound calls to third-party APIs use retry-with-backoff and bounded concurrency that respects
  `Retry-After`.
- **Human in the loop.** No introduction is ever sent automatically — an operator approves each one.

### 5 · Graceful degradation, by design

| Path | Primary | Fallback |
|---|---|---|
| Interview | Claude conversational intake | Deterministic scripted interview |
| Extraction | Claude structured extraction | Heuristic field mapping |
| Match ranking | Claude ranker | Local weighted scorer (`same weights`) |
| Voice intake | Live voice provider | Text chat (voice is opt-in, off by default) |
| Backend | Supabase (Postgres + RLS) | localStorage mock (dev) |

The result: a clone runs with **`npm run dev` and zero environment variables** — seeded data, scripted
interview, local scorer — and lights up the real integrations (Claude, Supabase, and the rest) by adding
keys and flipping the relevant feature flags as each one is finished.

---

## Tech stack

| Layer | Choice | Notes |
|---|---|---|
| **Frontend** | React 18 · TypeScript · Vite | Hand-rolled CSS-variable design system (warm cream / terracotta; Lora + DM Sans). Tailwind is scoped to the interactive demo only. |
| **Routing** | React Router | Public marketing site at `/`; authenticated app under `/app/*`. |
| **Backend** | Supabase — Postgres · Auth · RLS · Edge Functions | Behind a swappable `Backend` interface; localStorage mock for dev. |
| **AI** | Anthropic **Claude API** | Interview, extraction, and ranking — server-side only, with deterministic fallbacks. |
| **Identity** 🚧 | University SSO (Google / Microsoft) · SheerID | `.edu` proof + independent enrollment verification — **work in progress** (interim email sign-up active today). |
| **Hosting** | AWS **S3 + CloudFront** | Static build; CI deploys on push to `main`. |
| **Type safety** | TypeScript `strict` (`noUnusedLocals`) | Build is `tsc -b && vite build`. |

> **Positioning:** built by a **Claude Builder Ambassador** on Anthropic's Claude — AI-native, not
> AI-bolted-on.

---

## Status & roadmap

**Stage: early work in progress — a scaffold, not a finished product.** TriangleAI is being built for a
single region (the Triangle — UNC · Duke · NC State), with every match approved by a human operator. It
is **not deployed as a fully-functioning public website yet.** The legend below reflects where each
piece actually stands:

> ✅ working in the development scaffold (local demo mode) · 🚧 in progress · 🔜 planned

- ✅ Conversational AI interview (text) with structured extraction
- ✅ AI-ranked matching with explainable rationale + deterministic fallback
- ✅ Operator console: match queue, approvals, engagements
- ✅ RLS, rate limiting, and graceful degradation across every AI path
- 🚧 **University `.edu` verification (SSO + SheerID)** — built, but currently feature-flagged off and
  being finished; an interim email sign-up is active today
- 🚧 Production wiring &amp; end-to-end hardening — the live, deployed experience is still coming together
- 🔜 Optional voice intake (spec'd; off by default)
- 🔜 **Phase 2:** Stripe Connect for in-app payouts + automated service fee (engagements are billed manually today)
- 🔜 Multi-region scale-out and a purpose-built agent catalog

**Business model (target):** a service fee per engagement (default **18%**) plus a monthly retainer for
active businesses. Customer value: roughly **20% of typical agency cost**, delivered in days.

---

## About

**TriangleAI** is operator-led, not a faceless platform — a real person stands behind every match.

- **Founder / operator:** Sai Kasani — CS + Finance, UNC · Claude Builder Ambassador
- **Region:** the Research Triangle, NC — Raleigh · Durham · Chapel Hill
- **Contact:** [sai.kasani@lafayettestandard.com](mailto:sai.kasani@lafayettestandard.com)

<p align="center">
  <img src="assets/mark.svg" alt="" width="34"><br>
  <sub>© 2026 Sai Kasani · TriangleAI. This repository is a public showcase and contains no application source code.</sub>
</p>
