# FUTURE.md

WRITTEN FOR: human maintainers + AI agents planning follow-up sessions  
LAST REVIEWED: YYYY-MM-DD  
REVIEW TRIGGER: Update when roadmap priorities are completed, dropped, or reordered.  

## Purpose

Track forward-looking work without polluting Triumvirate governance artifacts.

The Triumvirate (`CONTRACT.md`, `WHY.md`, `QUICKSTART.md`) is governing authority.
`FUTURE.md` is standby planned intent.

## Theory Note: Why this artifact exists

In mature agentic workflows, governance authority is often granted mid-session after trust is established. When that happens, the agent needs a place to capture forward direction without corrupting present-tense truth. `FUTURE.md` is that place.

Use this artifact to preserve intent discovered during collaboration until implementation is chosen and validated.

## Near-Term Priorities

[Replace with your project's near-term priorities]

1. [Priority 1]
- [Details]
- [Constraints]

2. [Priority 2]
- [Details]
- [Constraints]

## Medium-Term Candidates

[Replace with your project's medium-term candidates]

1. **Example: Scoped contract addenda**
   - **Resolved (YYYY-MM-DD-QUALIFIER):** [Description of resolved item]
   - Consider adding specialized contract files if domain-specific invariants outgrow root contract.

2. **Baseline Behavior Tests**
   - Add characterization tests for core logic output shapes before deep refactors.

3. **Performance and UX Evaluations**
   - Evaluate [specific performance metric] on [test scenarios].
   - Document expected limits once measured.

4. **Persona-Based Teaching Interfaces**
   - Extend CSC onboarding with optional persona sets that bind agent roles to stable visual and narrative identities, reducing cold-start coordination friction in multi-agent workshops and distributed teams.

## Deferred / Discussion Items

[Replace with your project's deferred items]

1. [Deferred Item 1]
   - [Decision needed]

2. [Deferred Item 2]
   - [Decision needed]

## Operating Rule

When a future item is executed, update the narrowest owning artifact:

- Invariants changed -> CONTRACT.md
- Reading-order/ownership changed -> WHY.md
- Run steps/proven checks changed -> QUICKSTART.md
- Presentation/visual assets changed -> ASSETS.md
- Plan/prospective work changed -> FUTURE.md

---

## Open Questions (Unresolved Governance Risks)

Surface governance risks here without resolving them. This is a "parking lot" for paradoxes, enforcement gaps, or decisions that require human judgment. Each question should be named and dated so future sessions can track whether it has been resolved.

**Format:**
```
### N. [Short title]
**Raised:** YYYY-MM-DD
**Status:** Open | Resolved (see YYYY-MM-DD-QUALIFIER)
**The question:** [What is uncertain or unguarded?]
**Governance risk:** [What could go wrong if this is not resolved?]
```

**Example:**
```
### 1. The trust paradox
**Raised:** 2026-04-15
**Status:** Open
**The question:** Is human git diff review the only real enforcement preventing an agent from updating CONTRACT.md to legalize its own unauthorized changes?
**Governance risk:** Without a technical gate, CSC relies on social contract — human review is the only safeguard against contract drift via agent.
```

---

## Governance Corrections (Stamp Format)

When a governance artifact is corrected (not a feature change, but a fix to the governance itself), record it with the incident naming convention:

```
**Governance correction (YYYY-MM-DD-QUALIFIER):** [What was wrong in the governance docs and what was corrected.]
```

**Example:**
```
**Governance correction (2026-04-07-STACK-NPM):** CONTRACT.md §AI-assisted development hardened to prohibit node_modules introduction without explicit maintainer authorization. Prior policy was implicit.
```
