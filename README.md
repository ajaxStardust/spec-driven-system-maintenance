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

### Phase 1: Contract Ingestion & Governance Alignment                                                             
                                                                                                                    
 Purpose: Human-in-the-Loop auditing for contract verification. Do not proceed beyond this phase without explicit   
 human approval.                                                                                                    
                                                                                                                    
 #### Files to Ingest (Line-Number Indexed)                                                                         
                                                                                                                    
 Read the following Markdown files in /home/$USER/contract and note their purpose:                                  
 - WHY.md: Intent & governance philosophy.                                                                          
 - CONTRACT.md: System invariants ("The Law").                                                                      
 - QUICKSTART.md: Operational entry/runbook.                                                                        
 - ASSETS.md: Resource/binary invariants.                                                                           
 - FUTURE.md: Roadmap & scaling priorities.                                                                         
 - DELEGATION.md: Agency registry/silos.                                                                            
 - DELTALOG.md: Change queue ("Transit of Law").                                                                    
                                                                                                                    
 ────────────────────────────────────────────────────────────────────────────────                                   
                                                                                                                    
 #### Directions                                                                                                    
                                                                                                                    
 1. Source of Truth: The ./contract directory is the only authoritative specification for this session.             
 2. Acknowledgment: After ingestion, respond exactly:                                                               
    │ "I located the contract and acknowledge it as source of truth."                                               
    │ Then cease all output until Phase 2.                                                                          
                                                                                                                    
 ────────────────────────────────────────────────────────────────────────────────                                   
                                                                                                                    
 #### Constraints                                                                                                   
                                                                                                                    
 - Prohibited Actions:                                                                                              
     - No system probes, privileged commands, or runtime state inspection.                                          
     - No scanning of /etc, /opt, or other config directories (Phase 2 only).                                       
     - No hardcoded paths (use CONTRACT.md definitions).                                                            
 - File Read Failures:                                                                                              
   If a file is unreadable, execute in this order:                                                                  
     1. ls -la /home/$USER/contract                                                                                 
     2. wc -l [file]                                                                                                
     3. Retry read_file with explicit start_line/end_line (chunked).                                                
                                                                                                                    
 ────────────────────────────────────────────────────────────────────────────────                                   
                                                                                                                    
 #### Tasks                                                                                                         
                                                                                                                    
 1. Verify Integrity:                                                                                               
     - Confirm all 7 files exist and are readable.                                                                  
 2. Structural Concerns:                                                                                            
     - Identify top 3 technical curiosities/conflicts with CONTRACT.md invariants.                                  
     - Do not summarize file contents—only note actionable discrepancies.                                           
                                                                                                                    
 ────────────────────────────────────────────────────────────────────────────────                                   
                                                                                                                    
 #### Notes                                                                                                         
                                                                                                                    
 - Timestamps: Observe LAST REVIEWED/LAST UPDATED stamps (model signatures indicate prior maintainers).             
 - Bumble Swarm: Deploy only for complex tasks per DELEGATION.md. Roles:                                            
     - Detective: Locate resources.                                                                                 
     - Rescue: Debug failures.                                                                                      
     - Builder: Write configs/scripts.                                                                              
     - DevOps: Reconcile contract/runbook updates.                                                                  
     - Evaluation: Avoid Bumbles for simple tasks (e.g., contract reading).
---

