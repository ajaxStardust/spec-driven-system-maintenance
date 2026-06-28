# CSC Decision Checklist

**Purpose:** Quick routing guide for humans and AI stewards new to CONTRACT-style governance. This is *not* a replacement for reading the canonical docs—it's a triage tool to help you pick which artifact to read first.

---

## 🚦 When Something Changes: Which File Do I Update?

### 📝 Code/Logic Changes
- **Adding/removing a function?** → Add inline CONTRACT comment in code
- **Changing function behavior?** → Update the inline CONTRACT *and* reference `CONTRACT.md` if it affects system-wide invariants
- **New critical invariant discovered?** → Add to `CONTRACT.md` under appropriate section
- **Removing an invariant?** → Remove from `CONTRACT.md` in same PR

### 🎨 Visual/Asset Changes
- **New image, logo, or binary asset?** → Register in `ASSETS.md` §Resource Invariants
- **Changing CSS/design tokens?** → Update `ASSETS.md` with new rules
- **Modifying page layout?** → Update `ASSETS.md` and reference in inline template comments
- **OGP/social preview changes?** → Update `ASSETS.md` §Social preview

### 🏃 Operational Changes
- **New run command or dependency?** → Update `QUICKSTART.md` §System Map
- **New "proven check" for verification?** → Add to `QUICKSTART.md` §Proven Checks
- **File locations changed?** → Update `QUICKSTART.md` §Key content locations
- **Environment variables added?** → Document in `QUICKSTART.md` §Prerequisites

### 🧭 Architectural Relationships
- **Adding a new governance file?** → Update `WHY.md` §Reading Order *and* §What each file owns
- **Changing document boundaries?** → Update `WHY.md` with new scope rules
- **New tie artifact needed?** → Add to `WHY.md` table with ownership notes

### 🚀 Roadmap/Planning
- **New priority for next sprint?** → Add to `FUTURE.md` §Near-Term Priorities
- **Medium-term idea?** → Add to `FUTURE.md` §Medium-Term Candidates
- **Deferred discussion?** → Add to `FUTURE.md` §Deferred/Discussion Items
- **Completed a FUTURE item?** → Move to appropriate artifact *and* update FUTURE.md

### 🤖 Multi-Agent Sessions
- **Assigning Workers?** → Update `DELEGATION.md` §Current Assignments
- **Scope extension needed?** → File delta in `DELTALOG.md` first
- **Governance change proposed?** → Add to `DELTALOG.md` §Proposal Queue
- **Delta approved?** → Update Triumvirate artifact *and* close delta in DELTALOG.md

---

## 🔍 Common Patterns: Where to Look First

### "I need to add a new web site"
1. Check `CONTRACT.md` §Web Application Registry for URL/port patterns
2. Check `QUICKSTART.md` §System Map for backend framework and port
3. Check `ASSETS.md` if the site has special asset paths or SSL certs
4. Update the narrowest owning artifact when done

### "I found a broken backend"
1. Check `CONTRACT.md` §Web Application Registry for domain → backend mapping
2. Check `/www/wwwroot/<site>/` for the application code and gunicorn config
3. Check `ASSETS.md` if it's a path or dependency issue
4. File fixes with inline CONTRACT comments referencing the governance docs

### "I want to change the control panel"
1. Check `ASSETS.md` §BT-Panel for path and binary constraints
2. Check `CONTRACT.md` §Web Application Registry for any dependent site configs
3. Update `ASSETS.md` if panel paths or managed services change

### "I need to add a new environment check"
1. Check `QUICKSTART.md` §Proven Checks for existing patterns
2. Add new check to `QUICKSTART.md` with clear pass/fail criteria
3. Reference from `CONTRACT.md` if it guards a critical invariant

---

## 📖 Reading Order Cheat Codes

**If you have 2 minutes:**
- Skim `CONTRACT.md` §Host Identity and §Hardware Constraints
- Skim `QUICKSTART.md` §System Map
- Skim `ASSETS.md` §Resource Invariants

**If you have 10 minutes:**
1. Read `CONTRACT.md` §Purpose and §Governance
2. Read `QUICKSTART.md` §Proven Checks
3. Read `ASSETS.md` §Resource Invariants
4. Glance at `FUTURE.md` for context

**If you're editing code:**
1. Read full `CONTRACT.md`
2. Read `WHY.md` for relationships
3. Read relevant section of `QUICKSTART.md` or `ASSETS.md`
4. Update the narrowest owning artifact when done

**If you're in a multi-agent session:**
1. Read `DELEGATION.md` first to avoid collisions
2. Read `DELTALOG.md` for pending changes
3. Follow normal reading order for your scope

---

## 🔄 The Update Loop (TL;DR)

```
CODE CHANGE → IDENTIFY SCOPE → UPDATE NARROWEST ARTIFACT → SIGN WITH DATE+QUALIFIER
          ↓
  Git holds history ← Contract holds present-tense law
```

**Qualifier Examples:**
- `2026-06-22-FEATURED-IMAGE-STANDARDIZATION` (specific)
- `2026-06-22-BLOG-ROUTE-HARDENING` (specific)
- `2026-06-22-STEWARDSHIP` (general)
- `2026-06-22-DB-SCHEMA-SYNC` (specific)

**Never:**
- `2026-06-23` (bare date = ambiguous)
- `2026-06-20` (past date without context)
- `2026-06-25` (future date)

---

## 🚧 When in Doubt

1. **Ask:** "What's the narrowest file that owns this change?"
2. **Check:** Does this affect invariants (`CONTRACT.md`) or presentation (`ASSETS.md`) or operations (`QUICKSTART.md`)?
3. **Update:** That one file (not all three)
4. **Sign:** With today's date + semantic qualifier

---

*This checklist is a **bridge**, not a replacement. Always reconcile with the canonical artifacts in `~/sdsm/` after using this guide.*
