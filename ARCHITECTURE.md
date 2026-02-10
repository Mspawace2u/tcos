# Architecture — Codr + MCP Mappr (Portfolio View)

This architecture shows two complementary pieces:

1) **Codr** — an LLM-driven build + deploy pipeline for micro-agents
2) **MCP Mappr** — a diagramming “translator” that produces a machine-readable `map.json` plus a styled schematic

## A) Codr high-level flow
1. **Intake** (6-question flow)
2. **Plan** (scoped MVP + constraints)
3. **Build** (template + generation)
4. **Deploy** (Cloudflare Workers)
5. **Chain** (contracts + invocation metadata)

## B) MCP Mappr flow
Input: “human-speak” spec (or an agent analysis)  
Output: 
- `map.json` (consumable by a viewer or renderer)
- a styled schematic (napkin-glow style)

Included in this pack:
- `map.json` (machine-readable)
- `schematic_viewer.html` (self-contained renderer)



## D) State + artifact store (anti-degradation core)
- **Persisted state:** the system’s truth (constraints, decisions, stage outputs) lives in a DB/service (serverless, SaaS, or local DB).
- **Traceable runs:** each build run uses a trace ID so you can replay what happened.
- **Version pointers:** PRD/orchestration/map versions are recorded alongside artifacts.

**Why it matters:** this prevents context collapse across long agent runs and makes the system auditable.

## C) Why this matters (Technical CoS lens)
- Consistent artifacts (PRD, contracts, diagrams) reduce misalignment.
- Machine-readable maps create repeatability and make handoffs clean.
- Visuals speed up executive comprehension without exposing IP.
