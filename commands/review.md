---
description: Audit continuity, thread health, foreshadowing status, and glossary consistency — catch drift before it becomes a problem
argument-hint: "<scope — 'full', 'recent', chapter range, or specific check>"
---

# /review — Continuity & Thread Audit

Health check across all tracking documents. Catches drift before it becomes a structural problem. Run this periodically (every 3-5 chapters) or whenever something feels off.

## Invocation

```
/review                    # Full audit
/review recent             # Last 5 chapters only
/review chapters 10-15     # Specific range
/review threads            # Thread health only
/review continuity         # Continuity check only
/review foreshadowing      # Foreshadowing status only
```

## Skills Referenced

- `continuity-management` — canon tracking, conflict detection
- `narrative-craft` — thread health, foreshadowing system

## Workflow

### Step 1: Determine Scope

Based on invocation:
- **Full**: Audit everything from the beginning
- **Recent**: Last 5 drafted chapters
- **Chapter range**: Specified chapters only
- **Specific check**: Only the requested audit type

For full and recent audits, perform all checks below. For specific checks, perform only the requested one.

### Step 2: Continuity Audit

Read `docs/07-continuity.md` and scan recent draft chapters for contradictions:

- **Fact conflicts**: Does the draft state something that contradicts a canon entry? (character descriptions, established locations, timeline, relationships, world rules)
- **Timeline inconsistencies**: Do events happen in an impossible order? Do travel times make sense?
- **Character consistency**: Do characters act in ways that contradict established traits without narrative justification? Are names/titles used correctly?
- **World rule violations**: Does the draft break established rules about how the world works?

For each issue found, record:
- What the contradiction is
- Which draft chapter and which continuity entry conflict
- Severity: **Critical** (breaks the plot), **Major** (noticeable to readers), **Minor** (nitpick)
- Suggested fix

### Step 3: Thread Health Check

Read `docs/13-threads.md` and check each active thread:

- **Stale threads**: Any thread introduced (I) or developed (D) more than **4 chapters ago** without a subsequent appearance
- **Orphaned threads**: Threads introduced but never developed (I only, with no D/S/P markers)
- **Premature payoffs**: Threads paid off (P) without sufficient development
- **Missing threads**: Threads mentioned in the outline that haven't been introduced yet

For each issue:
- Which thread
- How many chapters since last appearance
- Severity: **High** (reader will notice the dropped thread), **Medium** (thread losing momentum), **Low** (thread can wait a bit longer)
- Suggested action: develop in next chapter, plant a reminder, consciously shelve, or pay off

### Step 3b: Voice Consistency Audit

If `docs/08-voice.md` exists, audit voice consistency across the reviewed chapters:

- **Narrator consistency**: Do recent chapters sound like they're written by the same consciousness? Is the attention filter consistent — does the narrator notice the same kinds of things? Are the beliefs and stance toward events stable?
- **Character voice distinction**: Do POV characters' interior voices match their profiles? Can you distinguish one POV character from another by voice alone?
- **Voice drift**: Is the narrator becoming more generic over time? Are character voices converging toward a single default? Is the prose losing the specific qualities captured in the voice doc?
- **Anti-pattern check**: Are anti-patterns from the voice doc appearing in recent drafts? Is the prose falling into any of the novel-specific anti-patterns (identical character voices, telling instead of showing, omniscient leaking into limited POV)?
- **Evolution tracking**: Has any character's voice evolved in ways that should be recorded in their profile? Has the authorial consciousness sharpened or shifted based on recent drafting?

For each issue:
- What the voice problem is
- Which chapters are affected
- Severity: **High** (fundamentally off-voice), **Medium** (drifting), **Low** (minor inconsistency)
- Suggested correction

### Step 4: Foreshadowing Audit

Read `docs/19-foreshadowing-checklist.md`:

- **Unplanted seeds**: Seeds that should have been planted by now (based on payoff target timeline) but haven't been
- **Approaching deadlines**: Seeds whose payoff target is within the next 3-5 chapters and haven't been planted
- **Under-supported payoffs**: Seeds planted once but needing reinforcement before their payoff window
- **Orphaned seeds**: Seeds planted but whose payoff target is past or unclear

For each issue:
- Which seed
- Current status (planted/not planted, in which chapter)
- Payoff target
- Urgency: **Urgent** (payoff window is now), **Soon** (next few chapters), **Watch** (approaching)

### Step 5: Scene Log Audit

Read `docs/06-scene-log.md`:

- **Unresolved loose threads**: Items listed in "Loose threads" across entries that were never picked up in subsequent scenes
- **Missing entries**: Chapters that have drafts but no scene log entry (indicates the post-draft update was skipped)
- **Incomplete entries**: Scene log entries with blank fields

### Step 6: Glossary Consistency

Read `docs/05-glossary.md` and spot-check against recent drafts:

- **Name drift**: Character or place names spelled differently in draft vs. glossary
- **Missing entries**: Names or terms used in recent drafts that aren't in the glossary
- **Stale entries**: Glossary entries that were superseded or renamed but not updated

### Step 7: Generate Report

Produce a structured report:

```markdown
## Review Report — [scope]

**Chapters reviewed**: [range]
**Date**: [date]

### Summary
- Continuity issues: [count] ([critical/major/minor breakdown])
- Stale threads: [count]
- Foreshadowing concerns: [count]
- Scene log gaps: [count]
- Glossary inconsistencies: [count]
- Voice consistency issues: [count]

### Critical Issues (fix before next draft)
1. [Issue description, location, suggested fix]

### Major Issues (fix soon)
1. [Issue description, location, suggested fix]

### Minor Issues (note for later)
1. [Issue description, location, suggested fix]

### Thread Health
| Thread | Last Appearance | Status | Action Needed |
|--------|----------------|--------|---------------|
| [name] | Ch [NN] | [stale/healthy/orphaned] | [suggestion] |

### Foreshadowing Status
| Seed | Planted? | Payoff Target | Urgency |
|------|----------|---------------|---------|
| [description] | [Ch NN / No] | [target] | [urgent/soon/watch] |

### Voice Consistency
| Issue | Chapters | Severity | Suggested Fix |
|-------|----------|----------|---------------|
| [description] | [affected chapters] | [high/medium/low] | [suggestion] |

### Recommendations
[Prioritized list of what to address next, and when]
```

## Notes

- Run this regularly. Continuity debt compounds — small inconsistencies become structural problems if left unchecked.
- The review doesn't fix anything — it identifies issues. The user decides what to fix and when.
- Critical issues should block further drafting until resolved. Major issues should be addressed within 1-2 chapters. Minor issues can be batched for a revision pass.
- If the review reveals that tracking docs are behind (missing scene log entries, un-updated threads), prioritize catching up the docs before drafting more chapters. The methodology only works if the docs are current.
