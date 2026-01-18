---
name: extract-memories
description: Extract facts and memories from conversation history and save to the appropriate Area files. Use when the user asks to save memories, extract facts from chat, or update their profile/memories files.
---

# Extract Memories from Conversation

Review the current conversation and extract facts worth remembering, categorizing them by Area and saving to the appropriate files.

## Discovery

### Step 1: Find Vault Root

Read `AGENTS.md` at the workspace root to find the PARA root path. Look for the `PARA root:` field in the System Context section.

If not found, assume the workspace root is the PARA vault.

### Step 2: Discover Areas

List the `Areas/` directory to find all existing Areas. For each Area found:
1. Read `Areas/<AreaName>/AREA.md` to understand its scope
2. Check for existing Profile and Memories files

### Standard File Naming Convention

| File Type | Pattern | Purpose |
|-----------|---------|---------|
| Profile | `Areas/<Area>/<Area>_Profile.md` | Static facts about this Area |
| Memories | `Areas/<Area>/<Area>_Memories.md` | Timestamped events for this Area |

If these files don't exist, create them when needed.

---

## Extraction Workflow

### Step 1: Scan Conversation

Review the conversation for extractable information:

- **Profile facts:** Relatively permanent attributes (preferences, biographical info, specs, ongoing state)
- **Memory events:** Timestamped happenings, decisions, milestones, learnings

### Step 2: Categorize by Area

For each extracted fact, determine which Area it belongs to by reading that Area's `AREA.md` for scope guidance.

If uncertain which Area something belongs to, ask the user.

### Step 3: Distinguish Profile vs Memories

**Profile (static):** Things that *are*—identity, preferences, specs, ongoing state
- Add to `*_Profile.md` files
- Update existing entries if information changed

**Memories (temporal):** Things that *happened*—events, decisions, milestones
- Add to `*_Memories.md` files
- Use date headers: `### Month Day, Year`
- Use the current date if known, otherwise run `date "+%B %-d, %Y"`

### Step 4: Skip Project-Specific Content

Do NOT extract:
- Technical notes specific to a project in the vault (belongs in the project folder)
- Temporary debugging info
- Code snippets or implementation details
- Task lists or todos

DO extract:
- Personal/family updates
- Career milestones and decisions
- Property/home changes
- Technical learnings with lasting value
- Preferences and recurring patterns

### Step 5: Append to Files

1. Read the target file to understand existing format
2. For **Memories**: Append new date section at the end
3. For **Profile**: Add to appropriate section, or update existing entry if outdated
4. Use bullet points for individual facts
5. Keep entries concise but complete

---

## Output Format

After extraction, summarize what was saved. List only Areas that had content added:

```
## Extracted Memories

**<Area 1>:**
- [Summary of what was added]

**<Area 2>:**
- [Summary of what was added]

(No facts extracted for: <Area 3>, <Area 4>)
```

---

## Example

Conversation mentions: "Partner got a new job at a tech company making $95k"

**Action:**
1. Determine which Area this belongs to (likely Personal based on AREA.md scope)
2. Update Profile with partner's career info
3. Add timestamped Memory entry

**Profile update:**
```markdown
## Partner
- **Career:** Tech sales, $95K
```

**Memory entry:**
```markdown
### January 17, 2026

- Partner started new job in tech sales.
```

---

## Rules

- Always read AREA.md files before categorizing
- Don't assume which Areas exist—discover them
- Create Profile/Memories files if they don't exist
- When in doubt about categorization, ask the user
- Never overwrite existing content—append or update in place
