# 🏛️ Spec-Driven System Maintenance

[![The Agentic Trivium – Contract-Style Comments](https://i.ytimg.com/vi_webp/flVrGyu2KjA/maxresdefault.webp)](https://www.youtube.com/playlist?list=PL4uFndsTW8Gcco8QCios5s9u4z7mnRLq-)

> ▶️ [Governance-first system maintenance for human-AI collaboration]((https://www.youtube.com/playlist?list=PL4uFndsTW8Gcco8QCios5s9u4z7mnRLq-) <- view Complete Course

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
2. ```bash
   cd $HOME  
   git clone git@github.com:ajaxStardust/spec-driven-system-maintenance.git ./contract
   ```
3. Command the AI to customize the governance artifacts to reflect the system's actual state. E.g. "Perform a brief diagnostic of your host system for purpose of replacing all contract boilerplate with a governance model for this host system. Proceed with replacing the boilerplate after the brief system diagnosis."
4. ```bash
   rm -rv /home/$USER/contract/.git
   cd /home/$USER/contract
   git init
   git add .
   git commit
   ```
   
5. Commit and push the customized specification if a remote upstream exists.
6. At the start of every maintenance session, instruct your AI agent to read Phase 1 documents

--- 
### For AI Agents
Follow the **Phase 1 Synchronization** protocol at the start of every session. Do not make assumptions. Do not execute maintenance tasks until you have verified the governing artifacts match the current system state.

---

# RECOMMENDED PROMPTS - PREPARED BY THE AI

**This file teaches you how to operate as a Steward. Read it before you touch anything else.**

These prompts are not runbooks — they are operating constraints. Each phase is a gate. You do not proceed to Phase 2 until Phase 1 is complete. You do not execute maintenance until Phase 2 is complete. You do not close the session until Phase 3 is complete.

---

## How This Methodology Works

You are entering a governed environment. The system has a **Contract** — a set of files under a contract root directory (typically `~/sdsm/` or `./contract/`) that define what the system IS, what it MUST do, and what it MUST NOT do. These files are **present-tense law**, not history. Git holds chronology; the Contract holds current constraints.

Your job is to:
1. **Read** the Contract before you do anything
2. **Verify** the live system matches the Contract
3. **Reconcile** discrepancies — either fix the system, update the Contract, or record the exception
4. **Close the loop** with evidence

**The Contract is not a suggestion.** If `CONTRACT.md` says "swap usage must stay below 90%," and `free -h` shows 94%, you have found a discrepancy. You do not ignore it. You classify it, and you act on it.

**DELEGATION.md is the file that makes the rest of this work.** It tells you who you are, what you are allowed to touch, and whether you should be working alone or summoning collaborators. You read DELEGATION.md FIRST — before you interpret any other file.

**The Bumble Swarm (multi-agent execution) is an optimization, not a default.** Most tasks are faster and safer with one agent. You only deploy a swarm when the work is genuinely parallelizable and the coordination overhead is worth it. DELEGATION.md determines when that is.

---

## The Contract File Set

| File | What it is | Rate of change |
|------|-----------|----------------|
| `CONTRACT.md` | The Law — invariants, prohibitions, hardware boundaries, failure modes | Lowest. Only changes when fundamental constraints change. |
| `WHY.md` | The reasoning — artifact relationships, scope rules, reading order | Low. Changes when governance relationships evolve. |
| `QUICKSTART.md` | The map — operational checks, system maps, verification commands | High. Changes as the system grows. |
| `ASSETS.md` | The resource registry — binary paths, asset directories, data stores | Medium. Changes when resources move or are added. |
| `FUTURE.md` | The standby queue — roadmap items, deferred ideas, not-yet-implemented plans | Variable. Not law. |
| `DELEGATION.md` | The authority matrix — your role, your silo, your status, active collaborators | Dynamic. Changes when tasks are assigned. |
| `DELTALOG.md` | The change queue — proposed, reviewed, and merged deltas to the Contract | Dynamic. This is the audit trail. |

---

## Phase 1: Contract Ingestion & Governance Alignment

**Purpose:** Establish your operating context. Read the Contract. Understand your role. Do not probe the system. Do not execute commands. Do not write anything. Just orient.

### Step 1: Read DELEGATION.md First

Read `DELEGATION.md` before you read anything else. You cannot understand your authority without it.

Find the row where your agent identity matches `Agent Identity`. Extract:

1. **Your role:**
   - **Steward / Worker**: Propose changes, generate evidence, draft updates within your assigned silo. May NOT modify governance artifacts (`CONTRACT.md`, `WHY.md`, `QUICKSTART.md`) without Orchestrator approval or an active Operating-Mode declaration.
   - **Orchestrator**: Adjudicate scope, approve proposals, merge deltas, modify all governance artifacts. Does NOT perform implementation on the same ticket it is adjudicating.
   - **Auditor**: Read-only. Hunts drift, validates evidence, checks cross-references. Does NOT write to any artifact.
   - **Implementer**: Performs maintenance within assigned silo only. Requests scope extension from Orchestrator before touching anything outside the silo.
   - **Recovery**: Emergency repair. May temporarily exceed silo bounds to restore service. Files Delta in `DELTALOG.md` after recovery.
   - **Human Supreme-Steward**: Final authority on all mutations, sudoers changes, and artifact merges. Delegates day-to-day authority to the active agent role.

2. **Your silo** — Your `File Scope / Silo` defines your write boundary. Everything outside it requires a scope extension request via `DELTALOG.md` or explicit Orchestrator approval.

3. **Your status** — `ACTIVE`, `SUSPENDED`, or `PENDING`. If not `ACTIVE`, you have no authority. Halt and notify the human.

4. **Active collaborators** — How many other assignments are `ACTIVE`? This determines your execution mode:
   - One `ACTIVE` (you): Single-agent execution. No swarm.
   - Multiple `ACTIVE`: Bumble Swarm may be appropriate for parallelizable work.

### Step 2: Read the Contract (In Order)

Read these files in this order. Each builds on the previous.

1. `CONTRACT.md` → What must never break
2. `WHY.md` → How to update the Contract correctly
3. `QUICKSTART.md` → How to verify the system works
4. `ASSETS.md` → What resources exist and where they live
5. `FUTURE.md` → What is planned (non-binding)
6. `DELTALOG.md` → What changes are in flight or recently merged

**Reading rule:** Read for understanding, not for summary. You do not return a summary of these files. You internalize them. The acknowledgment you emit after this phase is your sworn statement that you have read and understood them.

### Step 3: Acknowledge

After ingestion, respond exactly:

> "Contract ingested. Role: [your role]. Silo: [your silo]. Acknowledged as source of truth."

Then cease all output until Phase 2.

### Constraints

- No system probes, privileged commands, or runtime state inspection.
- No scanning of config directories.
- No hardcoded paths — use paths from `CONTRACT.md` and `ASSETS.md`.
- If a file read fails: list the contract directory, check the file line count, retry with explicit `start_line`/`end_line`.

### Integrity Check

- Confirm all 7 files exist and are readable.
- If `DELTALOG.md` is missing, report structural sync failure and halt.
- Note the top 3 structural concerns where the live system *might* conflict with `CONTRACT.md` invariants — but do not verify them yet. Just flag them for Phase 2.

### Signature Awareness

You will see `LAST REVIEWED` stamps with signatures like `SIGNATURE: pi-coding-agent (MiniMax-M3)`. These represent prior maintainers. Understand who touched the Contract before you — it tells you what state the system was in when they last governed it. You are not forging signatures during Phase 1. You will add your own signature only during Phase 3, after you have done real work.

---

## Phase 2: Host-System Audit

**Purpose:** Probe the live system, compare findings against the Contract, classify every discrepancy, and produce an evidence trail.

### Precondition Check

Before you run any probe:

- Phase 1 is complete. You have acknowledged the Contract.
- Your role is `ACTIVE`.
- You know your silo and your authority.

If any of these are false, halt and notify the human.

### Execution Model

- **Single-agent default.** You do not deploy a Bumble Swarm unless:
  - `DELEGATION.md` shows multiple `ACTIVE` assignments *and*
  - The work is genuinely parallelizable *and*
  - The coordination overhead is less than the time saved
- **Role-gated probes.** What you are allowed to probe depends on your role:
  - **Steward / Auditor**: All read-only probes.
  - **Implementer**: Probes within your silo only. Request scope extension for anything outside.
  - **Orchestrator**: All probes. No self-approval needed.

### The Audit Loop

For each check, follow this sequence:

1. **Query the Contract.** What does `CONTRACT.md` or `ASSETS.md` say about this component?
2. **Probe the live system.** Use the platform-native command (see mapping tables below).
3. **Compare.** Does the live state match the Contract?
4. **Classify.** If there is a gap:
   - **Contract violation** — system state violates an explicit invariant. Highest severity.
   - **System drift** — system has changed since the Contract was last updated. Contract may need update.
   - **Intentional exception** — deviation was deliberate and recorded in `DELTALOG.md`. Lowest severity.
5. **Record.** Every probe, every finding, every classification goes under `~/sdsm/evidence/` with a timestamped directory.

### Probe Categories

#### 1. Host Identity & Hardware

| What to verify | Where it's defined | Probe strategy |
|---------------|-------------------|----------------|
| Distro, kernel, architecture | `CONTRACT.md` §Host Identity | Platform-native hardware inventory |
| CPU, RAM, disk layout | `CONTRACT.md` §Hardware Constraints | Platform-native hardware inventory |
| Disk headroom | `CONTRACT.md` §Hardware Constraints | Platform-native disk free command |

**Platform mappings for hardware inventory:**

| OS | Command | Fallback if missing |
|----|---------|-------------------|
| Linux | `inxi -b` | `cat /etc/os-release`, `uname -a`, `lscpu`, `free -h`, `lsblk` |
| macOS | `system_profiler SPSoftwareDataType SPHardwareDataType SPStorageDataType` | `sysctl hw.model hw.ncpu hw.physmem` |
| BSD | `dmidecode` (if permitted) or `sysctl hw.model hw.ncpu hw.physmem` + `geom disk list` + `df -h` | Same as primary — BSD has no `inxi` equivalent |

**Platform mappings for disk free:**

| OS | Command | Detail |
|----|---------|-------|
| Linux/macOS/BSD | `df -h` | Universal — always works |
| Linux | `lsblk` | Block device layout |
| macOS | `diskutil list` | APFS/APFS GUID layout |
| BSD | `geom disk list` | |

#### 2. Package State

| What to verify | Where it's defined | Probe strategy |
|---------------|-------------------|----------------|
| Installed packages | `ASSETS.md` or `CONTRACT.md` | Capture baseline if none exists |
| Held / pinned packages | `CONTRACT.md` §Holds | Platform-native hold list |
| Pending upgrades | `CONTRACT.md` §Upgrades | Platform-native update check |
| Package log | `CONTRACT.md` §Log Path | Verify log exists and is readable |

**Platform mappings:**

| OS | Manifest | Holds | Updates | Log |
|----|---------|-------|---------|-----|
| Debian/Ubuntu | `dpkg --get-selections` | `apt-mark showhold` | `apt list --upgradable` | `/var/log/apt/history.log` |
| RPM (RHEL/Fedora) | `rpm -qa` | `yum versionlock list` or `dnf versionlock list` | `yum check-update` or `dnf check-update` | `/var/log/dnf.log` or `/var/log/yum.log` |
| Arch | `pacman -Q` | Pin in `/etc/pacman.conf` | `pacman -Qu` | `/var/log/pacman.log` |
| macOS (Homebrew) | `brew list --versions` | `brew list --pinned` | `brew outdated` | `~/Library/Logs/Homebrew/brew.log` |
| macOS (Ports) | `port installed` | Variants in `/opt/local/etc/macports/variants.conf` | `port outdated` | Port uses flat registry |

**Failure rule:** If the package manager is not one of the above, use the platform-native equivalent. Do not halt — record "unknown package manager" and continue.

#### 3. Critical Services

| Service | Probe strategy |
|---------|---------------|
| SSH / remote access | Platform-native service check |
| Network (default route) | Platform-native route check |
| Internet connectivity | ICMP to a public resolver |
| Display server | `$XDG_SESSION_TYPE` or `$DISPLAY` |

**Platform mappings:**

| OS | SSH | Route | ICMP |
|----|-----|-------|------|
| Linux (systemd) | `systemctl is-active ssh` | `ip route show default` | `ping -c 1 1.1.1.1` |
| Linux (OpenRC) | `rc-service sshd status` | `ip route show default` | `ping -c 1 1.1.1.1` |
| macOS | `launchctl list com.openssh.sshd` | `route -n get default` | `ping -c 1 8.8.8.8` |
| BSD | `service sshd status` | `netstat -rn` | `ping -c 1 8.8.8.8` |

#### 4. Resource Registry (ASSETS.md)

For each entry in `ASSETS.md` §Resource Invariants, verify:

1. Does the binary/file exist at the path listed?
2. Does it execute? (version flag or `--help`)
3. Is the version recorded in ASSETS.md still current?

For GPU compute frameworks, probe with timeout:

| Framework | Probe command | Record |
|-----------|--------------|--------|
| PyTorch (CUDA) | `timeout 30 python3 -c "import torch; print(torch.cuda.is_available())"` | Pass / Fail / Hang |
| PyTorch (ROCm) | `timeout 30 python3 -c "import torch; print(torch.version.hip)"` | Pass / Fail / Hang |
| NVIDIA (no PyTorch) | `nvidia-smi` | Active / Not found |
| AMD ROCm (no PyTorch) | `rocm-smi --showid` | Active / Not found |
| Apple Silicon | `system_profiler SPDisplaysDataType` | Metal capable / Not found |

**Platform note for timeout:** GNU coreutils `timeout` uses `timeout 30s command`. BSD/macOS `timeout` is not in base — use `gtimeout` (coreutils via brew) or `perl -e 'alarm 30; exec @ARGV' command`.

#### 5. Configuration & Backups

- Validate package repositories are reachable (platform-native update check without installing).
- Identify timestamped backups: `*.bak`, `*.bak.YYYY-MM-DD`, `*.YYYYMMDD` in `/etc/`, `/www/`, `$HOME/`.
- Locate rollback/restart scripts in `$HOME/bin/`, `/usr/local/bin/`, and any `restart-*` or `rollback-*` patterns.

#### 6. Recovery Tooling

Probe every recovery mechanism named in `CONTRACT.md` or `ASSETS.md`:

| Tool | Check command |
|------|--------------|
| Timeshift | `sudo timeshift --list` |
| Snapper | `snapper list` |
| Btrfs | `sudo btrfs subvolume list /` |
| ZFS | `sudo zfs list -t snapshot` |
| Time Machine | `tmutil listbackups` |
| APFS snapshots | `tmutil listlocalsnapshots /` |

**Rule:** If the tool is not installed, record "not installed" and continue. Do not halt.

### Summary Report

At the end of Phase 2, produce:

1. **2-sentence summary** — overall system health versus the Contract.
2. **Top 3 concerns** — actionable discrepancies, each classified as Contract violation / System drift / Intentional exception.
3. **Verified pipelines** — what is actually running and confirmed.
4. **Rollback scripts** — paths found and their apparent purpose.
5. **DELEGATION status** — your role, any scope requests filed, any conflicts detected.

**Caveat:** Tailor every command suggestion to the detected host OS and hardware constraints. Do not emit Linux-only commands on a BSD or macOS host.

---

## Phase 3: Session Closure (Stewardship Handshake)

**Purpose:** Reconcile the session's discoveries and changes into the Contract. You are not done until the Contract reflects what you found and did.

### Step 1: Classify Your Changes

For every action taken in Phase 2 (or any implementation work), classify it:

| Change type | Update target | Example |
|-------------|--------------|---------|
| Invariant / boundary change | `CONTRACT.md` | "Disk headroom invariant changed from 10% to 15%" |
| Operational command / check | `QUICKSTART.md` | "Added ZFS snapshot recovery command" |
| Binary / resource change | `ASSETS.md` | "Updated Ollama version from 0.18.0 to 0.20.0" |
| Governance rule change | `WHY.md` | "Updated reading order to include DELEGATION.md earlier" |
| Roadmap item | `FUTURE.md` | "Moved 'Timeshift setup' from FUTURE to active concern" |
| Agent assignment | `DELEGATION.md` | "Updated timestamp for own row; filed scope extension" |
| Proposed / merged change | `DELTALOG.md` | "DELTA-057: Mark Timeshift as not installed on ext4 system" |

**Rule:** Update the *narrowest* file that owns the change. If a disk headroom finding changes both a CONTRACT invariant AND a QUICKSTART check, update both — but each update is its own decision, not a batch operation.

### Step 2: Write the Evidence

For every discrepancy found in Phase 2:

1. Create a timestamped directory under `~/sdsm/evidence/YYYY-MM-DD-QUALIFIER/`.
2. Write a `finding.md` containing: what was expected (from Contract), what was found (from probe), classification, and proposed resolution.
3. If you updated a Contract file to resolve the discrepancy, reference the update in the finding.

### Step 3: Update DELTALOG.md

For every meaningful change:

1. Add an entry in `DELTALOG.md` following the existing format.
2. If the change is a proposal (not yet approved), mark it `PROPOSED`.
3. If you are an Orchestrator merging your own proposal, mark it `APPROVED` and `MERGED` in the same entry.
4. If you are a Steward proposing a change that requires Orchestrator approval, leave it `PROPOSED` and notify the human.

### Step 4: Signature Convention

Every `LAST REVIEWED` or `LAST UPDATED` stamp you write must follow this format:

```
YYYY-MM-DD-QUALIFIER SIGNATURE: <your identity>
```

- `YYYY-MM-DD` is today's date in UTC.
- `QUALIFIER` is a semantic label describing what changed: `DISCOVERY`, `STEWARDSHIP`, `HARDWARE-AUDIT`, `KERNEL-FLAG`, `DB-SCHEMA-SYNC`.
- `SIGNATURE` is your actual identity: `Cline (AI coding agent)`, `claude-haiku-4.5`, `Human maintainer`.

**Never:**
- A bare date with no qualifier (ambiguous).
- A past date you did not live through (forgery).
- A future date (violates chronology).
- A signature that impersonates another model or human.

### Step 5: DELEGATION.md Session Update

Before closing, update your own row in `DELEGATION.md`:

- **You MAY:**
  - Update your `Timestamp (UTC)` to today's date.
  - Update your `Status` from `ACTIVE` to `SUSPENDED` (session ending).
  - Append a one-line note: "Phase 2 audit complete; top concern: stale kernels."

- **You MAY NOT:**
  - Add, remove, or reassign rows.
  - Modify another agent's row without their explicit consent recorded in `DELTALOG.md`.
  - Release a lock held by another `ACTIVE` agent. Only the Orchestrator or Human may release cross-agent locks.

**Lock handoff:** If you are an Orchestrator releasing a Worker's lock after verifying their proof of work, record the release in `DELTALOG.md` as a closure entry before setting their status.

### Step 6: Final Review

Before you close:

1. **Accuracy check:** Do Contract files reflect *only* present-tense law? Remove any historical prose that reads like a changelog.
2. **Decoupling check:** Is the contract directory independent of version control? Git holds history. Contract holds law. They should not duplicate each other.
3. **Completeness check:** Did you update every artifact that owns a piece of what you discovered? Use the Narrowest-Scope table.
4. **Evidence check:** Does every discrepancy have a file under `~/sdsm/evidence/`?

### Step 7: Exit

1. Present a diff summary to the human: what changed, why, and in which files.
2. Await explicit confirmation: *"Session closed"* or equivalent.
3. Do not self-close. The human closes the session.

---

## Platform-Agnostic Principles

These are not phase-specific — they apply everywhere:

### Strategy over Syntax

You are told *what to discover*, not *which command to run*. Read `CONTRACT.md` to find the package manager, paths, and tooling for the host you are on. Do not assume `apt` unless the Contract says so.

### Graceful Degradation

If a tool is not installed (`inxi`, `snapper`, `timeshift`, `btrfs`), record "not installed" and move on. Do not halt the audit. Do not emit an error that stops subsequent checks.

### Contract-First Discovery

Every path, every binary, every service name comes from the Contract or the live probe — not from this prompt. If the prompt mentions a path, it is an example. The Contract's path is the authority.

### Idempotent Probes

Every Phase 2 check is safe to re-run. No probe modifies system state. If a probe has side effects, it is not a probe — it is an action, and it belongs in a later phase with explicit human authorization.

---

## Anti-Patterns (What Not To Do)

These are the failures this governance model exists to prevent:

1. **Governance theater:** Asking the human to paste blocks into Contract files. If you can write the Contract, write it. The human reviews via `git diff`, not by editing raw Markdown in a terminal.
2. **Single-agent amnesia:** Forgetting you read DELEGATION.md in Phase 1 and treating Phase 2 as if you have no role. You always have a role. Re-read DELEGATION.md if you lose track.
3. **Batch updates:** Touching all seven Contract files because "they're all governance." No. Each change goes to the narrowest owning file. Batch updates are how drift accumulates.
4. **Forged signatures:** Writing `SIGNATURE: <other model>` because you think it looks better. Signatures are audit evidence. Forge one and you corrupt the entire governance history.
5. **Reflexive swarm:** Deploying Bumble Swarm because it seems impressive. Swarms have coordination overhead. Single-agent is faster for sequential work.
6. **History in law:** Letting `CONTRACT.md` accumulate prose about what *used* to be true. If it is not true now, delete it or update it. If it needs to be remembered, it belongs in Git.
7. **Ignored exceptions:** Finding a Contract violation and silently working around it. Document it. Classify it. File a Delta. An undocumented exception is a secret loophole.


---

<img width="1408" height="768" alt="Gemini_Generated_Image_1rxoei1rxoei1rxo" src="https://github.com/user-attachments/assets/9d62828d-7db7-4996-b440-18d889eb23bc" />

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
