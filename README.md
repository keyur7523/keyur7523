# Keyur Pawaskar

**Software Engineer — AI systems & full-stack.** I build LLM agents that ship into real workflows, and the evaluation, observability, and access-control layers that make them trustworthy enough to run in production.

Right now I'm the developer inside a cardiovascular practice, where the AI platform I built is used daily by clinicians — it cut a 20-minute manual documentation workflow to 2–3 minutes.

---

## What I Focus On

- **Agent systems** — tool-calling loops, multi-step orchestration, RAG and retrieval
- **Evaluation & reliability** — automated eval harnesses, trajectory vs. outcome scoring, regression and hallucination detection, cost/latency telemetry
- **Production guarantees** — authorization, audit trails, human-in-the-loop approval, graceful fallback

Most AI demos answer *"can it do the thing?"* I'm more interested in *"how do we know it did it correctly, and what happens when it doesn't?"*

---

## Projects

### [Northwind Support Agent](https://github.com/keyur7523/rag-assistant) — Multi-Tool AI Agent with Automated Evaluation

A customer-support agent that chains its own tools — SQLite order lookups, RAG policy search over Chroma, and drafted replies — to resolve requests end to end.

- Built on a Claude **tool-calling loop** that decides which tool to reach for and when
- **Automated eval harness** scoring *trajectory* (right steps) and *outcome* (right answer) separately — 18/18 passing
- Served behind FastAPI with structured tool contracts, versioned schemas, and reproducible eval runs

### [Delegate](https://github.com/keyur7523/delegate) — Transparent Agent Authorization for Gmail & Calendar &nbsp;·&nbsp; [live](https://delegate-client.vercel.app)

An AI assistant you can actually give real permissions to. Every action is visible, scopes are revocable mid-session, and high-risk actions require explicit approval.

- **Classifier-gated execution** — every tool call is risk-scored; high-risk calls block on step-up auth over SSE
- **Scope enforcement is server-side**, so it holds even if the model ignores its system prompt
- Multi-provider agent runtime (Anthropic / OpenAI / Gemini) on one unified tool-calling loop; BYOK, no credentials persisted server-side
- React 19 + TypeScript · Node/Express · direct Google OAuth 2.0 · 10 REST tools · 8 SSE event types

### [ProbeKit](https://github.com/keyur7523/probekit) — Behavioral Evaluation Toolkit for LLM Prompts &nbsp;·&nbsp; [live](https://probekit.vercel.app)

- Multi-model evaluation engine with cost/latency tracking across GPT, Claude, and Ollama
- Evaluators for instruction adherence, hallucination, stability, refusal behavior, and format consistency
- Regression detection and version-comparison dashboards with human-annotation accuracy tracking

### [PromptLab](https://github.com/keyur7523/promptLab) — LLM Experimentation & Evaluation Platform &nbsp;·&nbsp; [live](https://prompt-lab-gold.vercel.app/)

- Deterministic A/B experimentation with real-time SSE streaming and structured feedback capture
- End-to-end observability — structured logging with trace IDs, per-request cost tracking, live token/latency/spend dashboards
- Rust microservice for sub-1ms token estimation with automatic Python fallback
- FastAPI · PostgreSQL · Redis · React

### [Koda](https://github.com/keyur7523/koda) — AI Coding Agent &nbsp;·&nbsp; [live](https://koda-tau.vercel.app/)

- Multi-phase orchestration (understand → plan → execute → approve) with a recursive tool-use loop across 7 tools
- Agent reasoning streamed over FastAPI WebSockets at sub-second latency
- Cost-optimized model routing cut LLM API spend ~40%; human-in-the-loop review keeps every action reversible

### [AuthZ](https://github.com/keyur7523/authz) — Authorization & Approval Workflow Platform &nbsp;·&nbsp; [live](https://authz-liard.vercel.app/)

- Two-layer authorization: RBAC (roles → permissions) plus a JSON **policy engine** (PBAC) with deny-override-allow and default-deny
- Multi-tenant isolation via org scoping, immutable audit logging, and a full approval workflow state machine
- JWT with 15-min access tokens and rotating refresh tokens (SHA-256 hashed, invalidated on logout)
- FastAPI · async SQLAlchemy 2.0 · PostgreSQL · React 19

---

## Also Shipped

| | |
|---|---|
| **[CollabCanvas](https://github.com/keyur7523/collabcanvas)** · [live](https://collabcanvas-tau.vercel.app/) | Real-time collaborative canvas — Yjs CRDT over authenticated WebSockets, live cursors and presence |
| **[HireTrack](https://github.com/keyur7523/hiretrack)** · [live](https://hiretrack-puce.vercel.app/) | Multi-tenant hiring platform — granular RBAC, Redis idempotency, audit logging, async Postgres |
| **[DeepSearch](https://github.com/keyur7523/deep-search)** · [live](https://deep-search-two.vercel.app/) | Agentic research assistant — task-DAG planning, parallel retrieval, cited synthesis |
| **[Verbatim](https://github.com/keyur7523/verbaTim)** | Evaluation case study measuring and stabilizing verbosity drift across multi-turn LLM conversations |
| **[docr](https://github.com/keyur7523/docr)** | Local VLM OCR for messy documents — handwriting, diagrams, mixed layouts |
| **[Ember](https://github.com/keyur7523/ember)** | Self-hosted LLM inference on NVIDIA DGX Spark |

---

## Tech Stack

**Languages**  
Python · TypeScript · JavaScript · SQL · Rust (microservice)

**Backend**  
FastAPI · Flask · Node.js · Express · NestJS · REST · SSE/WebSockets

**Frontend**  
React · Next.js · Tailwind CSS

**AI/ML**  
LLM APIs (Anthropic, OpenAI, Gemini) · RAG & vector search (Chroma) · LangChain · agent evaluation

**Infra & Data**  
PostgreSQL · MongoDB · Redis · AWS · Docker · CI/CD

---

## Reach Me

[Portfolio](https://keyur-portfolio-psi.vercel.app) &nbsp;·&nbsp; [LinkedIn](https://www.linkedin.com/in/keyur-pawaskar-7b05b6169) &nbsp;·&nbsp; codekeyur7523@gmail.com
