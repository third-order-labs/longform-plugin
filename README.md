# Longform

A writing workflow plugin for [Cowork](https://claude.com/product/cowork) (also compatible with Claude Code) that maintains coherence across novel-length fiction. Provides structured continuity tracking, thread management, foreshadowing systems, and living documents that grow with your manuscript.

> **What this is:** A methodology plugin. It doesn't generate plots or characters for you — it gives the AI agent the workflow discipline to maintain a 100k+ word manuscript without losing track of what happened in chapter 3 by the time you're drafting chapter 30. Genre-neutral, no fantasy/sci-fi specifics baked in.

## How It Works

Long-form fiction breaks without external memory. An AI agent can't hold an entire novel in context simultaneously, so structured documents become the memory system. This plugin implements a workflow loop proven across 116k words of published fiction:

**Plan → Draft → Log → Verify → Repeat**

Every chapter gets an outline before drafting. Every draft triggers automatic updates to scene logs, continuity records, glossary, thread tracking, and foreshadowing checklists. The documents grow with the manuscript, not before it.

## Installation

```
claude plugins add longform
```

## Quick Start

### 1. Install the plugin

```
claude plugins add longform
```

### 2. Start a new project

```
/start-project
```

This walks you through defining your concept — pitch, characters, world, tone, scope — and scaffolds the full document structure. It's a conversation, not a questionnaire.

### 3. Plan your first chapter

```
/plan-chapter
```

Creates a detailed outline with scene breakdowns, lived-in targets, thread assignments, and foreshadowing seeds.

### 4. Draft from the outline

```
/write-chapter
```

Drafts the chapter, then automatically updates all tracking documents — scene log, continuity, glossary, threads, foreshadowing.

### 5. Check your work periodically

```
/review
```

Audits continuity, thread health, foreshadowing status, and glossary consistency. Catches drift before it becomes a problem.

### 6. End each session cleanly

```
/wrap
```

Summarizes progress, verifies all documents are current, and previews the next session's work.

## Commands

### `/start-project` — Bootstrap a New Writing Project

Interactive project setup. Walks through defining your concept and scaffolds the full document structure: pitch, north-star, world, characters, outline, tracking docs, style guide, AGENTS.md, and directory structure.

```
/start-project
/start-project "noir detective novel set in 1940s LA"
```

### `/plan-chapter` — Pre-Draft Chapter Planning

Creates a detailed chapter outline before drafting. Checks thread health, foreshadowing needs, and recent scene log for context. Produces a spec the agent can execute against.

```
/plan-chapter
/plan-chapter next
/plan-chapter 12
/plan-chapter "The Crossing"
```

### `/write-chapter` — Draft a Chapter

The core workflow loop. Drafts from the outline, then automatically updates scene log, continuity, glossary, threads, and foreshadowing checklist. Reports what was written and what was updated.

```
/write-chapter
/write-chapter next
/write-chapter 12
```

### `/review` — Continuity & Thread Audit

Health check across all tracking documents. Scans for continuity contradictions, stale threads, unplanted foreshadowing seeds, scene log gaps, and glossary inconsistencies. Produces a severity-ranked report.

```
/review                    # Full audit
/review recent             # Last 5 chapters
/review threads            # Thread health only
/review continuity         # Continuity check only
```

### `/wrap` — End-of-Session Summary

Clean session boundary. Verifies all living documents are current, summarizes what was accomplished, flags documents needing attention, and previews the next session's work.

```
/wrap
```

### `/voice-session` — Capture Authorial Voice

Conversational voice capture session. Produces the authorial consciousness layer — what makes this novel sound like it was written by one mind. Two modes: full session for the narrator's worldview, or character-focused session for individual POV character profiles.

```
/voice-session
/voice-session character "Elena"
```

## Skills

| Skill | Description |
|-------|-------------|
| `long-form-methodology` | Core philosophy: why structure enables coherence at scale, document hierarchy, workflow loop, living documents, decision rules |
| `continuity-management` | Scene log format, canon tracking, conflict resolution (canon always wins), cumulative tracking, glossary as entity resolver |
| `narrative-craft` | Thread tracking (I/D/P/S markers), thread health monitoring, foreshadowing as deliberate system, arc pacing, multi-book continuity |
| `scene-craft` | Lived-in texture, texture beats, supporting character motives, consequence glue, dialogue craft, POV discipline, violence/humor/magic presentation |
| `authorial-voice` | Voice in long-form fiction: authorial consciousness layer, character voice profiles, two-layer capture system, novel-specific anti-patterns |
| `project-scaffolding` | Full template library for all planning documents, directory conventions, file naming rules |

## Example Workflows

### Starting a Novel

1. Run `/start-project` — define your concept through conversation
2. Review the scaffolded documents in `docs/`
3. Run `/plan-chapter` to outline chapter 1
4. Run `/write-chapter` to draft it
5. Continue the plan → write cycle

### Mid-Project Health Check

1. Run `/review` to audit all tracking documents
2. Fix any critical continuity issues before drafting more
3. Address stale threads in the next chapter plan
4. Plant any overdue foreshadowing seeds

### Daily Writing Session

1. Run `/plan-chapter next` to outline the next chapter
2. Run `/write-chapter` to draft it
3. Repeat for additional chapters
4. Run `/wrap` to close the session cleanly

### Multi-Book Series

1. Set up the project as a series in `/start-project`
2. Use the same tracking documents across all volumes (scene log, continuity, threads, glossary are cumulative)
3. Use `/review` at the end of each volume to check series-level thread health
4. Plant foreshadowing seeds for future volumes during current drafting

## Project Structure (scaffolded by `/start-project`)

```
your-novel/
├── AGENTS.md                         # Agent workflow rules
├── docs/
│   ├── 00-pitch.md                   # Hook, synopsis, core contrasts
│   ├── 01-north-star.md              # Guardrails and open decisions
│   ├── 02-world.md                   # Setting, geography, society
│   ├── 03-characters.md              # Cast with arcs
│   ├── 04-outline.md                 # Act structure and beats
│   ├── 05-glossary.md                # Names, terms, places
│   ├── 06-scene-log.md               # Running ledger of what happened
│   ├── 07-continuity.md              # Canon facts (highest precedence)
│   ├── 08-voice.md                   # Authorial consciousness + character voices
│   ├── 09-chapter-outline-template.md # Reusable chapter outline format
│   ├── 13-threads.md                 # Thread tracking with I/D/P/S markers
│   ├── 19-foreshadowing-checklist.md # Seeds and payoff targets
│   └── 25-style-guide.md            # Prose register, POV, tone
├── outlines/
│   └── book-one/                     # Chapter outlines
├── draft/
│   └── book-one/                     # Draft chapters
└── manuscript/                       # Final assembled manuscript
```

## Document Hierarchy

When documents conflict, resolve in this order (highest precedence first):

1. **Continuity** (`07-continuity.md`) — canon facts that must not be broken
2. **Voice** (`08-voice.md`) — authorial consciousness + character voice profiles
3. **Outline** (`04-outline.md`) — the structural plan
4. **Threads** (`13-threads.md`) — active narrative threads
5. **Scene log** (`06-scene-log.md`) — what actually happened
6. **Style guide** (`25-style-guide.md`) — prose and tone targets
7. **Pitch** (`00-pitch.md`) — the original vision

## File Structure

```
longform-plugin/
├── .claude-plugin/plugin.json
├── README.md
├── commands/
│   ├── start-project.md
│   ├── plan-chapter.md
│   ├── write-chapter.md
│   ├── review.md
│   ├── wrap.md
│   └── voice-session.md
└── skills/
    ├── authorial-voice/SKILL.md
    ├── long-form-methodology/SKILL.md
    ├── continuity-management/SKILL.md
    ├── narrative-craft/SKILL.md
    ├── scene-craft/SKILL.md
    └── project-scaffolding/SKILL.md
```
