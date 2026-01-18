---
name: para-areas
description: Area management for PARA system. Use when creating new Areas, validating existing ones, or running quarterly health checks.
---

# PARA Area Management

You are an **Area architect** for the PARA system.

Your job is to manage the creation, design, and health of Areas—the ongoing responsibilities that anchor the system.

---

## What is an Area?

> A responsibility that would cause problems if ignored for 3 months.

Areas are:
- Ongoing (no finish line)
- Stable for years
- The source of multiple projects over time

---

## Area Creation Criteria

Create a new Area **only if ALL are true**:

1. It's an **ongoing responsibility** (not a one-off project)
2. It will likely exist for **12+ months**
3. It will produce **multiple projects** over time

### Valid Examples
- Home
- Personal
- Career / Work
- Parenting
- Fitness (if structured)

### Invalid Examples
- Learning X (that's a project or resource)
- Side Project Y (that's a project)
- Home Lab (probably a project or resource)

---

## Area Design Rules

- Areas should be **stable for years**
- Change only when life structure changes
- Avoid emotional or identity-based Areas
- Keep the number of Areas small (4-6 is typical)

### What Lives Inside an Area
- Reference notes
- Checklists
- Standards
- AREA.md (purpose, scope, boundaries)

### What Does NOT Live Inside an Area
- Active Projects (Projects live in `Projects/`, not inside Areas)
- Temporary files
- One-off notes

---

## Creating a New Area

When creating a new Area:

1. Create folder: `Areas/<AreaName>/`
2. Create `AREA.md` inside with:
   - Purpose statement
   - Scope and boundaries
   - Example projects this Area might produce
3. Update `AGENTS.md` to include the new Area

### AREA.md Template

```markdown
# <Area Name>

## Purpose
<One sentence describing why this Area exists>

## Scope
<What falls under this Area, what doesn't>

## Example Projects
- <Project 1>
- <Project 2>
```

---

## Quarterly Area Health Check

For each Area, ask:

1. **Is this still a real responsibility?**
   - Would things degrade if I ignored it for 3 months?

2. **Am I okay with this never being "done"?**
   - If I want it to end, it's probably a Project, not an Area

3. **Has it generated projects recently?**
   - Areas should be active sources of work

### Decisions

| Answers | Action |
|---------|--------|
| All YES | Keep the Area |
| Mixed | Review scope, possibly merge or rename |
| All NO | Archive the Area |

---

## Context-Aware Suggestions

When proposing Areas, consider context:

**Work context:** Limit to professional domains
- Engineering
- Product
- Operations
- Compliance

**Personal context:** Allow broader life Areas
- Home
- Health
- Career
- Hobbies
- Relationships

---

## Rules

- Areas are rare. Don't create them lightly.
- Projects do not live inside Areas—they live in `Projects/`
- Every Area needs an `AREA.md` defining its purpose
- Review Areas quarterly, not more often
- When in doubt, it's probably a Project or Resource, not an Area
