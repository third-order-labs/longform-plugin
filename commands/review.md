---
description: Audit the manuscript against whatever tracking exists — continuity, threads, voice, foreshadowing — catch drift before it becomes structural
argument-hint: "<scope — 'full', 'recent', chapter range, or specific check>"
---

# /review — Manuscript Health Check

Audit the manuscript against whatever tracking documents exist in the project. The scope of the review adapts to the project's infrastructure — a project with only a continuity doc gets a continuity review; a project with the full suite of tracking documents gets the full audit.

Run this periodically (every 3-5 chapters) or whenever something feels off.

## Invocation

```
/review                    # Full audit (everything that exists)
/review recent             # Last 5 chapters only
/review chapters 10-15     # Specific range
/review continuity         # Continuity check only
/review threads            # Thread health only (if tracker exists)
/review voice              # Voice consistency only (if voice doc exists)
/review foreshadowing      # Foreshadowing status only (if tracker exists)
```

## Skills Referenced

- `continuity-management` — canon tracking, conflict detection
- `narrative-craft` — thread health, foreshadowing awareness
- `authorial-voice` — voice consistency, character distinction

## Workflow

### Step 1: Determine Scope and Available Audits

**Scope** — based on invocation:
- **Full**: Audit everything from the beginning
- **Recent**: Last 5 drafted chapters
- **Chapter range**: Specified chapters only
- **Specific check**: Only the requested audit type

**Available audits** — based on what documents exist in the project. Check what's there:

| Document | If exists | Audit available |
|----------|-----------|-----------------|
| `docs/07-continuity.md` | Always | Continuity audit |
| `docs/13-threads.md` | Check | Thread health check |
| `docs/08-voice.md` | Check | Voice consistency audit |
| `docs/19-foreshadowing-checklist.md` | Check | Foreshadowing audit |
| `docs/06-scene-log.md` | Check | Scene log completeness check |
| `docs/05-glossary.md` | Check | Glossary consistency check |

For full and recent audits, perform all available checks. For specific checks, perform only the requested one — if the required document doesn't exist, tell the user: "There's no thread tracker in this project yet, so I can't audit thread health. Want me to do a continuity review instead, or would you like to set up a thread tracker?"

### Step 2: Continuity Audit (always available)

Read `docs/07-continuity.md` and scan draft chapters in the review scope for contradictions:

- **Fact conflicts**: Does the draft state something that contradicts a canon entry? (character descriptions, established locations, timeline, relationships, world rules)
- **Timeline inconsistencies**: Do events happen in an impossible order? Do travel times make sense?
- **Character consistency**: Do characters act in ways that contradict established traits without narrative justification? Are names/titles used correctly?
- **World rule violations**: Does the draft break established rules about how the world works?

For each issue found, record:
- What the contradiction is
- Which draft chapter and which continuity entry conflict
- Severity: **Critical** (breaks the plot), **Major** (noticeable to readers), **Minor** (nitpick)
- Suggested fix

### Step 3: Thread Health Check (if `docs/13-threads.md` exists)

Check each active thread:

- **Stale threads**: Any thread introduced (I) or developed (D) more than **4 chapters ago** without a subsequent appearance
- **Orphaned threads**: Threads introduced but never developed (I only, with no D/S/P markers)
- **Premature payoffs**: Threads paid off (P) without sufficient development
- **Missing threads**: Threads mentioned in the outline that haven't been introduced yet

For each issue:
- Which thread, how many chapters since last appearance
- Severity: **High** (reader will notice the dropped thread), **Medium** (thread losing momentum), **Low** (thread can wait a bit longer)
- Suggested action: develop in next chapter, plant a reminder, consciously shelve, or pay off

**If no thread tracker exists** but the review scope covers 8+ chapters: While doing the continuity audit, note any subplots or narrative threads you observe running through the chapters. If you identify threads that seem to have gone dark or been dropped, mention it in the report — and note that a thread tracker would make this check systematic rather than ad hoc.

### Step 4: Voice Consistency Audit (if `docs/08-voice.md` exists)

Audit voice consistency across the reviewed chapters:

- **Narrator consistency**: Do recent chapters sound like they're written by the same consciousness? Is the attention filter consistent? Are the beliefs and stance toward events stable?
- **Character voice distinction**: Do POV characters' interior voices match their profiles? Can you distinguish one POV character from another by voice alone?
- **Voice drift**: Is the narrator becoming more generic over time? Are character voices converging toward a single default?
- **Anti-pattern check**: Are anti-patterns from the voice doc appearing in recent drafts?
- **Evolution tracking**: Has any character's voice evolved in ways that should be recorded in their profile?

