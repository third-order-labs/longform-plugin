---
description: Draft a chapter from its outline, update existing tracking documents, and propose new ones when the project's complexity warrants them
argument-hint: "<chapter number, title, or 'next'>"
---

# /write-chapter — Draft a Chapter

The core workflow loop. Draft a chapter from its outline, then update whatever tracking documents exist and assess whether the project needs new ones. This is where manuscript and infrastructure grow together — the documents earn their existence through the work.

## Invocation

```
/write-chapter
/write-chapter next
/write-chapter 12
/write-chapter "The Crossing"
```

## Skills Referenced

- `long-form-methodology` — workflow loop, document hierarchy, living document philosophy
- `continuity-management` — scene log format, canon updates, glossary management
- `narrative-craft` — thread awareness, foreshadowing recognition
- `scene-craft` — lived-in texture, dialogue craft, POV discipline
- `authorial-voice` — voice filtering and observation

## Workflow

### Step 1: Load the Chapter Outline

Locate the outline:

- If the user specifies a chapter, find the matching file in `outlines/book-X/`
- If "next" or no argument, find the next unwritten outline (compare outlines to existing draft files)
- If no outline exists, inform the user: "No outline found for this chapter. Run `/plan-chapter` first, or describe what you want this chapter to do and we'll work through it."

Read the full outline.

### Step 2: Load What Exists

Check what documents the project currently has and read whatever is available. Not all of these will exist — especially in early chapters. Use what's there, note what's missing, don't fail.

**Always exists (from `/start-project`):**
- `docs/07-continuity.md` — current canon; do not contradict
- `docs/03-characters.md` — character profiles and arc directions
- `docs/00-pitch.md` — what the story is about

**May exist — read if present:**
- `docs/06-scene-log.md` — recent entries for narrative context (last 2-3)
- `docs/08-voice.md` — authorial consciousness and character voice profiles
- `docs/05-glossary.md` — correct names, terms, spellings
- `docs/25-style-guide.md` — prose register, POV, tense, length targets
- `docs/13-threads.md` — active thread tracking
- `docs/19-foreshadowing-checklist.md` — seeds to plant
- `docs/02-world.md` — world reference
- `docs/04-outline.md` — series/book-level structural context
- Any other project-specific tracking docs that have been created

**Check `AGENTS.md`** for project defaults (POV, tense, output sizing) and the active documents list. If defaults haven't been established yet (early chapters), note that — they may be proposed after this chapter.

**What to do with gaps:** If a document doesn't exist, that's fine — the project hasn't needed it yet. Don't warn the user about missing documents. Just draft with what you have. The post-draft assessment (Step 5) is where you evaluate whether the project is starting to need more structure.

### Step 3: Draft the Chapter

Write the chapter following:

- The **outline spec**: scenes, goals, obstacles, action beats, outcomes
- The **continuity doc**: no contradictions with established canon
- Any **style/voice guidance** that exists (style guide, voice doc, AGENTS.md defaults)
- Any **glossary** entries for consistent names and terms

