---
description: Create a detailed chapter outline before drafting — checks threads, foreshadowing, and continuity to build a spec the agent can execute against
argument-hint: "<chapter number, title, or 'next'>"
---

# /plan-chapter — Pre-Draft Chapter Planning

Create a detailed chapter outline before any drafting happens. Ensures the agent has a spec to execute against, with full awareness of continuity state, thread health, and foreshadowing needs.

## Invocation

```
/plan-chapter
/plan-chapter next
/plan-chapter 12
/plan-chapter "The Crossing"
```

## Skills Referenced

- `long-form-methodology` — workflow loop (plan phase)
- `continuity-management` — scene log review, canon awareness
- `narrative-craft` — thread health, foreshadowing needs
- `scene-craft` — lived-in targets, texture planning

## Workflow

### Step 1: Identify the Chapter

Determine which chapter to plan:

- If the user specifies a chapter number or title, use that
- If "next" or no argument, check `docs/06-scene-log.md` for the last completed scene/chapter
- Confirm with the user: "The last drafted chapter was [X]. Planning chapter [Y] — correct?"

Determine the book/volume (check which `outlines/book-X/` and `draft/book-X/` directories exist and contain work).

### Step 2: Load Context

Read the following documents to build situational awareness:

1. **Recent scene log entries** (`docs/06-scene-log.md`) — last 2-3 entries for immediate context: where are we, what just happened, what loose threads are dangling?
2. **Continuity doc** (`docs/07-continuity.md`) — current canon state, especially any recent additions
3. **Outline** (`docs/04-outline.md`) — what the structural plan says should happen around this chapter
4. **Active threads** (`docs/13-threads.md`) — which threads are active, which are approaching staleness
5. **Foreshadowing checklist** (`docs/19-foreshadowing-checklist.md`) — any seeds that need planting in this window
6. **Style guide** (`docs/25-style-guide.md`) — prose targets and constraints

### Step 3: Thread Health Check

Scan `docs/13-threads.md` for stale threads:

- Any thread that hasn't appeared in the last **4 chapters** is flagged as stale
- Report stale threads to the user: "These threads haven't appeared recently and need oxygen: [list]"
- Suggest which stale threads could naturally fit in this chapter

### Step 4: Foreshadowing Check

Scan `docs/19-foreshadowing-checklist.md`:

- Any seeds with payoff targets approaching that haven't been planted yet
- Any seeds that should be reinforced (planted once but need a second touch)
- Report to the user: "These seeds should be considered for this chapter: [list]"

### Step 5: Discuss with the User

Ask the user (broad strokes):

- "What should happen in this chapter?" — the core events, turns, or reveals
- "Any specific scenes or moments you want included?"
- "Any characters who need to appear?"

The user provides direction; the agent structures it. If the user says "you decide based on the outline," use the outline and thread/foreshadowing needs to determine content.

### Step 6: Generate the Chapter Outline

Write the outline using the format from `docs/09-chapter-outline-template.md`:

```markdown
# Chapter [NN]: [Title]

## Chapter summary (3-6 sentences)
[What happens, what changes, why it matters]

## Lived-in targets
- Setting function: [what this place is for day-to-day]
- Texture beats (2-3):
  - [beat 1]
  - [beat 2]
  - [beat 3]
- Supporting-character motive to surface: [fear/debt/pride/kindness-with-cost — which character, what motive]

## Scenes

### Scene 1
- POV: [character]
- Location/time: [where and when]
- Goal: [what the POV character wants in this scene]
- Obstacle: [what prevents easy success]
- Action beats:
  - [beat]
  - [beat]
  - [beat]
- Outcome/turn: [what changes as a result]
- New question raised: [what the reader now wonders]

### Scene 2
[same format]

## Thread appearances
- [Thread name]: [I/D/P/S — what happens with this thread]
- [Thread name]: [I/D/P/S]

## Foreshadowing
- [Seed being planted or reinforced]

## Continuity notes
- Names/terms to add to `docs/05-glossary.md`: [list]
- Facts to add to `docs/07-continuity.md`: [list]
- Expected updates to `docs/13-threads.md`: [list]
```

### Step 7: Write the Outline

Save to `outlines/book-X/NN-chapter-title.md` (e.g., `outlines/book-one/12-the-crossing.md`).

### Step 8: Report

Summarize:
- What the chapter covers
- Which threads get oxygen
- Which foreshadowing seeds are planted
- Any continuity concerns to watch during drafting
- Suggest: "Run `/write-chapter` when you're ready to draft from this outline."

## Notes

- Never draft blind. Every chapter should have an outline before drafting begins.
- The outline is a **spec**, not a straitjacket. The agent should follow it during drafting but can adjust details if the scene demands it. Major deviations from the outline should be noted.
- Thread and foreshadowing checks are not optional — they're what prevents the "forgotten subplot" problem in long-form fiction.
- If the user wants to plan multiple chapters at once (e.g., "plan the next 3"), repeat the process for each, noting how they connect.
