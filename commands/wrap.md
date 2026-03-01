---
description: End-of-session summary — verify tracking docs are current, assess project evolution, summarize progress, and set up the next session
argument-hint: ""
---

# /wrap — End-of-Session Summary

Clean session boundary. Check that whatever tracking documents exist are current, take stock of where the project stands, and make sure the next session can start without a "where were we?" scramble.

This is also a natural checkpoint for project evolution — a wider-angle view than `/write-chapter` provides. If the project has been outgrowing its infrastructure across several chapters, this is where to address it.

## Invocation

```
/wrap
```

## Skills Referenced

- `long-form-methodology` — living documents, workflow state
- `continuity-management` — document currency, canon verification
- `narrative-craft` — thread health, foreshadowing status (if tracking docs exist)

## Workflow

### Step 1: Summarize Session Accomplishments

Review what happened this session:

- **Chapters planned**: List any outlines created via `/plan-chapter`
- **Chapters drafted**: List any chapters written via `/write-chapter`, with word counts
- **Reviews conducted**: Any `/review` audits and key findings
- **Other work**: Document updates, retcons, world-building additions, character development, outline revisions, new tracking docs created

### Step 2: Verify Existing Documents

Check that all tracking documents *that currently exist* reflect the current state of the manuscript. Don't check for documents that haven't been created — that's Step 3's job.

**Always check:**

- **Continuity** (`docs/07-continuity.md`) — Were new canon facts from this session's chapters recorded? Anything missing?
- **Characters** (`docs/03-characters.md`) — Were new characters introduced this session? Do existing characters need arc updates?

**Check if they exist:**

- **Scene log** (`docs/06-scene-log.md`) — Does every drafted chapter have an entry? Are entries complete?
- **Glossary** (`docs/05-glossary.md`) — Were new names/terms recorded? Any missing entries?
- **Thread tracker** (`docs/13-threads.md`) — Were thread markers updated? Any thread appearances that weren't recorded?
- **Foreshadowing** (`docs/19-foreshadowing-checklist.md`) — Were seeds planted this session recorded? Any organic foreshadowing that wasn't tracked?
- **Voice doc** (`docs/08-voice.md`) — Were voice observations recorded? Has the authorial voice sharpened? Character voice evolution captured?
- **Style guide** (`docs/25-style-guide.md`) — Has the prose style shifted in ways that should be captured?
- **Any other project-specific tracking docs** — Update as appropriate to their purpose

If any existing document is behind, **update it now** before closing the session.

### Step 3: Project Evolution Assessment

This is the wider-angle version of `/write-chapter`'s infrastructure proposals. Instead of looking at one chapter, look across the session and the manuscript as a whole.

**Review the project's current state:**

- How many chapters have been drafted?
- How many characters, locations, and invented terms exist?
- How many subplots and narrative threads are in play?
- How complex has the timeline gotten?
- How much world-building has accumulated?
- What's the cast size and how are relationships evolving?

**Then ask: what's the project bumping into?**

Think about what was hard during this session. Where did you have to search back through previous chapters to check something? Where did continuity feel fragile? Where did the user have to remind you of something you should have known? Those friction points are signals.

**Propose new infrastructure when you see these patterns:**

- **Invented terms are hard to keep straight** → glossary (if not yet created)
- **Subplots are going dark or getting tangled** → thread tracker
- **Deliberate seeds are being planted without a tracking mechanism** → foreshadowing tracker
- **The narrator's voice has emerged but isn't captured** → voice doc
- **Prose patterns are established but undocumented** → style guide
- **Chronology is getting complex** → timeline doc
- **Character relationships are evolving in plot-relevant ways and you're losing track** → relationship tracker
- **The world has rules or systems that need consistency** → world-specific reference doc (magic system, technology constraints, political structure, period-accuracy reference, etc.)
- **The outline has drifted significantly from what's been written** → outline revision or new chapter map
- **The cast has grown large enough that who-knows-what matters** → knowledge tracker or character awareness matrix
- **Writing defaults have emerged but aren't recorded** → AGENTS.md defaults update

