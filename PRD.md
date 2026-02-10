# Codr — LLM-Driven Vibe-Coding App Generator (Portfolio PRD, Sanitized)

**Document date:** 2026-02-09  
**Status:** Portfolio-safe excerpt (implementation details/redacted)  
**Product concept:** An ND-friendly chat interface that converts messy human intent into **deployable, chainable micro-agents** (MCP-style) on **Cloudflare Workers** with a phase-based build pipeline.

---

## 1) Problem
Non-developers (founders/operators) can clearly describe *what they need* but get blocked by:
- translation gap between “human goal” → “technical spec” → “working app”
- fragile workflows and context drift in multi-step AI builds
- bloated, unintuitive tools that break flow and increase cognitive load

---

## 2) Target Users
**Primary:** neurodivergent founders/operators and lean teams who need fast, reliable micro-tools.  
**Secondary:** technical leads who want a repeatable “agent factory” for internal tools.

---

## 3) Goals
1. Turn a natural-language workflow description into a **minimal viable spec** in minutes.
2. Generate a **production-ready React/Vite app** (or micro-agent) with **ND-friendly UX** and consistent styling.
3. Deploy to **Cloudflare Workers (Workers for Platforms)** with isolated per-app routing.
4. Make outputs **chainable** (agent → agent) using clear contracts and state.
5. Reduce “AI degradation” via enforced schemas, versioned prompts, and gated steps.

### Non-goals
- Replace a full IDE.
- Build bespoke enterprise integrations without a defined connector layer.
- “Autonomous agent” behavior without guardrails/HITL gates.

---

## 4) Core User Journey
1. **Intake (6 questions):** clarify JTBD, inputs/outputs, constraints, environment.
2. **Planning:** turn answers into a scoped MVP spec + architecture.
3. **Build pipeline:** Foundation → Core → Styling → Integration → Optimization.
4. **Preview:** live preview + instructions.
5. **Deploy:** one-click deploy to Cloudflare + post-deploy checklist.
6. **Chain:** export contracts so the new agent can be invoked by other agents.

---

## 5) Functional Requirements

### 5.1 Intake & Spec
- Present questions one at a time (anti-overwhelm).
- Capture:
  - JTBD + definition of done
  - inputs (sources, formats)
  - outputs (schema + destination)
  - constraints (cost, privacy, latency, environment)
- Generate:
  - **PRD-lite** (one-page)
  - **Build spec** (developer-facing)
  - **State contract** (what persists)

**Acceptance criteria**
- A first-time user can finish intake in <7 minutes.
- Output contains: objective, scope, constraints, user flow, acceptance tests.

### 5.2 Orchestration & Agent Roles
- Support a primary orchestrator + sub-agents (planner, spec-writer, UI stylist, code generator, deployer, QA).
- Each sub-agent:
  - receives only the **minimum context slice** needed
  - returns structured output (schema)
- Orchestrator composes results into the final build artifact.

**Acceptance criteria**
- Sub-agent outputs validate against schema.
- Orchestrator can resume from any step (idempotent stages).

### 5.3 Code Generation & Templates
- Generate React/Vite app scaffolds from templates (e.g., dashboard, tool, form).
- Enforce style system / tokens for consistent UI.
- Produce deploy-ready code with build instructions.

**Acceptance criteria**
- Build succeeds locally on first run (no missing deps).
- App includes required UX patterns (see §7).

### 5.4 Deployment
- Deploy apps to Cloudflare Workers (Workers for Platforms model).
- Provide step-by-step deployment instructions + rollback note.

**Acceptance criteria**
- User can deploy without editing source code (unless advanced mode).
- Deployment emits URL + health check result.

### 5.5 Observability & Safety
- Log every stage result + timestamps + input hashes.
- Provide “why this changed” diff notes between iterations.

**Acceptance criteria**
- Any stage can be audited post-hoc.
- Failures include actionable error messages.

---

## 6) Data & State Model (Conceptual)
A single “truth object” persists across the pipeline.

- **SpecCore:** mission, scope, constraints, definition of done
- **BuildState:** chosen template, UI tokens, current stage, decisions
- **Contracts:** input/output schema for each agent/module
- **Artifacts:** files generated + deployment metadata

---

## 7) ND-Friendly UX Requirements (High Signal)
- One question at a time; explicit progress cues.
- Clear “done / next” actions; no ambiguous CTAs.
- Low visual clutter; generous spacing; readable typography.
- Gentle motion + glow accents (fun, not distracting).
- Defaults that work; advanced options tucked away.

---

## 8) Non-Functional Requirements
- **Reliability:** deterministic stage boundaries; retries with backoff.
- **Security:** secrets never echoed; least-privilege connectors.
- **Performance:** avoid giant-context calls; summarize + reference state.
- **Cost control:** token budgeting per stage; caching where safe.
- **Accessibility:** contrast, reduced motion option, keyboard nav.

---

## 9) Success Metrics
- Time-to-first-deploy
- % successful deploys on first attempt
- User-reported “flow preserved” score (simple 1–5)
- Reuse rate of generated templates/agents
- Drift incidents (context mismatch) per build

---

## 10) Risks & Mitigations (selected)
- **Context drift** → state contract + schema validation + stage gating
- **Over-generation/bloat** → “bare-minimum prototype” mode + template constraints
- **User overwhelm** → progressive disclosure + micro-steps
- **Model variance** → eval cases + golden outputs + HITL gates

---

## 11) Open Questions
- Preferred connector layer (Make/Zapier/Pipedream vs native)
- Auth + user memory: when to introduce without bloating MVP?
- Team collaboration: versioning + permissions model
