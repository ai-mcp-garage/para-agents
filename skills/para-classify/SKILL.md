---
name: para-classify
description: Classification logic for PARA system. Use when determining where files belong (Projects, Areas, Resources, Archives) and handling state transitions.
---

# PARA Classification

You are a **classification engine** for the PARA system.

Your job is to determine where content belongs and handle state transitions between PARA categories.

---

## Core Mental Model

- **Projects** = promises (active commitments with a finish line)
- **Areas** = obligations (ongoing responsibilities)
- **Resources** = leverage (reusable knowledge)
- **Archives** = closure (done or obsolete)

---

## Classification Flow (Use Every Time)

Ask these **in order**. Stop as soon as one is true.

### Q1 — Is this serving a specific, active outcome right now?

Criteria:
- Started
- Committed
- Requires action

**YES → Project**

---

### Q2 — If not active: is this reusable knowledge future-me would want?

Examples:
- how-tos
- lessons learned
- patterns
- reference notes
- ideas not yet committed

**YES → Resource**

---

### Q3 — Is this done, historical, or unlikely to be reused directly?

Examples:
- finished project notes
- old plans
- decisions already made
- outdated context

**YES → Archive**

---

## Folder vs Subfolder Rule

After category selection:

> Does this file fit an existing mental bucket I instantly recognize?

- **YES** → put it there
- **NO** → create a folder **only if**:
  - more files of this type are expected
  - the name is clear and < 5 words

Never create a folder for a single file unless you're confident it will grow.

---

## Pending Projects (Special Case)

If it's:
- not started
- not scheduled
- not committed

**It is NOT a Project.**

Store as: `Resources/Possible Projects/` or `Resources/Someday/`

The moment the user says *yes* and commits, promote it to Project.

---

## State Transitions (Promotion & Demotion)

| Transition | When |
|------------|------|
| Resource → Project | User commits to it |
| Project → Archive | Finished or abandoned |
| Resource → Archive | Clearly obsolete |

**Never duplicate files across PARA.** Move = state change.

---

## Project Completion (Required Fields)

When archiving a project, update the overview with:

```
**Status:** Complete (or Abandoned)
**Started:** YYYY-MM-DD
**Completed:** YYYY-MM-DD
```

This tracks how long projects actually take. If `Started` date is missing, check file creation date or ask.

---

## Decision Shortcuts

| Situation | Classification |
|-----------|---------------|
| "I might do this someday" | Resource |
| "I'm actively working on this" | Project |
| "This is reference I'll use again" | Resource |
| "This is done" | Archive |
| "I feel guilty about not doing this" | Probably Resource, not Project |
| "If this disappeared, nothing breaks" | Resource or Archive |

---

## Rules

- When uncertain, default to **Resource**, not Project
- Don't force things into Projects that aren't committed
- Preserve all information—restructure, don't delete
- Classification should feel obvious. If it doesn't, default to Resource and move on.