**How to propose:** Same principle as `/write-chapter` — use specific examples from the project, explain what problem the document solves, let the user decide. But at wrap time, you can be a bit more expansive than mid-chapter. This is the reflective moment.

**Don't propose everything at once.** If multiple needs are emerging, prioritize the one or two that would have the biggest impact on the next few chapters. The rest can wait for the next wrap.

**If the project is early (chapters 1-3):** It's probably too soon for most infrastructure beyond what `/write-chapter` already proposes (scene log, glossary). Don't rush it. The project needs to develop enough complexity to earn its tracking systems.

**If the project is mid-flight (chapters 8+):** This is where the biggest evolution happens. The cast is full, subplots are running, the world is built out. If the infrastructure hasn't grown with it, the user is probably starting to feel the friction even if they haven't named it yet.

### Step 4: Flag Documents Needing Deeper Work

Separate from currency checks (Step 2) and new infrastructure (Step 3), identify existing docs that need more than routine updates:

- Outline needs revision (story has diverged from the plan)
- Characters doc needs major updating (new characters, arc changes, relationships shifted)
- World doc needs expanding (significant new world-building established in recent chapters)
- Voice doc needs sharpening (patterns have clarified, or the voice has evolved)
- Continuity doc is getting unwieldy (needs reorganization, not just additions)

These don't need to be fixed now — just flagged for next session.

### Step 5: Preview Next Session

Look ahead based on what exists in the project:

1. **Next chapter**: What does the outline say? If no outline exists for the next chapter, note that `/plan-chapter` should be the first action next session.
2. **Thread oxygen** (if thread tracker exists): Which threads need attention soon? Any approaching the staleness threshold?
3. **Foreshadowing windows** (if foreshadowing tracker exists): Any seeds that need planting soon?
4. **Loose threads**: What unresolved questions from the scene log (if it exists) or continuity doc should be addressed?
5. **Open decisions**: Any deferred decisions from earlier sessions that are now blocking or informing upcoming chapters?
6. **Infrastructure to create**: If new documents were proposed in Step 3 and the user agreed, note that setting them up is first-session-next-time work.

### Step 6: Generate Session Summary

```markdown
## Session Wrap — [date]

### Accomplished
- [List of what was done, with file references]

### Manuscript Status
- **Total chapters drafted**: [count]
- **Current word count**: [approximate total]
- **Current position**: Book [N], Chapter [NN]

### Document Status
[List only documents that exist in the project]
| Document | Current? | Notes |
|----------|----------|-------|
| Continuity | [yes/updated] | [details if updated] |
| [other existing docs] | [yes/updated/behind] | [details] |

### Project Evolution
[If new infrastructure was proposed, note what and why. If nothing was proposed, omit this section.]

### Flagged for Attention
[Docs or issues that need deeper work. Omit if nothing flagged.]

### Next Session
- **Start with**: [plan-chapter / write-chapter / create proposed doc / fix flagged issue]
- **Upcoming threads**: [if tracker exists — what needs oxygen]
- **Open questions**: [decisions to make or things to figure out]

### Notes
[Observations, concerns, ideas to carry forward. The agent's honest read on how the project is going — what's working, what's starting to strain, what feels good.]
```

## Notes

- This command is about session hygiene AND project evolution. The hygiene part (docs current, summary written) ensures smooth session transitions. The evolution part (infrastructure assessment) ensures the project's support system grows with its complexity.
- If the session was purely planning (no drafting), the wrap is simpler — confirm docs are current, summarize decisions made, preview the first draft.
- The preview section is crucial for multi-session projects. It reduces ramp-up time and prevents the "where were we?" problem.
- If document health is behind, fix it as part of the wrap rather than deferring. Debt accumulates fast.
- The session summary is a real document — write it honestly, not as a progress report. If the session was rough, say so. If the story surprised you, note that. These summaries become the project's memory of its own process.
- Update AGENTS.md's "Active Documents" section if any new tracking docs were created this session.
