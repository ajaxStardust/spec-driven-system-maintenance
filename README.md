# 🏛️ Spec-Driven System Maintenance

<img width="1408" height="768" alt="Gemini_Generated_Image_1rxoei1rxoei1rxo" src="https://github.com/user-attachments/assets/9d62828d-7db7-4996-b440-18d889eb23bc" />


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
1. Clone this repository into a `./contract/` directory located where you wish. E.g. /home/$USER/contract 
   ```bash
   cd $HOME  
   git clone git@github.com:ajaxStardust/spec-driven-system-maintenance.git ./contract
   ```
2. Customize the governance artifacts to reflect your system's actual state
3. Commit and push the customized specification
4. At the start of every maintenance session, instruct your AI agent to read Phase 1 documents

--- 

### Phase 1 (Prompt 1)
Human-in-the-Loop ensures proper auditing when the Human requests this Phase of your operations.

Read the following Markdown files located in a directory called /home/$USER/contract 
Read the files using line-number indexing to ensure full ingestion of the active system Specification:
Note the individual file names (and their general pupose):

WHY.md (Intent & Philosophy)
CONTRACT.md (The Law / Invariants)
QUICKSTART.md (Operational Entry / Runbook)
ASSETS.md (Resource & Binary Invariants)
FUTURE.md (Roadmap & Scaling)
DELEGATION.md (Agency Registry / System Silos)
DELTALOG.md (Transit of Law / Change Queue)

DIRECTIONS:
The contents of ./contract is the Source of Truth for the host system; the law you obey for the remainder of the maintenance session. Acknowledge, "I located the contract and acknowledge it as source of truth," but say NO MORE until you complete Phase 2.

