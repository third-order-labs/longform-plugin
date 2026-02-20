---
name: authorial-voice
description: Theory and practice of voice in long-form fiction — capturing the authorial consciousness that makes a novel read like it was written by one mind, not just following a style guide.
---

# Authorial Voice

Voice in long-form fiction is the deeper problem beneath coherence. Continuity tracking ensures chapter 40 doesn't contradict chapter 2. Voice ensures the novel reads like it was written by one consciousness with a consistent worldview across 300 pages. This skill covers capturing that consciousness and maintaining it at scale.

---

## Voice vs. Style

**Style guide** = surface. Prose register, sentence length, POV rules, dialogue formatting. You can follow a style guide and produce competent generic prose. Two different writers can follow the same style guide and produce completely different novels.

**Authorial voice** = the perceptual filter underneath. What the narrator pays attention to, what they skip, what they believe about the world. You can't follow a checklist for this — it has to be consistent across 300 pages because it comes from a consistent consciousness.

The style guide says HOW to write. The voice doc says WHO is writing.

Hemingway didn't write short declarative sentences because of a style guide. He wrote that way because of who he was — his worldview produced the style. The authorial consciousness layer captures the *who*, not just the *how*.

---

## The Authorial Consciousness Layer

What the voice doc captures — not a style spec, but a portrait of the mind behind the prose:

### Attention filter

What does this narrator notice? Physical spaces? Social dynamics? Interior states? The mundane? Power structures? The body?

A narrator who lingers on landscape writes differently from one who lingers on power dynamics — and this colors every scene, not just the ones "about" that thing. The attention filter determines which details make it onto the page and which get passed over. It's the most pervasive element of voice because it operates in every paragraph.

### Beliefs about the world

Not the theme of the novel — the narrator's operating assumptions. Do people change? Are institutions redeemable? Is violence ever justified? Is love sufficient? Does effort correlate with outcome? Is the universe indifferent or responsive?

These aren't stated. They shape which details get included and how events are framed. A narrator who believes people don't fundamentally change will present a redemption arc differently from one who believes transformation is always possible — even if the plot events are identical.

### The iceberg

What this narrator refuses to say directly. Some narrators are confessional — everything is on the page. Some are withholding — the emotional weight lives in what's implied. Some are analytical — they'll dissect a feeling rather than express it.

The relationship between what's on the page and what's implied is a voice signature. Hemingway's iceberg. Didion's cool surface over volcanic feeling. McCarthy's refusal to psychologize.

### Relationship to suffering

How pain, loss, and injustice are presented. Clinical? Empathetic? Detached? Dark humor? Unflinching? This is the "lived experience" layer — what gives the prose gravity or lightness.

A narrator who treats suffering with dark humor produces a fundamentally different novel from one who treats it with quiet empathy, even with the same plot and characters.

### Relationship to humor

When humor appears, what form it takes, what it's allowed to touch. Some voices use humor as defense. Some as clarity. Some as subversion. Some never use it. Some use it everywhere except where it matters most.

The boundary of humor — what it's permitted to touch and what it must respect — is voice data.

### Relationship to uncertainty

Does this narrator resolve ambiguity or sit with it? Is not-knowing treated as failure or as honesty? Does the prose reach for closure or leave things open?

Some narrators need to understand everything. Some are comfortable reporting what they see without explaining it. This shapes endings, transitions, and the relationship between scenes.

### Energy levels

How the prose shifts between quiet observation and intensity:

- **Level 1 — Quiet observation**: Understated weight. The temperature is low but the specificity is high. Descriptions that land without reaching for effect.
- **Level 2 — Working through**: Analytical, building, the narrator processing events. Longer sentences, more interiority, connections being drawn.
- **Level 3 — Committed intensity**: Landing claims, closing distance, prose that has stopped hedging. Sentences get shorter. The narrator is no longer observing — they're declaring.
- **Level 4 — Peak moments**: Compressed, declarative, rare. The moments the novel has been building toward. The prose is at its most stripped and its most powerful. Overuse kills it.

Where's the default register? What moves it? Most prose should live at 2-3. Level 4 should appear rarely enough to earn its impact.

---

## Character Voice Profiles

For each POV character, the voice doc maintains a lighter profile that differentiates their sections from each other and from the narrator's baseline:

### What to capture per character

