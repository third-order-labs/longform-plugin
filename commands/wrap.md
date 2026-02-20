---
description: End-of-session summary — verify all living documents are current, summarize progress, and preview the next session's work
argument-hint: ""
---

# /wrap — End-of-Session Summary

Clean session boundary. Ensures all documents are current, summarizes what was accomplished, and previews what's next. Run this at the end of every writing session.

## Invocation

```
/wrap
```

## Skills Referenced

- `long-form-methodology` — living documents, workflow state
- `continuity-management` — document currency check

## Workflow

### Step 1: Summarize Session Accomplishments

Review what happened this session:

- **Chapters planned**: List any outlines created via `/plan-chapter`
- **Chapters drafted**: List any chapters written via `/write-chapter`, with word counts
- **Reviews conducted**: Any `/review` audits and key findings
- **Other work**: Document updates, retcons, world-building additions, character development, outline revisions

### Step 2: Verify Living Documents

Check that all tracking documents reflect the current state of the manuscript:

#### Scene Log (`docs/06-scene-log.md`)
- Does every drafted chapter have a scene log entry?
- Are entries complete (no blank fields)?

#### Continuity (`docs/07-continuity.md`)
- Were new canon facts from this session's chapters recorded?
- Any facts that should be added but weren't?

#### Glossary (`docs/05-glossary.md`)
- Were new names/terms from this session's chapters recorded?
- Any missing entries?

#### Threads (`docs/13-threads.md`)
- Were thread markers updated for this session's chapters?
- Any thread appearances that weren't recorded?

#### Foreshadowing (`docs/19-foreshadowing-checklist.md`)
- Were any seeds planted this session? Are they recorded?
- Any foreshadowing that happened organically during drafting but wasn't tracked?

#### Voice (`docs/08-voice.md`)
- Were any voice observations from this session's chapters recorded?
- Has the authorial consciousness section sharpened based on user feedback?
- Do character voice profiles reflect any evolution from this session's drafting?
- Any new anti-patterns identified that should be added?

If any document is behind, **update it now** before closing the session.

### Step 3: Flag Documents Needing Attention

Identify any docs that need work beyond routine updates:

- Outline needs revision (story has diverged from the plan)
- Characters doc needs updating (new characters introduced, arcs changed)
- World doc needs expanding (new locations or world-building established in recent chapters)
- Style guide needs adjustment (the tone has shifted or the user has given new direction)
- Voice doc needs updating (new voice patterns emerged, character voices evolved, or authorial consciousness has sharpened through feedback)

These don't need to be fixed now — just flagged for next session.

### Step 4: Preview Next Session

Look ahead:

1. **Next chapter**: What does the outline say? If no outline exists for the next chapter, note that `/plan-chapter` should be the first action next session.
2. **Thread needs**: Which threads need oxygen soon? (Check for threads approaching the 4-chapter staleness threshold)
3. **Foreshadowing needs**: Any seeds that need planting in the upcoming window?
4. **Loose threads**: What unresolved questions from the scene log should be addressed?
5. **Open decisions**: Any deferred decisions from the north-star doc or previous sessions that are now blocking progress?

### Step 5: Generate Session Summary

```markdown
## Session Wrap — [date]

### Accomplished
- [List of what was done, with file references]

### Manuscript Status
- **Total chapters drafted**: [count]
- **Current word count**: [approximate total]
- **Current position**: Book [N], Chapter [NN]

### Document Health
| Document | Status | Notes |
|----------|--------|-------|
| Scene log | [current/behind] | [details if behind] |
| Continuity | [current/behind] | |
| Glossary | [current/behind] | |
| Threads | [current/behind] | |
| Foreshadowing | [current/behind] | |
| Voice | [current/behind/not yet created] | |

### Flagged for Attention
- [Any docs or issues that need work]

### Next Session Preview
- **First action**: [plan-chapter / write-chapter / fix issue]
- **Threads needing oxygen**: [list]
- **Foreshadowing window**: [seeds to plant]
- **Open questions**: [decisions to make]

### Notes
[Any observations, concerns, or ideas to carry forward]
```

## Notes

- This command is about maintaining session hygiene. A clean wrap means the next session starts with full context, not a "where were we?" scramble.
- If the session was purely planning (no drafting), the wrap is simpler — just confirm docs are current and preview the first draft.
- The preview section is crucial for multi-session projects. It reduces ramp-up time at the start of each session.
- If document health is behind, fix it as part of the wrap rather than deferring. Debt accumulates fast.
