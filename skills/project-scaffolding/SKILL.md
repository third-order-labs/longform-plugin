---
name: project-scaffolding
description: Templates, directory conventions, and document structure for scaffolding long-form fiction projects. Contains the full template library used by /start-project.
---

# Project Scaffolding

This skill provides the complete template library and directory conventions for long-form fiction projects. It defines the standard project structure, file naming rules, and starter templates for every planning document. The `/start-project` command uses these templates to initialize a new project repository.

---

## Directory Conventions

```
project-root/
├── AGENTS.md                    # Agent workflow rules and defaults
├── docs/                        # All planning and tracking documents
│   ├── 00-pitch.md
│   ├── 01-north-star.md
│   ├── 02-world.md
│   ├── 03-characters.md
│   ├── 04-outline.md
│   ├── 05-glossary.md
│   ├── 06-scene-log.md
│   ├── 07-continuity.md
│   ├── 08-voice.md
│   ├── 09-chapter-outline-template.md
│   ├── 13-threads.md
│   ├── 19-foreshadowing-checklist.md
│   └── 25-style-guide.md
├── outlines/                    # Chapter outlines by volume
│   ├── book-one/
│   ├── book-two/
│   └── book-three/
├── draft/                       # Draft chapters by volume
│   ├── book-one/
│   ├── book-two/
│   └── book-three/
└── manuscript/                  # Final assembled manuscript
```

### Purpose of each directory