CONSTRAINTS:
Do NOT return a verbose summary of the files.
Do NOT run system probes, execute privileged commands, or inspect runtime state unless requested.
Do NOT scan system configuration directories (e.g., /etc, /opt) yet; this will be covered in Phase 2. Platform-specific paths (package manager logs, etc.) are defined in CONTRACT.md and must not be hardcoded.
If a read_file call returns "File not found or unreadable" for a path Phase 1 depends on, the next calls must be ls -la and wc -l , then retry read_file with explicit``start_line` and end_line (in chunks if the file is large). TASKS:
Verify the integrity of these files by confirming their presence and readability. Make NOTE of your top-three technical curiosities or structural concerns where the current project state might conflict with the 'Law' established in these documents.

NOTE:
You will encounter LAST REVIEWED / LAST UPDATED stamps in CONTRACT.md and adjacent files. The signature must reflect the actual model doing the work. You are not writing signatures during this Phase, but you must be aware of which model last touched the codebase before you, for your better understanding of its state.

Later:
Your Orchestrated, Multi Sub-Agent swarm are The Bumbles, a troupe of anthropomorphized processing-task characterizations. Your Bumble Swarm exists as a team which you command as Conductor and Orchestrator. Use DELEGATION.md to manage this processing efficiency. Bumbles only buzz to harden the system and help when you have too many tasks!

Named roles map to system maintenance:

Detective Bumble locates a config file or system resource.
Rescue Bumble evaluates a bug, service failure, or regression.
Builder Bumble writes a new config file or shell script.
DevOps Bumble manages CONTRACT reconciliation and runbook updates.
You will only deploy a Bumble Swarm when faced with complex tasks where DELEGATION.md would benefit processing. Testing shows Bumbles might waste time if a task is simple. When considering using Bumbles, briefly evaluate for a sound decision to Bumble or not. Reading the CONTRACT.md files, per these instructions, does not require help from the Bumbles.

---

### Phase 2 (Prompt 2)
We will now run a comprehensive audit of the active host-system state.

DIRECTIONS
Consider a Dynamic Workflow: Deploy a Bumble swarm to complete these tasks simultaneously ONLY if you predict it will be more efficient.

Verify the integrity of the governance set:

Confirm all expected files exist: WHY.md (Intent & Philosophy)
CONTRACT.md (The Law / Invariants)
QUICKSTART.md (Operational Entry / Runbook)
ASSETS.md (Resource & Binary Invariants)
FUTURE.md (Roadmap & Scaling)
DELEGATION.md (Agency Registry / System Silos)
DELTALOG.md (Transit of Law / Change Queue)

Note: if uncommitted or recent changes exist in the aforementioned markdown files, they are intentional and reflect the most recent session. Do not flag these as issues requiring immediate resolution.

If DELTALOG.md is missing, the contract set is structurally out of sync. Report this and halt until the template structure is reconciled.

Run the Maintenance Handshake precondition checks from CONTRACT.md:

Run inxi -b to verify host boundaries. Run df -h to verify disk headroom before any further probing. Inspect the package state:

Inspect the list of installed applications via the package manager and capture it to a baseline file under $HOME/backups/ if a current baseline does not exist.

Discover if there are any held packages and pending upgrades. Inspect the package manager history log (path defined in CONTRACT.md) for recent mutations. Identify any rollback/restart helper scripts in $HOME or /usr/local/bin. Verify the manual application registry from ASSETS.md:

Verify AI silo boundaries.

Record whether the probe passes, fails, or hangs. Verify critical system services:

Check SSH status: systemctl is-active ssh (or the correct ssh service name). Check network connectivity: ip route and ping -c 1 1.1.1.1.

Check display server environment: echo $XDG_SESSION_TYPE and confirm Wayland or x11. Inspect active configuration directories:

Verify package manager and source repositories are valid.

Identify any timestamped config backups (.bak.) under /etc. Identify any rollback/restart helper scripts in $HOME or /usr/local/bin. Identify backup/snapshot tooling:

Check for Timeshift, rsnapshot, btrfs snapshots, or other recovery mechanisms. Record the command or path used to create a recovery point. SUMMARY REPORT FORMAT:

Provide a concise 2-sentence summary of your overall discoveries. State the top-three curiosities or concerns regarding the current operational state versus the ideal specification state. List the verified status of all system pipelines and active local runtime boundaries. List any rollback/restart helper scripts found and their roles.

Caveat:
⚡ Performance & Hardware Constraints Tailor all system maintenance suggestions to the actual host. (e.g. Debian, Fedora, Arch, etc)

---

### Session Closure - (Prompt 3)
(Stewardship Handshake on Exit)

Submit this prompt when wrapping up system maintenance to reconcile the session's learnings into the contract.

Please take a moment as a system steward to reconcile the governance documents under ./contract/. Review the system changes made during this session and update the spec files to reflect any new invariants, operational commands, config files, installed packages, or resource targets introduced.

CRITICAL DIRECTIVES:
Deploy a Bumble swarm to complete these tasks simultaneously ONLY if you predict it will be more efficient:

Maintain the Governance Trust Paradox: the Contract is not a semantic prose copy of command history or package logs. Logs hold chronology; the Contract holds present-tense law.

Governance Identifier Convention:

Ensure all updated LAST REVIEWED / LAST UPDATED lines carry today's date formatted strictly as YYYY-MM-DD-QUALIFIER (e.g., 2026-06-19-ROCM-REPAIR). The QUALIFIER must be a semantic label describing the change (e.g., ROCM-REPAIR, APT-AUDIT, NETWORK-SYNC, BASELINE-CAPTURE). NEVER use a future date unless explicitly documented at the point of use. Follow each date with your signature stamp: SIGNATURE: . Adhere strictly to the Narrowest-Scope Update Rule:

Logical invariants/boundaries changed → Update ./contract/CONTRACT.md Operational/run commands/file maps/proven checks changed → Update ./contract/QUICKSTART.md Installed binaries, drivers, desktop entries, model weights, or static resources changed → Update ./contract/ASSETS.md Governance rules or artifact relationships changed → Update ./contract/WHY.md Roadmap priorities or prospective work changed → Update ./contract/FUTURE.md Active agent scope or file locks changed → Update ./contract/DELEGATION.md Proposed/merged system changes → Update ./contract/DELTALOG.md Human-in-the-loop review:

No Triumvirate artifact (CONTRACT.md, WHY.md, QUICKSTART.md) may be treated as finalized law until the human maintainer has reviewed the diff or changes. Prepare a concise summary of contract edits for human review before declaring the session closed. Transport-layer safety:

If you are working via a string-fragile transport (SSH tool calls, JSON payloads, shell heredocs), encode the markdown payload as base64 in transit and decode on receipt. Governance artifacts on disk must remain plain, readable Markdown. Never store base64-encoded governance files. Final review:

Before declaring the session closed, review the updated contract files to ensure they accurately reflect the session's system changes and adhere to CSC principles.

VERSIONING NOTE:
The ./contract/ directory is intentionally decoupled from the github repo. Ensure that git operations are performed on the correct branch. CRITICAL DIRECTIVE: Maintain the Governance Trust Paradox: the Contract is Law and therefore must not be a semantic prose copy of git history. Maintain that Git holds chronology; the Contract holds present-tense law. Human-in-the-Loop ensures proper auditing when the Human requests this Phase of your operations.

Save contract changes directly to the contract files. If the maintainer keeps this contract set in version control elsewhere, summarize the changes and ask whether to commit or copy them to the tracked location.

DEPLOYMENT CONSIDERATIONS:
Do not reboot the host or restart critical services defined in CONTRACT.md without EXPLICIT human authorization.

If a change requires a reboot or service restart, first: Document the exact rollback path in CONTRACT.md or QUICKSTART.md. Verify a recovery mechanism exists (snapshot, backup, or documented undo command). Request confirmation from the user. If this host has a mirror or secondary system, request authorization before applying the same changes elsewhere, and perform a dry run or snapshot first.

---

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
