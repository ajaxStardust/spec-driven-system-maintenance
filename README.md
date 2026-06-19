# 🏛️ Spec-Driven System Maintenance

> **Governance-first system maintenance for human-AI collaboration**

## Purpose

**Spec-Driven System Maintenance** (SDSM) is a governance framework that enables stateless AI agents to perform system maintenance tasks with precision, accountability, and full alignment with human intent. It treats documentation as executable law, not as an afterthought.

In system maintenance contexts—where environments are complex, configurations drift, and dependencies age—traditional ad-hoc approaches fail. SDSM provides the control plane that transforms maintenance from reactive fire-fighting into a governed, auditable process.

---

## The Core Philosophy

A maintained system is a **governed system**. Without explicit specifications, AI agents operate on assumptions that may be incorrect, outdated, or contradictory. SDSM establishes:

1. **Invariants as Law**: What must never break, regardless of who performs maintenance
2. **Operational Truth as Map**: How the system actually runs, where components live, and how to verify integrity
3. **Resource Integrity as Contract**: Presentation and binary assets treated with the same rigor as code
4. **Audit Trail as Memory**: Every change recorded, every decision traceable

This is not documentation for humans to read. This is the **control plane** for human-AI maintenance collaboration.

---

## The Governance Architecture

SDSM organizes system knowledge into a **Triumvirate** of governing artifacts, supported by two supplements:

### 1. [CONTRACT.md](CONTRACT.md) — The Law
- **Purpose**: Defines system invariants, architectural boundaries, and absolute prohibitions
- **Maintenance View**: What the system IS and what must NEVER break during maintenance operations
- **Rate of Change**: Lowest — changes only when fundamental system constraints change

### 2. [WHY.md](WHY.md) — The Reasoning
- **Purpose**: Explains the relationship between governing artifacts and governance rules
- **Maintenance View**: How to update system law and operations docs correctly
- **Rate of Change**: Low — changes when governance relationships evolve

### 3. [QUICKSTART.md](QUICKSTART.md) — The Map
- **Purpose**: The empirical interface for operational verification
- **Maintenance View**: How to verify system integrity, where critical components live, and how to prove the system works
- **Rate of Change**: High — changes as the system evolves

### 4. [ASSETS.md](ASSETS.md) — The Resource Law
- **Purpose**: Governs presentation invariants, static assets, binary dependencies, and model weights
- **Maintenance View**: Prevents silent regressions when visual or binary resources change
- **Rate of Change**: Medium — changes when assets are added, removed, or modified

### 5. [FUTURE.md](FUTURE.md) — The Roadmap
- **Purpose**: Non-binding queue for planned maintenance priorities and deferred work
- **Maintenance View**: Captures intent without corrupting present-tense truth
- **Rate of Change**: Variable — changes as priorities shift

---

## Maintenance Workflow

### Phase 1: Synchronization (Cold Start)
At the beginning of every maintenance session, the agent must:

1. Read `CONTRACT.md` — Establish constraints and invariants
2. Read `WHY.md` — Understand governance relationships
3. Read `QUICKSTART.md` — Synchronize with operational reality
4. Read `ASSETS.md` — Check resource boundaries
5. Optionally read `FUTURE.md` — Review planned direction

This prevents **contextual drift** — the condition where an agent makes confident decisions based on incomplete or outdated system knowledge.

### Phase 2: Verification
Run proven checks from `QUICKSTART.md` to ensure the contract remains intact:
- Automated tests
- State verification
- Governance check (documentation reflects code changes)
- Infrastructure integrity (filesystems, packages, services)

### Phase 3: Execution
All maintenance changes follow the **Narrowest-Scope Update Rule**:
- Invariants/boundaries changed → Update `CONTRACT.md`
- Run commands/file maps changed → Update `QUICKSTART.md`
- Visual/binary assets changed → Update `ASSETS.md`
- Governance relationships changed → Update `WHY.md`
- Roadmap priorities changed → Update `FUTURE.md`

### Phase 4: Stewardship (Session Close)
Before ending the session, the agent must:
1. Review all changes against governing artifacts
2. Update the narrowest owning artifact for each scope-affecting change
3. Record decisions in `DELTALOG.md`
4. Commit and push with proper signature

---

## Multi-Agent Maintenance (The Bumble Swarm)

When multiple agents collaborate on system maintenance, SDSM prevents **agent collision** through strict role separation:

| Role | Persona | Responsibility | Scope |
|---|---|---|---|
| **Orchestrator** | Cue | Control plane: adjudicates scope, resolves conflicts, finalizes judgment | Governance artifacts only |
| **Archivist** | Stores-It | Memory keeper: maintains context, records, and governance state | Document updates |
| **Auditor** | Solves-It | Investigator: verifies claims, checks cross-references, hunts drift | Read-only verification |
| **Implementer** | Builder | Executor: performs maintenance within delegated scope | Assigned silo only |
| **Recovery** | Rescues-It | Repair agent: handles incident response and contract repair | Emergency scope |

**Golden Rule**: Workers propose, Orchestrator disposes. No Worker may modify governance artifacts without Orchestrator approval.

---

## The Agentic Handshake

Using SDSM transforms your relationship with AI from "tool user" to "system governor":

1. **Stewardship**: The AI agent is authorized—and expected—to act as a **Governance Steward** during maintenance sessions
2. **Responsibility**: No maintenance change is complete until the corresponding documentation artifact has been updated
3. **Surfacing Axioms**: If the agent discovers an undocumented system assumption, it must immediately surface it in `CONTRACT.md`
4. **Falsifiability**: Every claim must be testable or disprovable by evidence

---

## Quick Start

### For System Owners
1. Clone this repository into a `./contract/` directory at your project root:
   ```bash
   git clone git@github.com:ajaxStardust/spec-driven-system-maintenance.git ./contract
   ```
2. Customize the governance artifacts to reflect your system's actual state
3. Commit and push the customized specification
4. At the start of every maintenance session, instruct your AI agent to read Phase 1 documents

### For AI Agents
Follow the **Phase 1 Synchronization** protocol at the start of every session. Do not make assumptions. Do not execute maintenance tasks until you have verified the governing artifacts match the current system state.

---

## Contributing

This framework evolves through governance itself. To contribute:
1. Open an issue describing the governance gap or improvement
2. Submit a Delta proposal in `DELTALOG.md` format
3. Wait for Orchestrator approval before modifying Triumvirate artifacts

---

## License

This framework is provided for the advancement of human-AI collaboration in system maintenance. Use it to make your systems more maintainable, auditable, and resilient.

---

*Spec-Driven System Maintenance — Because maintained systems deserve governed maintenance.*