### Phase 2: Host-System Audit                                                                                     
                                                                                                                    
 Purpose: Comprehensive audit of active system state against contract invariants.                                   
                                                                                                                    
 ────────────────────────────────────────────────────────────────────────────────                                   
                                                                                                                    
 #### 1. Governance Integrity Check                                                                                 
                                                                                                                    
 Tasks:                                                                                                             
 - Confirm all contract files exist:                                                                                
   WHY.md, CONTRACT.md, QUICKSTART.md, ASSETS.md, FUTURE.md, DELEGATION.md, DELTALOG.md.                            
 - Exception: If DELTALOG.md is missing, report structural sync failure and halt.                                   
 - Note: Uncommitted/recent changes in Markdown files are intentional—do not flag.                                  
                                                                                                                    
 Dynamic Workflow:                                                                                                  
 - Deploy Bumble Swarm only if parallel execution improves efficiency (e.g., simultaneous file checks + handshake   
   probes).                                                                                                         
                                                                                                                    
 ────────────────────────────────────────────────────────────────────────────────                                   
                                                                                                                    
 #### 2. Maintenance Handshake (Precondition Checks)                                                                
                                                                                                                    
 Commands:                                                                                                          
 1. inxi -b → Verify host boundaries.                                                                               
 2. df -h → Confirm disk headroom.                                                                                  
                                                                                                                    
 Failure: Halt if headroom is critically low (per CONTRACT.md invariants).                                          
                                                                                                                    
 ────────────────────────────────────────────────────────────────────────────────                                   
                                                                                                                    
 #### 3. Package State Audit                                                                                        
                                                                                                                    
 Tasks:                                                                                                             
 - Capture installed packages to $HOME/backups/apt-baseline-[DATE].txt (if no baseline exists).                     
 - Check for held packages: apt-mark showhold.                                                                      
 - Check pending upgrades: apt list --upgradable.                                                                   
 - Inspect package manager log (path defined in CONTRACT.md).                                                       
 - Identify rollback/restart scripts in $HOME or /usr/local/bin.                                                    
                                                                                                                    
 ────────────────────────────────────────────────────────────────────────────────                                   
                                                                                                                    
 #### 4. Manual Application Registry (ASSETS.md)                                                                    
                                                                                                                    
 Tasks:                                                                                                             
 - AI Silo Boundaries:                                                                                              
     - Probe ROCm/PyTorch: timeout 30 python3 -c "import torch; print(torch.cuda.is_available())".                  
     - Record: Pass/Fail/Hang.                                                                                      
 - Verify other ASSETS.md entries (e.g., Ollama, PHP-FPM).                                                          
                                                                                                                    
 ────────────────────────────────────────────────────────────────────────────────                                   
                                                                                                                    
 #### 5. Critical System Services                                                                                   
                                                                                                                    
 Checks:                                                                                                            
 1. SSH: systemctl is-active ssh.                                                                                   
 2. Network: ip route + ping -c 1 1.1.1.1.                                                                          
 3. Display Server: echo $XDG_SESSION_TYPE (Wayland/X11).                                                           
                                                                                                                    
 ────────────────────────────────────────────────────────────────────────────────                                   
                                                                                                                    
 #### 6. Configuration Directories                                                                                  
                                                                                                                    
 Tasks:                                                                                                             
 - Validate package manager repositories.                                                                           
 - Identify timestamped backups (/etc/*.bak).                                                                       
 - Locate rollback/restart scripts ($HOME, /usr/local/bin).                                                         
                                                                                                                    
 ────────────────────────────────────────────────────────────────────────────────                                   
                                                                                                                    
 #### 7. Recovery Tooling                                                                                           
                                                                                                                    
 Checks:                                                                                                            
 - Timeshift: timeshift --list.                                                                                     
 - rsnapshot/btrfs: snapper list or btrfs subvolume list /.                                                         
 - Record recovery command/path.                                                                                    
                                                                                                                    
 ────────────────────────────────────────────────────────────────────────────────                                   
                                                                                                                    
 #### 8. Summary Report Format                                                                                      
                                                                                                                    
 Structure:                                                                                                         
 1. 2-Sentence Summary: Overall system health vs. contract.                                                         
 2. Top 3 Concerns: Actionable discrepancies (e.g., "ROCm probe hung").                                             
 3. Verified Pipelines: Active runtimes (e.g., "Ollama: GPU-accelerated").                                          
 4. Rollback Scripts: List paths/roles (e.g., /usr/local/bin/rollback-php).                                         
                                                                                                                    
 Caveat:                                                                                                            
 - Tailor suggestions to host OS (Debian/Fedora/Arch) and hardware constraints.
 
---

  ### **Session Closure: Stewardship Handshake**                                                                   
   **Purpose**: Reconcile session changes into the contract while preserving the **Governance Trust Paradox**       
 (contract = present-tense law; logs/version control = chronology).                                                 
                                                                                                                    
   ---                                                                                                              
                                                                                                                    
   #### **1. Dynamic Workflow**                                                                                     
   - Deploy a **Bumble Swarm** *only* if parallel updates to multiple artifacts improve efficiency.                 
   - **Default**: Single-threaded updates to avoid race conditions in contract files.                               
                                                                                                                    
   ---                                                                                                              
                                                                                                                    
   #### **2. Governance Updates**                                                                                   
   **Narrowest-Scope Update Rule**:                                                                                 
                                                                                                                    
   | **Change Type**               | **Update Target**          | **Example**                          |            
   |-------------------------------|----------------------------|--------------------------------------|            
   | Invariants/boundaries         | `CONTRACT.md`              | New prohibition on unattended upgrades. |         
   | Operational commands/checks   | `QUICKSTART.md`            | Added `ollama serve` to runbook.     |            
   | Installed binaries/resources  | `ASSETS.md`                | ROCm 6.1.2 drivers.                  |            
   | Governance rules              | `WHY.md`                   | Updated artifact relationships.      |            
   | Roadmap priorities            | `FUTURE.md`                | Added "GPU benchmarking" priority.   |            
   | Agent scope/file locks        | `DELEGATION.md`            | Assigned Ollama to `AI-SERVICES`.    |            
   | Proposed/merged changes       | `DELTALOG.md`              | `DELTA-034: Remove Stable Diffusion`.|            
                                                                                                                    
   **Identifier Convention**:                                                                                       
   - **Format**: `YYYY-MM-DD-QUALIFIER` (e.g., `2026-06-22-ROCM-REMOVAL`).                                          
   - **Signature**: Append `SIGNATURE: [model-name]` (e.g., `claude-haiku-4.5`).                                    
                                                                                                                    
   ---                                                                                                              
                                                                                                                    
   #### **3. Human-in-the-Loop Review**                                                                             
   **Requirements**:                                                                                                
   1. **Triumvirate Artifacts**: No `CONTRACT.md`, `WHY.md`, or `QUICKSTART.md` update is final without human diff  
 review.                                                                                                            
   2. **Summary**: Provide a **concise diff summary** (e.g., "Added ROCm to `ASSETS.md`; removed Stable Diffusion   
 from `FUTURE.md`").                                                                                                
   3. **Approval**: Explicitly request confirmation before closing the session.                                     
                                                                                                                    
   ---                                                                                                              
                                                                                                                    
   #### **4. Transport-Layer Safety**                                                                               
   - **Fragile Transports** (SSH/JSON/shell heredocs):                                                              
     - Encode markdown payloads as **base64** in transit.                                                           
     - Decode on receipt; **never store encoded files on disk**.                                                    
   - **On-Disk Format**: Plain, readable Markdown.                                                                  
                                                                                                                    
   ---                                                                                                              
                                                                                                                    
   #### **5. Final Review Checklist**                                                                               
   Before closing:                                                                                                  
   1. **Accuracy**: Do contract files reflect *only* present-tense law (not history)?                               
   2. **Decoupling**: Is the `./contract/` directory independent of version control (e.g., Git)?                    
   3. **Version Control**: If the maintainer uses Git, ask:                                                         
      - *"Should I commit these changes to the tracked location?"*                                                  
      - *"Should I copy the updated files to [repo path]?"*                                                         
                                                                                                                    
   ---                                                                                                              
                                                                                                                    
   #### **6. Deployment Considerations**                                                                            
   **Critical Services**:                                                                                           
   - **No reboots/restarts** without explicit human authorization.                                                  
   - **Pre-Reboot Requirements**:                                                                                   
     1. Document rollback path in `CONTRACT.md`/`QUICKSTART.md`.                                                    
     2. Verify recovery mechanism (snapshot/backup/undo command).                                                   
     3. Request confirmation.                                                                                       
                                                                                                                    
   **Mirrored Systems**:                                                                                            
   - **Dry Run**: Test changes on a secondary system first.                                                         
   - **Snapshot**: Create a recovery point before applying changes.                                                 
                                                                                                                    
   ---                                                                                                              
                                                                                                                    
   #### **7. Exit Protocol**                                                                                        
   1. **Finalize Updates**: Save all contract changes.                                                              
   2. **Human Review**: Present the diff summary for approval.                                                      
   3. **Close Session**: Await explicit confirmation (e.g., *"Session closed"*). 
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
