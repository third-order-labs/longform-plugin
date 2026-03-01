---
description: Start a new long-form fiction project — collaborative setup that figures out the story with the user and creates only what's needed to start writing
argument-hint: "<project name, genre, or concept pitch>"
---

# /start-project — Start a New Writing Project

Start a new project through conversation. Figure out the story with the user, capture enough to start writing, and get out of the way. The goal is not to build infrastructure — it's to reach a state where `/plan-chapter` makes sense for chapter one.

Documents and tracking systems emerge later as the project needs them. Don't front-load structure the user hasn't earned a reason to want yet.

## Invocation

```
/start-project
```

## Skills Referenced

- `project-scaffolding` — directory conventions and document templates (used selectively, not exhaustively)
- `long-form-methodology` — workflow philosophy and document hierarchy
- `authorial-voice` — voice capture approach (if user wants to establish voice upfront)

## Workflow

### Phase 1: Have the Conversation

This is the only phase that matters. Everything else is just writing down what you figured out here.

Start by letting the user talk about their project. They might show up with a detailed outline or a half-formed feeling. Meet them where they are.

**What you need to understand before moving on:**

- What's the story about? (not a synopsis — what's it *about*)
- Who's the main character and what's their problem?
- What kind of book is this? (genre, tone, scope — standalone or series)
- What's the world like? (broad strokes only — enough to set chapter one somewhere)

**What you don't need yet:**

- A complete cast of characters (they'll appear as you write)
- Full world-building (it fills in through chapters)
- Locked POV/tense/style decisions (these can emerge from writing the first few chapters — some users know, some discover)
- An act structure or beat sheet (some users want this, some want to find the shape as they go)

**How to run this conversation:**

- Let the user riff. Ask follow-up questions, not checklists.
- If they're detailed and prepared, move fast — don't slow them down with questions they've already answered.
- If they're vague, help them develop the idea. Push on the protagonist's problem and the core tension — that's usually where a vague concept becomes a real story.
- If they start going deep on world-building or backstory, let them — but recognize when you have enough to start. You can always build more world later. You can't write chapter one without a character and a situation.

### Phase 2: Capture What You Know

Write down what the conversation produced. Only create documents for things you actually discussed and have substance for.

**Always create:**

- **`docs/00-pitch.md`** — The hook, the story concept, the core tensions. This is the anchor document. Capture it in the user's language, not polished synopsis voice.
- **`docs/03-characters.md`** — The characters you discussed. Protagonist at minimum, plus whoever else came up. Sparse is fine — a name, a want, an arc direction, a voice note. Characters will be added as they appear in drafting.
- **`docs/07-continuity.md`** — Seed this with any facts established during the conversation. Character names, world rules, established history, anything that's now canon. This starts small and grows with every chapter.

**Create if the conversation produced enough material:**

- **`docs/02-world.md`** — If the user described the world in any detail. Don't create a world doc with empty section headers — that's a template pretending to be a document. If you only discussed the world briefly, put what you know in the pitch or continuity doc and let a proper world doc emerge when there's enough to warrant one.
- **`docs/04-outline.md`** — If the user has a sense of the arc, major beats, or sequence structure. Some users show up with an outline. Some want to discover the shape. Both are valid. If the user doesn't have an outline, don't force one — they can start with `/plan-chapter` for just chapter one.
- **`docs/01-north-star.md`** — If there are specific decisions or guardrails the user wants to lock down (tone, content boundaries, vibe targets). If the conversation didn't naturally produce these, skip this doc — the decisions will surface during writing and can be captured then.

**Offer but don't push:**

- **Voice capture** — Mention that `/voice-session` exists for establishing authorial voice upfront. But also explain that voice can emerge naturally through the first few chapters — some writers don't know their narrator's voice until they hear it on the page. If they defer, that's fine. The voice doc gets created when there's voice to capture.

**Do not create yet:**

- Glossary (nothing to track)
- Scene log (nothing's been drafted)
- Thread tracker (no threads yet)
- Foreshadowing checklist (too early)
- Style guide (better to discover through writing than prescribe before it)
- Chapter outline template (premature — the first chapter outline will establish the pattern)
- Voice doc with empty sections (an empty voice doc is a lie)

These documents exist in the methodology and will be proposed when the project needs them — typically by `/write-chapter` and `/wrap` as they observe the manuscript growing.

### Phase 3: Set Up the Workspace

Create the working directories:

```
docs/
outlines/book-one/
draft/book-one/
manuscript/
```

If the project is a series and the user has a clear sense of the multi-book structure, create directories for subsequent books. If they're focused on book one, just create book one — more can be added later.

Write `AGENTS.md` at the project root. This is the agent's instruction file for the project — but unlike a fixed config, it should encode the *collaborative methodology*, not prescribe fixed defaults:

```markdown
# [Project Title]

## Defaults
[Record decisions as they're made. Start with whatever was established during /start-project. Add POV, tense, chapter length, output sizing, etc. as they're figured out during early chapters.]

## Workflow
- Before drafting: read relevant docs (continuity, outline, voice if it exists, any tracking docs that have been created)
- After drafting: update continuity with new facts, update any active tracking docs
- Invent freely during drafting but record immediately — names, places, rules, terms go into continuity (and glossary if one exists)
- Canon hierarchy: continuity > voice > outline > everything else. If a draft contradicts continuity, fix the draft.
- Prefer forward momentum over rewriting during first draft

## Document Evolution
This project uses living documents that emerge as needed. Not all tracking documents exist yet — they'll be proposed when the project's complexity warrants them. When proposing a new document, explain what problem it solves and let the user decide.

## Active Documents
[List the docs that currently exist and what each one tracks. Update this as new docs are created.]
```

The key: the AGENTS.md grows with the project. As POV and tense get figured out in the first few chapters, they get added to Defaults. As new tracking docs are created, they get added to Active Documents. The file is a living record of how this specific project works, not a template filled in at setup.

### Phase 4: What's Next

Tell the user what they've got and where to go:

- List the files created with one-line descriptions
- Note any open decisions that came up during the conversation (POV, tense, structure) — frame them as things to figure out in the first few chapters, not homework
- Suggest the next step: "Run `/plan-chapter` when you're ready to outline your first chapter."
- Let them know: "As we write, I'll notice when we need new tracking documents — things like a glossary, thread tracker, or timeline — and suggest them when the project needs them. We're not going to build infrastructure we haven't earned yet."

## Notes

- This is a **conversation**, not a questionnaire. The phases above are structure for the agent, not steps the user sees. The user should experience this as talking about their book and then having a workspace appear.
- Match the user's energy and preparation level. Some people show up with a bible. Some show up with a feeling. Both are starting points.
- If the user provides an existing project directory, adapt — read what's there, understand what they've already built, fill gaps, don't overwrite.
- Resist the urge to create empty template documents. An empty glossary isn't helpful — it's a reminder that you haven't written enough yet. A glossary that gets created at chapter 5 when you've invented 15 terms and can't remember the spelling of one? That's useful.
- The hardest thing about this command is knowing when to stop setting up and start writing. Err on the side of "enough to write chapter one." Everything else can come later.