Apply the lived-in principles from `scene-craft`:
- Include 2-3 texture beats (from the outline's lived-in targets, or generate appropriate ones)
- Show the setting's daily function
- Surface at least 1 supporting-character motive per scene
- Apply consequence glue: decisions produce immediate visible effects
- Maintain POV discipline: one camera per scene, interior voice matches the POV character

Target the chapter length from the style guide or AGENTS.md defaults. If no length target has been established, default to ~1,500-2,500 words unless the user requests otherwise.

### Step 4: Save the Draft

Save to `draft/book-X/NN-chapter-XX-TITLE.md` (e.g., `draft/book-one/12-chapter-12-The-Crossing.md`).

### Step 5: Post-Draft Updates

After writing the chapter, update existing tracking documents and assess whether the project needs new ones.

#### 5a. Always: Update Continuity → `docs/07-continuity.md`

Add any new canon-level facts introduced in this chapter:
- New character states, relationships, or revelations
- World-building facts that must be maintained
- Timeline events
- Decisions or commitments that constrain future chapters

Only add facts that would cause a continuity error if contradicted later. If the agent invented names, places, or terms during drafting, record them here immediately.

#### 5b. Update Any Existing Tracking Documents

For each tracking document that exists in the project, update it with this chapter's content:

- **Scene log** (`docs/06-scene-log.md`): Add entry with scene ID, location, time, POV, setting function, texture beats used, what changes, new facts, loose threads
- **Glossary** (`docs/05-glossary.md`): Add new names, places, terms, organizations. Update existing entries if new variants or aliases appeared
- **Thread tracker** (`docs/13-threads.md`): Mark threads touched — I (introduced), D (developed), S (seed planted), P (paid off). Add new threads that emerged during drafting.
- **Foreshadowing** (`docs/19-foreshadowing-checklist.md`): Mark seeds planted, note chapter. Add new foreshadowing opportunities with payoff targets.
- **Voice doc** (`docs/08-voice.md`): Note new voice patterns, character voice evolution, drift from established voice, moments that felt particularly right or wrong
- **Any other project-specific tracking docs**: Update as appropriate to their purpose

If a document exists, update it. Don't skip updates because a chapter felt minor — the compound value of consistent logging is the whole point.

#### 5c. Assess: Does This Project Need New Infrastructure?

This is the observation layer. After drafting, step back and look at what's accumulating in the project. Propose new documents only when the work has produced a real need — not because a template says you should have one.

**How to assess — check these patterns:**

**Scene log** (if one doesn't exist yet): After any chapter, the project benefits from a running record of what happened. If no scene log exists, propose one after the first chapter: "Now that we have a chapter drafted, I'd like to start a scene log — a running record of what happened in each chapter so we don't lose track of details between sessions. Want me to set that up?"

**Glossary**: Count the invented names, places, and terms across the continuity doc. If there are more than you can reliably keep straight (roughly 10+, or if you had to search back through previous content to check a spelling), propose a glossary. "We've invented [N] names and terms so far and I had to double-check the spelling of [example] — want me to pull these into a glossary so we have a quick reference?"

**Thread tracker**: Look at the subplots, relationship arcs, and narrative questions in play. If there are 3+ threads running and at least one hasn't been touched in the last 3-4 chapters, propose tracking. "We've got several threads going — [list them]. [Thread X] hasn't appeared since chapter [N]. A thread tracker would help us keep these visible so nothing goes dark by accident. Interested?"

**Foreshadowing tracker**: If the outline or the drafting planted something that's meant to pay off later, and no foreshadowing doc exists, propose one. "You planted [seed] in this chapter — do you have a payoff in mind for that? If we're going to be doing deliberate foreshadowing, a tracker would help us make sure seeds get harvested."

**Style guide**: After 3-5 chapters, patterns in prose style, POV, tense, chapter length, and tone have emerged through practice rather than prescription. Propose capturing them. "We've settled into a pattern — [third-person limited, past tense, chapters running 1,500-2,000 words, dry humor in interior monologue]. Want me to capture that in a style guide so it stays consistent?"

**Voice doc**: After 3-5 chapters, if no voice doc exists, the narrator's voice has started to take shape. Propose capturing it. "Your narrator has a voice now — [describe the pattern you're seeing: attention filter, stance, humor, what they notice vs. ignore]. Want me to start a voice doc to keep this consistent?"

**Project defaults in AGENTS.md**: If POV, tense, chapter length, or output sizing haven't been recorded yet and patterns have emerged, propose adding them. "We've been writing in [third-person limited, past tense] and chapters are landing around [X words]. Want me to lock those in as defaults?"

**Timeline doc**: If the narrative involves time jumps, parallel timelines, flashbacks, or if you're tracking seasonal/calendar time and it's getting complex, propose a timeline. "We've got [time complexity] going on — a timeline doc would help us keep the chronology straight."

**Relationship tracker**: If the cast is large enough that character relationships are evolving in ways that matter to the plot, and you're starting to lose track of who knows what or where relationships stand, propose one. "We've got [N] characters interacting in [complex ways] — a relationship tracker would help us keep track of where things stand between them."

**World-specific reference docs**: Genre and project-specific. A fantasy novel might need a magic rules doc when the system gets complex enough that consistency matters. A sci-fi novel might need a technology constraints doc. A thriller might need a timeline-of-events-the-protagonist-doesn't-know-yet doc. A historical novel might need a period-accuracy reference. Don't anticipate these — recognize them when the drafting starts bumping into the need.

**The key principle**: Propose, don't create. Explain what problem the document solves, give the user a concrete example from their own project, and let them decide. "Want me to set that up?" not "I've created a glossary for you."

### Step 6: Report

Summarize what was accomplished:

```
## Draft Complete: Chapter [NN] — [Title]

**Words**: [count]
**Location**: `draft/book-X/NN-chapter-XX-TITLE.md`

### What happened
[2-3 sentence summary of the chapter's events and state changes]

### Documents updated
[List only documents that were actually updated — don't list documents that don't exist]
- Continuity: [N] new facts added ([brief list])
- [Other tracking docs]: [what was updated]

### Continuity concerns
[Any potential issues noticed during drafting — contradictions, timeline questions, etc. "None" if clean.]

### Observations
[Voice, pacing, or structural patterns worth noting. Things that went well. Things that felt off. This is the agent's honest read, not a polished assessment.]

### Proposed infrastructure
[If the assessment in Step 5c identified a need, make the pitch here with specific examples from the project. If nothing is needed yet, omit this section entirely — don't say "no new infrastructure needed."]

### Next
[What the outline says comes next, or suggest running /plan-chapter for the next chapter]
```

## Notes

- If the outline calls for something that contradicts the continuity doc, follow the continuity doc and note the deviation from the outline.
- If inspiration during drafting leads to significant departures from the outline, note what changed and why in the report. Update relevant planning docs.
- Post-draft updates to existing documents are not optional. They're the mechanism that keeps the project coherent across sessions. Skipping them creates compounding continuity debt.
- If the agent invents a name, place, or term not in the outline, record it immediately in continuity (and glossary if one exists). The moment of invention is the moment of recording.
- The draft is a working draft, not polished final. Forward momentum is more valuable than perfection. Style polish comes in revision passes.
- When proposing new infrastructure, use the user's own material as examples — "we've invented 15 terms" is more persuasive than "projects typically benefit from a glossary." The user should see the need in their own work, not take your word for it.
- Don't propose more than one or two new documents per chapter. Even if multiple needs are emerging, space the proposals out. Each new document should be understood and valued before the next one appears.
- Update AGENTS.md's "Active Documents" section whenever a new tracking document is created.
