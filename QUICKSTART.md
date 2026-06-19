# QUICKSTART.md — The Map (Operational Truth)

> **"A map is not the territory, but without one, the traveler is lost. In an agentic system, the map is the interface between intent and execution."**

## Purpose of This Artifact

In the **contract-style-comments** (CSC) framework, `QUICKSTART.md` serves as the system's **Empirical Interface**. While `CONTRACT.md` defines the laws (invariants), `QUICKSTART.md` defines the reality—how the system actually runs, where the critical components live, and how to prove that the system is still functioning as intended.

For a stateless AI agent, this file is the "Onboarding Manual" that prevents wasteful exploration and ensures every change is verified against a known-good baseline.

---

## Required Reading Order (The Synchronization)

To prevent "Contextual Drift" and ensure the agent understands the system's operational boundaries, this sequence is mandatory at the start of every session:

1.  **[CONTRACT.md](CONTRACT.md)**: Internalize the laws and invariants.
2.  **[WHY.md](WHY.md)**: Understand the governance and pedagogy.
3.  **[QUICKSTART.md](QUICKSTART.md)**: Synchronize with the operational map and verification steps.
4.  **[FUTURE.md](FUTURE.md)**: Optionally review roadmap intent after operational synchronization (standby, non-binding).

---

## STAGING URL and LIVE HTTP URL

Primary Entry Point:
 - LIVE: [Your production URL]
 - STAGING: [Your staging URL]

Secondary Entry Point:
 [If applicable]

---

## The System Map (Key Components)

*Modify this table to reflect the specific architecture of your project.*

| Area | Canonical File(s) | Role / System Interaction |
|---|---|---|
| **Entry Point** | [main file] | The primary bootstrap for the system state. |
| **Core Logic** | [core directory] | Where the core transformations and invariants are implemented. |
| **Configuration** | [config files] | The persistent state that the system must respect. |
| **Interface** | [API/CLI directory] | The boundary through which the system interacts with external agents. |

---

## Proven Checks (Verification Loop)

A system is only as reliable as its verification process. Every session must conclude with a "Proven Check" to ensure the `CONTRACT.md` remains intact.

1.  **Automated Tests**: Run [test command] and verify 100% pass rate.
2.  **State Verification**: Verify that a specific input (e.g., `X`) results in the expected output (e.g., `Y`) without violating any invariants.
3.  **Governance Check**: Ensure that if a scope-affecting change was made, the matching documentation artifact has been updated.

### Falsifiability Checklist (apply to critical claims)

For each high-impact contract statement, define:

1. **Claim**: the exact invariant/precondition/postcondition being asserted.
2. **Counterexample**: what evidence would prove the claim false.
3. **Check Method**: how to test it (test case, `curl` probe, linter/static check, runtime assertion).
4. **Owner Artifact**: where the claim is governed (`CONTRACT.md`) and where checks are runbooked (`QUICKSTART.md`).

**Concrete Example:**
```
Claim: [Your critical invariant]
Counterexample: [What would disprove it]
Check: [Command or method to verify]
Owner: CONTRACT.md §[section]; QUICKSTART.md (this section).
```

### First-Party Verification Preference

Before asking humans for browser screenshots or DevTools dumps, run first-party checks when possible (`curl`, endpoint probes, reproducible shell commands, code-path inspection). Ask for human-captured evidence only when the required signal is browser-only or account-specific.

---

## The Narrowest-Scope Rule (Operational)

In the CSC framework, this file owns **operational truth**.

- **Update this file** when a file is moved, a new script is added, or a new verification step is discovered.
- **Do NOT update this file** for architectural changes or laws—those belong in `CONTRACT.md`.
- **Do NOT update this file** for planning-only ideas—those belong in `FUTURE.md`.
- **Instruction**: "If you add a tool, register it in the Key Files table. If you find a new way to break the system, add it to the Proven Checks."

---

## The Agentic Handshake (Proof of Work)

**The Verification Steward**: Within an active user session, the AI agent is authorized to update this map. 

-   **Responsibility**: No code change is considered "Proven" until it has passed the checks listed here.
-   **Drift Prevention**: If an agent discovers that a listed check is obsolete, it is expected to update the check immediately to reflect the new system reality.

---

## Last Reviewed & Trigger

-   **LAST REVIEWED**: YYYY-MM-DD-QUALIFIER SIGNATURE: [Agent or Human Identity]
-   **REVIEW TRIGGER**: Update this file whenever the project structure changes, new tools are introduced, or a more effective verification method is developed.

---

*Part of the `contract-style-comments` framework. For the full architectural manifesto, visit [WhatsOnYourBrain.com](https://whatsonyourbrain.com).*