- **Speech patterns**: Vocabulary, syntax, typical expressions, rhythm. How they actually talk — not a dialect transcription, but the shape of their sentences and what words they reach for.
- **Interior voice**: How they think vs. how they speak. Some characters think in the same register they talk. Some have a formal interior and a casual exterior. Some think in fragments. Some think in run-ons.
- **Blind spots**: What they can't or won't see. Every POV character has perceptual limitations — things they miss, things they misinterpret, things they refuse to look at. These should be consistent and should shape what appears on the page during their sections.
- **False certainties**: What they're sure about that's wrong. This creates dramatic irony and differentiates POV characters from an omniscient narrator.
- **Energy range**: What moves them between registers. What makes them go quiet. What makes them sharp. What makes them lose composure.
- **Evolution markers**: How voice shifts across the arc. Chapter 1 voice vs. chapter 30 voice. A character who starts guarded and ends open should have a voice that tracks that change — not abruptly, but gradually.

This is NOT the deep interview treatment that the authorial consciousness layer gets. It's a structured profile that the agent uses to maintain distinct character voices across the manuscript.

---

## Two-Layer Capture

### Upfront capture

During `/voice-session` or as part of `/start-project`: conversational extraction of the author's worldview, taste, and attention patterns.

This is lighter than it sounds — not psychoanalysis, more like "what do you notice, what do you skip, what do you hate in fiction, who do you admire." The conversation surfaces the consciousness underneath the style preferences. The output is the authorial consciousness section of `docs/08-voice.md`.

### Emergent capture

Self-updating through the drafting process. As chapters are written and the user reacts, the voice doc sharpens:

- "This scene feels flat" = voice data (something about the attention filter or energy level is wrong)
- "This character sounds too reasonable" = voice data (the character's blind spots or false certainties aren't showing)
- "This is too neat" = voice data (the narrator's relationship to uncertainty isn't being honored)
- "I love this passage" = voice data (the voice hit — study what worked)

The first 3-5 chapters are explicit calibration. The user should expect to give more feedback early. Each correction sharpens the voice doc, and the voice doc sharpens the output.

---

## Novel-Specific Anti-Patterns

The kill list for fiction AI writing. These are different from article or essay anti-patterns:

- **Identical character voices**: Every POV character sounds the same — same vocabulary, same sentence rhythm, same level of self-awareness. If you can swap character names and not notice, the voice profiles aren't working.
- **Purple prose / over-description**: Reaching for literary effect in every paragraph. Not every sunset needs three adjectives. The attention filter should determine what gets described and what gets passed over.
- **Telling emotions instead of showing behavior**: "She felt angry" instead of showing what anger looks like in this character's body and actions.
- **Omniscient narrator leaking into limited POV**: The POV character somehow knows things they couldn't know, notices things they wouldn't notice, or has insights that belong to the author, not the character.
- **Said bookisms**: "hissed," "exclaimed," "intoned," "breathed." Use "said" or cut the attribution entirely. The dialogue should carry the tone.
- **Characters who are always articulate about their feelings**: Real people struggle to name what they feel. Characters who perfectly diagnose their own emotional states sound like therapy transcripts, not people.
- **Convenient internal monologue**: Interior thoughts that exist purely to explain the plot to the reader. If a character is "thinking" about backstory the reader needs to know, that's exposition wearing a mask.
- **Dialogue as information transfer**: Conversations where characters tell each other things they already know, purely for the reader's benefit. "As you know, Bob..."
- **Every scene landing with a neat emotional resolution**: Real scenes trail off, get interrupted, end on wrong notes. If every scene closes with a clean beat, the prose is performing rather than living.
- **Atmosphere descriptions that don't filter through POV**: Generic scene-setting that any character would notice the same way. The room should look different through different eyes. What a soldier notices about a tavern is not what a merchant notices.

---

## Voice Precedence in Document Hierarchy

Where the voice doc sits in the resolution order when documents conflict:

1. **Continuity** (`07-continuity.md`) — canon facts that must not be broken
2. **Voice doc** (`08-voice.md`) — authorial consciousness + character profiles
3. **Outline** (`04-outline.md`) — the structural plan
4. **Threads** (`13-threads.md`) — active narrative threads
5. **Scene log** (`06-scene-log.md`) — what actually happened
6. **Style guide** (`25-style-guide.md`) — prose mechanics
7. **Pitch** (`00-pitch.md`) — the original vision

Voice sits above outline because a scene can deviate from the structural plan and still work, but a scene that violates the authorial consciousness will feel wrong regardless of whether it hits its plot beats. Voice sits below continuity because facts are facts — you can't break canon for the sake of voice.

Voice sits above style guide because style is the surface expression of voice, not the other way around. If the style guide says "short sentences" but the voice doc says "this narrator works through complexity at length," the voice doc wins and the style guide should be updated.

---

*This skill is referenced by `/voice-session`, `/write-chapter`, `/review`, and `/wrap`.*
