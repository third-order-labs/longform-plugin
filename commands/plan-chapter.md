---
description: Plan a chapter before drafting — load whatever context exists, discuss direction with the user, and build an outline to write against
argument-hint: "<chapter number, title, or 'next'>"
---

# /plan-chapter — Pre-Draft Chapter Planning

Plan a chapter before drafting. Load whatever context the project currently has, discuss direction with the user, and produce an outline spec. The depth of the outline scales with the project — a chapter 2 outline with minimal tracking docs looks different from a chapter 20 outline with a full suite of living documents.

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
- `narrative-craft` — thread health, foreshadowing awareness
- `scene-craft` — lived-in targets, texture planning

## Workflow

### Step 1: Identify the Chapter

Determine which chapter to plan:

- If the user specifies a chapter number or title, use that
- If "next" or no argument, determine the next unplanned chapter by checking existing outlines and drafts
- If a scene log exists, check it for the last completed chapter
- Confirm with the user: "Planning chapter [Y] — correct?"

Determine the book/volume (check which `outlines/book-X/` and `draft/book-X/` directories exist and contain work).

### Step 2: Load What Exists

Read whatever context documents the project currently has. Not all of these will exist — use what's there.

**Always exists:**
- `docs/07-continuity.md` — current canon; the outline must not set up contradictions
- `docs/03-characters.md` — who's in the story, arc directions
- `docs/00-pitch.md` — what the story is about

**Read if present:**
- `docs/06-scene-log.md` — last 2-3 entries for immediate context: where are we, what just happened, what's dangling
- `docs/04-outline.md` — what the structural plan says should happen around this chapter
- `docs/13-threads.md` — which threads are active, which need oxygen
- `docs/19-foreshadowing-checklist.md` — any seeds that need planting in this window
- `docs/25-style-guide.md` — prose targets and constraints
- `docs/08-voice.md` — authorial consciousness and POV character profiles
- `docs/05-glossary.md` — established names and terms
- Any other project-specific reference docs (world, timeline, relationships, etc.)

**Check `AGENTS.md`** for project defaults and the active documents list.

### Step 3: Assess What You Know

Before discussing direction with the user, take stock of what context you have and what you don't. This shapes the conversation.

**If tracking docs exist**, run health checks against them:

- **Thread tracker**: Any thread that hasn't appeared in the last 4 chapters is approaching staleness. Note which stale threads could naturally fit in this chapter. Report to the user: "These threads haven't appeared recently — [list]. Any of them fit here?"
- **Foreshadowing**: Any seeds with approaching payoff targets that haven't been planted. Seeds needing reinforcement. Report what's due.
- **Scene log**: What loose threads from recent entries are still unresolved?

**If tracking docs don't exist**, use continuity and previous drafts to build awareness. Read the last 2-3 drafted chapters if no scene log exists. Note subplots and character threads you're tracking mentally — this is the information that would be in a thread tracker if one existed.

If you're mentally tracking enough threads that it feels fragile (more than you can confidently keep straight), note that in the report at the end — it's a signal that a thread tracker might be worth proposing at the next `/wrap`.

### Step 4: Discuss with the User

Ask the user about this chapter. Adapt the conversation to where they are in the process:

**Early chapters (1-5):** The user is still finding the story. Ask broader questions:
- "What do you want to establish in this chapter?"
- "How should this open? Where are we, who are we with?"
- "What should change by the end of this chapter?"

**Mid-chapters (6+):** The story has momentum. Ask more specific questions informed by context:
- "What needs to happen in this chapter?" — events, turns, reveals
- "Any characters who need to appear?"
- If thread/foreshadowing checks surfaced needs: "Thread X hasn't appeared in a while — does it belong here?"
- If the outline exists and has a beat for this section: "The outline suggests [beat] around here — still tracking with that, or has the story moved?"

**In all cases:** The user provides direction, the agent structures it. If the user says "you decide based on the outline," use the outline and whatever thread/foreshadowing context is available to determine content.

### Step 5: Generate the Chapter Outline

Build the outline. The format should be consistent across the project — if a previous outline exists, match its structure. If this is the first outline, establish the pattern.

Core outline structure:

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
- Supporting-character motive to surface: [which character, what motive]

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
```

**Add sections based on what tracking exists in the project:**

If thread tracker exists:
```markdown
## Thread appearances
- [Thread name]: [I/D/P/S — what happens with this thread]
```

If foreshadowing tracker exists:
```markdown
## Foreshadowing
- [Seed being planted or reinforced]
```

If glossary exists:
```markdown
## Continuity notes
- Names/terms to watch: [known terms relevant to this chapter]
- Likely new terms: [names/terms expected to be invented during drafting]
```

### Step 6: Save the Outline

Save to `outlines/book-X/NN-chapter-title.md` (e.g., `outlines/book-one/12-the-crossing.md`).

### Step 7: Report

Summarize:
- What the chapter covers
- Which threads get oxygen (if tracking)
- Which foreshadowing seeds are addressed (if tracking)
- Any continuity concerns to watch during drafting
- Any observations about project complexity that might warrant new infrastructure (don't propose here — note for `/wrap`)
- Suggest: "Run `/write-chapter` when you're ready to draft from this outline."

## Notes

- The outline is a **spec**, not a straitjacket. The agent should follow it during drafting but can adjust details if the scene demands it. Major deviations from the outline should be noted.
- If the user wants to plan multiple chapters at once (e.g., "plan the next 3"), repeat the process for each, noting how they connect.
- Early in a project, outlines will be simpler — fewer tracking sections, more open questions. That's correct. The outline format grows with the project's infrastructure.
- If no outline template exists yet (`docs/09-chapter-outline-template.md`), the first outline establishes the pattern. After a few chapters, if the user likes the format, suggest saving it as a template for consistency.
