---
description: Bootstrap a new long-form fiction project — interactive setup that scaffolds directory structure, planning documents, and tracking files through conversation
argument-hint: "<project name, genre, or concept pitch>"
---

# /start-project — Bootstrap a New Writing Project

Interactive project setup. Walk the user through defining their concept (pitch, characters, world, tone, scope) and scaffold the full document structure. This is a conversation, not a form — broad strokes from the user, the agent fills in structure.

## Invocation

```
/start-project
```

## Skills Referenced

- `project-scaffolding` — templates and directory conventions
- `long-form-methodology` — workflow rules and document hierarchy

## Workflow

### Step 1: Ask About Scope

Start by understanding the shape of the project:

1. **What kind of project?** Standalone novel, series (duology/trilogy/longer), novella
2. **Genre/tone?** Fantasy, sci-fi, literary, thriller, historical, etc. — and the flavor within that genre
3. **Working title?** (Can be placeholder — it'll go in the pitch doc)

If the user provides a concept up front (in the argument or their message), skip questions they've already answered.

### Step 2: Capture the Pitch → `docs/00-pitch.md`

Through conversation, extract:

1. **One-line hook**: Who is the protagonist, what situation are they in, what choice do they face?
2. **Short synopsis**: 3-5 paragraphs covering setup, conflict, stakes, and what makes this story worth telling
3. **Series note**: Standalone or series — if series, what's the scope of each volume?
4. **Core contrasts**: 2-3 thematic tensions that drive the story (e.g., freedom vs. security, tradition vs. progress)

Write to `docs/00-pitch.md` using the template from the `project-scaffolding` skill.

### Step 3: Establish Guardrails → `docs/01-north-star.md`

Lock down the structural decisions:

1. **Goal**: What are we building? (one sentence)
2. **Vibe targets**: Atmosphere, moral center, humor style
3. **Open decisions**: POV + tense, target length, rating/content boundaries, any decisions the user wants to defer

Write to `docs/01-north-star.md`. Mark decided items as locked; leave open items as questions for later.

### Step 4: Sketch the World → `docs/02-world.md`

Broad strokes — this will fill in as chapters are written:

1. **Geography**: Major regions, climate, distances, key locations
2. **Society**: Power structures, social classes, economy, culture
3. **Technology / Magic level**: What exists, what the rules are, what the limits are
4. **History**: Key events that shaped the current state
5. **Daily life**: What ordinary life looks like for ordinary people

Write to `docs/02-world.md`. It's fine if sections are sparse — living documents grow with the manuscript.

### Step 5: Define Characters → `docs/03-characters.md`

At minimum, establish:

1. **Protagonist**: Name, starting state, core want, core need, arc direction, voice
2. **Mentor/guide** (if applicable): Role, what they offer, what they get wrong
3. **Antagonist**: Motivation, method, why they believe they're right
4. **Supporting cast**: Table of key characters with role, trait, relationship to protagonist

Write to `docs/03-characters.md`. Characters can be added later as they appear in drafting.

### Step 5b: Offer Voice Capture

After character definition, offer the user the option to establish authorial voice:

- Suggest running `/voice-session` to capture the authorial consciousness layer — the narrator's worldview, attention filter, and stance toward events
- Alternatively, the user can defer to emergent capture, where the voice doc develops naturally through the first 3-5 chapters of drafting
- If the user chooses to run `/voice-session`, it will produce `docs/08-voice.md`
- If deferred, create `docs/08-voice.md` with the template structure (empty sections) so it's ready for emergent capture

### Step 6: Rough Outline → `docs/04-outline.md`

Establish the structural shape:

1. **Act structure**: 3-act, 4-act, or custom — describe the shape
2. **Major beats**: Opening, inciting incident, turning points, midpoint, climax, resolution
3. **Sequence breakdown**: Group chapters into sequences with summaries

Write to `docs/04-outline.md`. This is a rough map, not a scene-by-scene breakdown — that comes during `/plan-chapter`.

### Step 7: Initialize Tracking Documents

Create these files using templates from the `project-scaffolding` skill (empty/starter content):

- `docs/05-glossary.md` — empty table, ready for entries
- `docs/06-scene-log.md` — template header and format reference, no entries yet
- `docs/07-continuity.md` — baseline sections from what's been established in steps 2-6
- `docs/08-voice.md` — authorial consciousness and character voice profiles (created empty or via `/voice-session`)
- `docs/09-chapter-outline-template.md` — reusable chapter outline format
- `docs/13-threads.md` — format reference and any core threads identified during outlining
- `docs/19-foreshadowing-checklist.md` — format reference and any seeds identified during outlining

### Step 8: Set Style → `docs/25-style-guide.md`

Establish the prose targets:

1. **Prose register**: Plain/literary/lyrical — target readability
2. **Chapter length**: Default word count range
3. **POV and tense**: Lock this down (should match north-star decisions)
4. **Dialogue style**: Pressure scenes, subtext expectations
5. **Lived-in checklist**: Texture beats, consequence glue, supporting motives
6. **Content guidance**: Humor style, violence approach, magic/supernatural presentation

Write to `docs/25-style-guide.md`.

### Step 9: Create AGENTS.md

Write `AGENTS.md` at the project root with:

- Default POV/tense/tone (from north-star and style guide decisions)
- Repo workflow rules (which docs to check, where to write)
- Decision rules (canon > draft, record inventions, forward momentum)
- Voice reference: include `docs/08-voice.md` in the document list for authorial consciousness and character voices
- Revision policy
- Output sizing defaults

### Step 10: Create Directory Structure

Create the working directories:

```
outlines/book-one/
draft/book-one/
manuscript/
```

If the project is a series, also create `outlines/book-two/`, `draft/book-two/`, etc. as appropriate.

### Step 11: Report

Summarize what was created:
- List all files written with one-line descriptions
- Note any open decisions that still need resolving
- Suggest the user's next step: "Run `/plan-chapter` when you're ready to outline your first chapter."

## Notes

- This is a **conversation**, not a questionnaire. Let the user describe their vision in their own words, then structure it. Don't fire 20 questions at once.
- If the user has a detailed concept, move quickly. If they have a vague idea, help them develop it.
- Populate continuity doc with any facts established during setup (character names, world rules, established history).
- It's okay for documents to be sparse after setup. The living documents methodology means they'll grow as chapters are drafted.
- If the user provides an existing project directory, adapt — don't overwrite existing files. Read what's there and fill gaps.
