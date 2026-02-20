---
description: Draft a chapter from its outline, then automatically update all living documents — scene log, continuity, glossary, threads, and foreshadowing
argument-hint: "<chapter number, title, or 'next'>"
---

# /write-chapter — Draft a Chapter

The core workflow loop. Draft a chapter from its outline, then automatically update all living documents. This is where manuscript and tracking docs grow together.

## Invocation

```
/write-chapter
/write-chapter next
/write-chapter 12
/write-chapter "The Crossing"
```

## Skills Referenced

- `long-form-methodology` — workflow loop (draft + log phases), document hierarchy
- `continuity-management` — scene log format, canon updates, glossary entries
- `narrative-craft` — thread marking, foreshadowing tracking
- `scene-craft` — lived-in texture, dialogue craft, POV discipline

## Workflow

### Step 1: Load the Chapter Outline

Locate the outline:

- If the user specifies a chapter, find the matching file in `outlines/book-X/`
- If "next" or no argument, find the next unwritten outline (compare outlines to existing draft files)
- If no outline exists, inform the user: "No outline found for this chapter. Run `/plan-chapter` first."

Read the full outline.

### Step 2: Load Context Documents

Read the following to ensure consistency:

1. **Continuity doc** (`docs/07-continuity.md`) — current canon; do not contradict
2. **Recent scene log** (`docs/06-scene-log.md`) — last 2-3 entries for immediate narrative context
3. **Active threads** (`docs/13-threads.md`) — know which threads this chapter should touch (per outline)
4. **Foreshadowing checklist** (`docs/19-foreshadowing-checklist.md`) — seeds to plant per outline
5. **Style guide** (`docs/25-style-guide.md`) — prose register, POV, tense, length targets, lived-in checklist
6. **Glossary** (`docs/05-glossary.md`) — correct names, terms, spellings
7. **Voice doc** (`docs/08-voice.md`) — authorial consciousness and character voice profiles for this chapter's POV character(s)

### Step 3: Draft the Chapter

Write the chapter following:

- The **outline spec**: scenes, goals, obstacles, action beats, outcomes
- The **style guide**: prose register, POV/tense, dialogue approach, lived-in targets
- The **continuity doc**: no contradictions with established canon
- The **glossary**: correct and consistent names/terms
- The **voice doc**: filter scene description through the authorial attention filter, maintain the narrator's stance toward events (from beliefs/iceberg sections), match POV character's interior voice to their profile

Apply the lived-in checklist from `scene-craft`:
- Include 2-3 texture beats (from the outline's lived-in targets, or generate appropriate ones)
- Show the setting's daily function
- Surface at least 1 supporting-character motive per scene
- Apply consequence glue: decisions produce immediate visible effects
- Maintain POV discipline: no head-hopping, interior voice matches the POV character

Target the chapter length specified in the style guide (default: ~1,000-2,500 words unless the user requests otherwise or the style guide specifies differently).

### Step 4: Write the Draft

Save to `draft/book-X/NN-chapter-XX-TITLE.md` (e.g., `draft/book-one/12-chapter-12-The-Crossing.md`).

### Step 5: Automatic Post-Draft Updates

This is mandatory — not optional cleanup. After writing the chapter, immediately update all living documents:

#### 5a. Scene Log Entry → `docs/06-scene-log.md`

Add a new entry with all fields:

```
- Scene ID: [BookN-ChNN]
- Location: [specific place(s)]
- Time: [time of day, relation to prior scene]
- POV: [character name]
- Setting function: [what this place is for day-to-day]
- Texture beats: [the 2-3 texture beats actually used]
- What changes: [state change — what's different after this chapter]
- New facts introduced: [anything that becomes canon]
- Loose threads: [questions raised, things left unresolved]
```

#### 5b. Continuity Updates → `docs/07-continuity.md`

Add any new **canon-level facts** introduced in this chapter:
- New character states, relationships, or revelations
- World-building facts that must be maintained
- Timeline events
- Decisions or commitments that constrain future chapters

Only add facts that would cause a continuity error if contradicted later.

#### 5c. Glossary Updates → `docs/05-glossary.md`

Add any new entries:
- Character names (including aliases)
- Place names
- Terms, titles, organizations
- Magical/cultural/technical vocabulary

Update existing entries if new variants or aliases appeared.

#### 5d. Thread Tracking → `docs/13-threads.md`

For each thread that appeared in this chapter, add the chapter marker:
- **I** if a new thread was introduced
- **D** if an existing thread was developed
- **S** if a foreshadowing seed was planted
- **P** if a thread was paid off

If a new thread emerged during drafting (not in the outline), add it as a new entry.

#### 5e. Foreshadowing Updates → `docs/19-foreshadowing-checklist.md`

- Mark any seeds that were planted in this chapter
- Note the chapter where they were planted
- If new foreshadowing opportunities emerged during drafting, add them with payoff targets

#### 5f. Voice Observations

Note any observations relevant to `docs/08-voice.md`:

- New voice patterns that emerged during drafting
- Any drift from the established authorial consciousness
- Character voice evolution that should be recorded in the character profile
- Moments where the voice felt particularly right or wrong
- Anti-patterns from the voice doc that appeared and needed correction

### Step 6: Report

Summarize what was accomplished:

```
## Draft Complete: Chapter [NN] — [Title]

**Words**: [count]
**Location**: `draft/book-X/NN-chapter-XX-TITLE.md`

### What happened
[2-3 sentence summary of the chapter's events and state changes]

### Documents updated
- Scene log: entry added for [Scene ID]
- Continuity: [N] new facts added ([brief list])
- Glossary: [N] new/updated entries ([brief list])
- Threads: [list of threads touched with markers]
- Foreshadowing: [seeds planted or "none this chapter"]
- Voice: [observations — drift, new patterns, character voice notes, or "consistent"]

### Continuity concerns
[Any potential issues noticed during drafting — contradictions, timeline questions, etc. "None" if clean.]

### Next
[What the outline says comes next, or suggest running /plan-chapter for the next chapter]
```

## Notes

- If the outline calls for something that contradicts the continuity doc, follow the continuity doc and note the deviation from the outline.
- If inspiration during drafting leads to significant departures from the outline, note what changed and why in the report. Update relevant planning docs.
- The post-draft document updates are what make this methodology work at scale. Skipping them creates compounding continuity debt.
- If the agent invents a name, place, or term not in the outline, record it immediately in the glossary and continuity doc (if canon-level). Do not defer this.
- The draft is a working draft, not a polished final. Forward momentum is more valuable than perfection. Style polish comes in revision passes.
