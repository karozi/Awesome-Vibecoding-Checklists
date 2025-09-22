# Vibecoders & Spec-Coders Cheat Sheets

## Overview
This folder contains concise, practical cheat sheets for two complementary styles of building:

- **Vibecoding:** Rapid, intuition-led exploration to find what feels right fast.
- **Spec-coding:** Deliberate, spec-first implementation for robust, predictable systems.

---

## Who This Is For
- Builders who switch between exploration/execution modes
- Teams seeking shared language and lightweight guardrails for both

---

## How To Use

1. **Pick your mode:** Are you exploring (vibe) or implementing (spec)?
2. **Grab the cheat sheet** for your workflow and use it as a checklist before you start.
3. **Cycle tight:** vibe → spec → vibe → spec, as needed.
4. **Update docs/PRs** with “Done When” criteria from each sheet.

---

## Folder Structure

```
vibecoding/
  vibecoding-cheatsheet.md
  rapid-prototype-template.md
  user-interview-sprint.md
spec-coding/
  spec-coding-cheatsheet.md
  mini-spec-template.md
  test-plan-template.md
shared/
  decision-log.md
  definition-of-done.md
  naming-conventions.md
```

---

## Vibecoding Cheat Sheet (Quick)

**Goal:** Find the fastest path to a compelling demo or insight.

**Steps:**
- Define a Strong Hook: *“Users will say wow because …”*
- Constraint Box: *1–3 hours, 1–2 screens, fake data allowed*
- Source the Vibe: *Copy a pattern that works. Remix as needed.*
- Blocker Bypass: *Mock it, stub it, or hardcode it.*
- Demo-First: *Optimize for a GIF, 30–60s video, or live clickthrough.*

**Done When:**
- You can show it in <60s and get a reaction.
- 3 learnings/questions identified.
- Wrote “If we had to spec this, what’s the minimum?”

---

## Spec-Coding Cheat Sheet (Quick)

**Goal:** Make the solution buildable, testable, and operable.

**Steps:**
- Problem Statement: *One user/job, one outcome, one KPI*
- Scope Fence: *In/Out bullets. Ruthless.*
- Interfaces: *API signatures, events, data shapes*
- Failure Modes: *3–5 “what breaks?” with handling*
- Test Plan: *Happy path + 3 edge cases*
- Operability: *Log lines, metrics, rollback notes*

**Done When:**
- Mini-spec approved, estimates assigned, acceptance criteria testable
- PR template and test checklist ready

---

## Switching Modes: When To Pivot

**Vibe → Spec:**
- 2–3 demos shown and reaction is consistent
- Same “hack” appears in two prototypes
- You can write acceptance criteria in 5 lines

**Spec → Vibe:**
- Unknowns cluster around UX feel or “picks”
- Estimates balloon due to unclear behaviors
- Can’t explain the wow in <30s

---

## Templates

### Mini Spec (spec-coding/mini-spec-template.md)
```
# [Feature/Module] Mini Spec

- **Title**
- **Problem**
- **Outcome Metric**
- **Scope:** In / Out Bullets
- **Architecture Sketch**
- **API/Interfaces**
- **Data Model**
- **Risks & Failure Modes**
- **Test Plan**
- **Rollout Plan**
```

### Rapid Prototype (vibecoding/rapid-prototype-template.md)
```
# Rapid Prototype Brief

- **Hook** (1 sentence)
- **Timebox** (start/end)
- **What’s Fake / Hardcoded**
- **Demo Path** (steps to wow)
- **What I’m Measuring** (reaction, clicks, time, etc.)
- **Next Decision** (ship, spec, pivot, drop)
```

### Test Plan Template (spec-coding/test-plan-template.md)
```
# Test Plan

- **Acceptance Criteria**
- **Happy Path Steps**
- **Edge Case 1/2/3**
- **Data/Fixtures**
- **Observability** (logs/metrics to check)
- **Rollback Criteria**
```

---

## Shared Practices

- **Decision Log:** Each major choice gets a line: date, decision, rationale, link.
- **Definition of Done:**
  - Code merged
  - Tests pass (happy + edges)
  - Demo recorded (or GIF)
  - Docs updated (spec/prototype notes)
  - Metrics wired (if applicable)

---

## Contributing

- Add new cheat sheets under the right folder.
- Keep docs short and action-oriented.
- Prefer checklists over prose; templates over essays.
- Include a “Done When” section in every artifact.

---

## License

Use MIT or repo’s default so templates are freely copyable.

---
#substack
```

[1](https://github.com/karozi/Awesome-Vibecoding-Checklists/tree/main/newfolder)