- **docs/** -- All planning, tracking, and reference documents. Numbered for sort order.
- **outlines/** -- Per-chapter outlines organized by volume. Written before drafting.
- **draft/** -- Narrative chapter files organized by volume. The working text.
- **manuscript/** -- Final assembled output for export or submission.

---

## File Naming Conventions

- **Docs**: `NN-name.md` where NN is a two-digit number for ordering (00, 01, 02...).
- **Chapter outlines**: `NN-chapter-title.md` (e.g., `01-the-crossing.md`).
- **Draft chapters**: `NN-chapter-XX-TITLE.md` (e.g., `01-chapter-01-The-Crossing.md`).
- Numbers provide sort ordering and cross-reference anchors across documents.

---

## Document Templates

The following templates are created by `/start-project`. Each contains the structure and placeholder content showing the user what to fill in.

---

### `00-pitch.md`

```markdown
# [Project Title] — Pitch

## One-line hook
[One sentence: who, what situation, what choice]

## Short synopsis
[3-5 paragraphs: setup, conflict, stakes, what makes this story worth telling]

## Series note
[Standalone / Series — if series, what's the scope?]

## Core contrasts
- [Contrast 1] (e.g., freedom vs. security)
- [Contrast 2] (e.g., freedom vs. safety)
- [Contrast 3] (e.g., identity vs. role)
```

---

### `01-north-star.md`

```markdown
# North Star (Decisions + Guardrails)

## Goal
[What are we building? One sentence.]

## Vibe targets
- Atmosphere: [adjective + adjective + genre feel]
- Moral center: [what ethical stance does the narrative take?]
- Humor: [what kind, how much?]

## Open decisions (answer to lock the draft)
- Target length: [word count / chapter count]
- Series shape: [standalone / duology / trilogy / series]
- POV + tense: [first/third, past/present, limited/omniscient]
- Rating lines: [any content boundaries?]
```

---

### `02-world.md`

```markdown
# World

## Geography
[Major regions, climate, distances, travel routes]

## Society
[Power structures, social classes, economy, culture]

## Technology / Magic Level
[What exists in this world? What are the rules and limits?]

## History
[Key events that shaped the current world state]

## Daily Life
[What does ordinary life look like for ordinary people?]
```

---

### `03-characters.md`

```markdown
# Characters

## Protagonist
- Name:
- Age/description:
- Starting state:
- Core want:
- Core need (may differ from want):
- Arc: [beginning state] → [end state]
- Voice: [how they think/speak — vocabulary, rhythm, worldview]

## Mentor / Guide
- Name:
- Role in protagonist's life:
- What they offer:
- What they withhold or get wrong:
- Arc:

## Antagonist
- Name:
- Motivation:
- Method:
- Why they believe they're right:
- Arc:

## Supporting Cast
| Name | Role | Key trait | Relationship to protagonist | Arc note |
|------|------|-----------|----------------------------|----------|
| | | | | |
```

---

### `04-outline.md`

```markdown
# Outline

## Act Structure
[3-act, 4-act, or custom — describe the shape]

## Major Beats
1. [Opening image / status quo]
2. [Inciting incident]
3. [First turning point]
4. [Midpoint]
5. [Second turning point]
6. [Climax]
7. [Resolution]

## Sequence Breakdown
### Act I: [name]
- Sequence 1: [chapters NN-NN — what happens, what changes]
- Sequence 2: [chapters NN-NN — what happens, what changes]

### Act II: [name]
- Sequence 3: [chapters NN-NN]
- Sequence 4: [chapters NN-NN]

### Act III: [name]
- Sequence 5: [chapters NN-NN]
- Sequence 6: [chapters NN-NN]
```

---

### `05-glossary.md`

```markdown
# Glossary

| Term | Definition | Variants/Aliases | First Appearance |
|------|-----------|-----------------|-----------------|
| | | | |
```

---

### `06-scene-log.md`

```markdown
# Scene Log

Use this as a running ledger so we don't lose continuity.

## Template
- Scene ID:
- Location:
- Time:
- POV:
- Setting function:
- Texture beats:
- What changes:
- New facts introduced:
- Loose threads:

---

## Logged

[Entries added automatically after each drafted chapter]
```

---

### `07-continuity.md`

```markdown
# Continuity (Facts We Must Not Break)

## Protagonist baseline
- [Key facts about the main character]

## World baseline
- [Key facts about the world that cannot be contradicted]

## Terminology conventions
- [Established terms and their usage rules]

## Timeline
- [Key dated events in story order]
```

---

### `08-voice.md`

```markdown
# Voice

## Authorial Consciousness

### Attention filter
[What does this narrator notice? Physical spaces, social dynamics, power, the mundane, interior states? What gets lingered on vs. passed over?]

### Beliefs about the world
[Operating assumptions — not the novel's theme, but the narrator's lens. Do people change? Are institutions redeemable? Is violence clarifying or corrupting?]

### What this narrator refuses to say directly
[How much is stated vs. implied? Confessional or withholding? How much interiority is on the page?]

### Relationship to suffering
[How pain, loss, injustice are presented. Clinical, empathetic, dark humor, detached?]

### Relationship to humor
[When humor appears, what form, what it's allowed to touch]

### Energy levels
- Level 1 — [quiet observation, understated weight]
- Level 2 — [analytical, working through, building]
- Level 3 — [committed, landing claims, intensity rising]
- Level 4 — [compressed, declarative, peak moments — rare]

### Prose anti-patterns (kill on sight)
- [Project-specific anti-patterns]
- [AI fiction anti-patterns relevant to this project's voice]

### What this narrator sounds like at their best
[2-3 example passages or descriptions of the target voice when it's working]

### The gap to watch for
[Where will the AI drift? Over-polishing? Under-expressing? Defaulting to generic competent prose?]

---

## Character Voices

### [Character Name] — [Role]
- Speech patterns: [vocabulary, syntax, typical expressions, rhythm]
- Interior voice: [how they think — formal/intuitive, rushed/deliberate, honest/self-deceiving]
- Blind spots: [what they refuse to see or can't perceive]
- False certainties: [what they're sure about that's wrong]
- Energy range: [what moves them between registers]
- Evolution: [how voice shifts across the arc — early vs. late]

[Repeat for each POV character]

---

*Living document. Sharpens through drafting sessions. The first 3-5 chapters are calibration.*
```

---

### `09-chapter-outline-template.md`

```markdown
# Chapter Outline Template

Use this when we're ready to draft a chapter.

## Chapter summary (3-6 sentences)

## Lived-in targets (fill before drafting)
- Setting function (what this place is *for* day-to-day):
- 2-3 texture beats (non-plot):
  -
  -
  -
- One supporting-character motive to surface (fear/debt/pride/kindness-with-cost):

## Scenes
For each scene:
- POV:
- Location/time:
- Goal:
- Obstacle:
- Action beats (bullets):
- Outcome/turn:
- New question raised:

## Continuity updates
- Add names/terms to `docs/05-glossary.md`
- Add durable facts to `docs/07-continuity.md`
- Add scene entry to `docs/06-scene-log.md`
```

---

### `13-threads.md`

```markdown
# Threads (Introduced → Developed → Paid Off)

Use this to ensure long arcs get oxygen across chapters and don't vanish for 100 pages.

## How to use
- Every thread should appear at least once every 2-4 chapters (even as a reminder, rumor, symbol, or consequence).
- Mark chapters where the thread is: **I** (introduced), **D** (developed), **P** (paid off), **S** (seed/foreshadow).

## Core threads

### [Thread Name]
- Question: [what the reader wonders about this thread]
- I: [chapter]
- D: [chapters]
- S: [chapters]
- P: [chapter or "Book X"]
```

---

### `19-foreshadowing-checklist.md`

```markdown
# Foreshadowing Checklist

Track seeds planted and their intended payoffs so nothing is dropped and nothing feels invented at the last minute.

## [Category Name] seeds ([Book/Act] payoffs)
- [What to seed]: [status — planted in ChNN / not yet planted]
  - Payoff target: [when this should pay off]

## [Category Name] seeds
- [What to seed]: [status]
  - Payoff target: [target]
```

---

### `25-style-guide.md`

```markdown
# Style Guide

Use this as the drafting north-star so tone stays consistent.

## Prose register
- Default voice: [plain/literary/lyrical — describe the target readability]
- [Specific prose guidance]

## Length targets
- Default chapter length: [word range]
- Prologue/epilogue: [word range]
- Capstone/climax chapters: [guidance]

## POV and tense
- [First/third person, past/present tense]
- [Head-hopping rules]
- [Interior thought style]

## Dialogue
- [Dialogue philosophy — pressure scenes, subtext, etc.]

## "Lived-In" checklist (apply per chapter)
- Include 2-3 texture beats that are not plot turns
- Show the setting's daily function
- Add at least 1 small supporting character motive
- Use consequence glue: decisions → immediate effects
- Vary sentence starts

## Humor
- [Style and boundaries]

## Violence
- [Approach and limits]

## Magic / Supernatural
- [Level and presentation rules]
```

---

### `AGENTS.md`

```markdown
# AGENTS.md — Writing Agent Instructions

You are a writing agent responsible for generating a cohesive long-form narrative in this repo.

## Defaults (unless user overrides)
- POV/tense: [default]
- Tone: [default]
- Writing style guide: `docs/25-style-guide.md`

## Repo workflow
- Canon/source-of-truth: `docs/07-continuity.md` (facts we must not break).
- Planning/bible: `docs/00-pitch.md`, `docs/02-world.md`, `docs/03-characters.md`, `docs/04-outline.md`, `docs/05-glossary.md`.
- Voice: `docs/08-voice.md` (authorial consciousness layer + character voice profiles).
- Scene ledger: after each drafted scene/chapter, update `docs/06-scene-log.md` with new facts + loose threads.
- Outlines: store chapter outlines in `outlines/book-one/` (and later `outlines/book-two/`, etc.).
- Draft output: write narrative chapters in `draft/book-one/` (and later `draft/book-two/`, etc.) as Markdown.

## Decision rules
- If canon conflicts with draft, update the draft to match canon (unless user explicitly chooses a retcon).
- You may invent names/places/terms as needed; immediately record them in `docs/05-glossary.md` and any permanent facts in `docs/07-continuity.md`.
- Keep continuity tight: no unexplained POV-hopping; avoid "omniscient" knowledge outside the current POV character.

## Revision policy
- Prefer forward momentum. Only rewrite earlier draft files when continuity breaks or the user asks for a rewrite.

## Output sizing
- Default iteration size: ~1,000-2,500 words per new chapter/sequence unless user requests otherwise.
```