For each issue:
- What the voice problem is, which chapters are affected
- Severity: **High** (fundamentally off-voice), **Medium** (drifting), **Low** (minor inconsistency)
- Suggested correction

**If no voice doc exists** but the review scope covers 5+ chapters: Note any voice observations from reading the drafts — is the narrator's voice consistent? Do POV characters sound distinct from each other? If patterns are clear enough to capture, suggest creating a voice doc. "Your narrator has a consistent voice across these chapters — [describe it]. Want to capture that in a voice doc so it stays locked in?"

### Step 5: Foreshadowing Audit (if `docs/19-foreshadowing-checklist.md` exists)

Check the foreshadowing tracker:

- **Unplanted seeds**: Seeds that should have been planted by now but haven't been
- **Approaching deadlines**: Seeds whose payoff target is within the next 3-5 chapters and haven't been planted
- **Under-supported payoffs**: Seeds planted once but needing reinforcement before their payoff window
- **Orphaned seeds**: Seeds planted but whose payoff target is past or unclear

For each issue:
- Which seed, current status, payoff target
- Urgency: **Urgent** (payoff window is now), **Soon** (next few chapters), **Watch** (approaching)

### Step 6: Scene Log Audit (if `docs/06-scene-log.md` exists)

Check the scene log:

- **Unresolved loose threads**: Items listed as loose threads across entries that were never picked up in subsequent scenes
- **Missing entries**: Chapters that have drafts but no scene log entry (indicates post-draft update was skipped)
- **Incomplete entries**: Scene log entries with blank fields

### Step 7: Glossary Consistency (if `docs/05-glossary.md` exists)

Spot-check against recent drafts:

- **Name drift**: Character or place names spelled differently in draft vs. glossary
- **Missing entries**: Names or terms used in recent drafts that aren't in the glossary
- **Stale entries**: Glossary entries that were superseded or renamed but not updated

### Step 8: Generate Report

The report only includes sections for audits that were actually performed. Don't include empty sections for documents that don't exist.

```markdown
## Review Report — [scope]

**Chapters reviewed**: [range]
**Date**: [date]
**Audits performed**: [list which checks were run based on available documents]

### Summary
[One line per audit type that was performed, with issue count and severity breakdown]

### Critical Issues (fix before next draft)
1. [Issue description, location, suggested fix]

### Major Issues (fix soon)
1. [Issue description, location, suggested fix]

### Minor Issues (note for later)
1. [Issue description, location, suggested fix]
```

Add detail sections only for audits that found issues:

Thread health table (if thread tracker exists and issues found):
```markdown
### Thread Health
| Thread | Last Appearance | Status | Action Needed |
|--------|----------------|--------|---------------|
```

Foreshadowing table (if tracker exists and issues found):
```markdown
### Foreshadowing Status
| Seed | Planted? | Payoff Target | Urgency |
|------|----------|---------------|---------|
```

Voice table (if voice doc exists and issues found):
```markdown
### Voice Consistency
| Issue | Chapters | Severity | Suggested Fix |
|-------|----------|----------|---------------|
```

End with:
```markdown
### Recommendations
[Prioritized list of what to address next, and when]

### Infrastructure Observations
[Only if the review surfaced needs that existing tracking doesn't cover. Specific examples, not generic suggestions. Omit this section if nothing surfaced.]
```

## Notes

- Run this regularly. Continuity debt compounds — small inconsistencies become structural problems if left unchecked.
- The review doesn't fix anything — it identifies issues. The user decides what to fix and when.
- Critical issues should block further drafting until resolved. Major issues should be addressed within 1-2 chapters. Minor issues can be batched for a revision pass.
- If the review reveals that existing tracking docs are behind (missing scene log entries, un-updated threads), prioritize catching up the docs before drafting more chapters.
- The review is also a natural moment to observe whether the project has outgrown its infrastructure. If you're doing the continuity audit and finding yourself mentally tracking threads, noting voice inconsistencies, or catching foreshadowing that's going stale — those are signs that the corresponding tracking docs would make the next review more systematic. Note them in the Infrastructure Observations section, but let `/wrap` be where the formal proposals happen.
