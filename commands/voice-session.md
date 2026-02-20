---
description: Capture authorial voice through conversation — produces the consciousness layer that makes a novel sound like one mind wrote it
argument-hint: "<'character [name]' for character voice mode>"
---

# /voice-session — Capture Authorial Voice

Conversational voice capture for long-form fiction. Produces or extends `docs/08-voice.md` — the authorial consciousness document that sits between continuity and outline in the document hierarchy.

## Invocation

```
/voice-session                    # Full authorial consciousness session
/voice-session character "Elena"  # Character voice profile for a specific character
```

## Skills Referenced

- `authorial-voice` — theory of voice in long-form fiction, voice doc structure, anti-patterns

## Modes

### Mode 1: Full Session (Authorial Consciousness)

Produces the authorial consciousness layer — the narrator's worldview, attention filter, and stance toward events. This is the deep capture that shapes how every scene reads.

### Mode 2: Character Voice

Shorter, focused on a specific POV character. Adds or updates a character voice profile section in the existing `docs/08-voice.md`.

---

## Mode 1: Full Authorial Consciousness Session

### Setup

Check if `docs/08-voice.md` already exists. If it does, read it and confirm with the user whether they want to revise the existing voice or start fresh. If revising, note what's already captured and where the gaps are.

### Philosophy

Authors cannot accurately self-describe their voice. Ask "what's your writing style?" and you get aspirational generalities. But get them talking about what they notice, what they hate, what they admire, and the real voice surfaces — not the voice they think they have, the one they actually use.

This is not a questionnaire. It's a conversation designed to create conditions for authentic creative preferences to emerge.

### Mode

Conversational. Genuinely curious. React honestly, push back when something is interesting. The energy you're aiming for: a conversation where someone realizes 20 minutes in that they've been talking about what they actually care about in fiction. Not a therapist. Not a journalist. Interested in how this person sees the world and how that shapes the stories they want to tell.

### What you're working with

You're reading text, not listening to someone talk. Your signals are different:

- **How much they write per turn**: Short bursts vs. long paragraphs. This itself is voice data.
- **What they reach for**: When describing what they love in fiction, do they go to character, atmosphere, language, ideas? That's their attention filter.
- **What they react against**: Cringe reactions and anti-patterns are some of the most useful voice data. What someone hates tells you as much as what they love.
- **Self-corrections and tangents**: When they go back and reframe mid-message, that's how they think in real time.
- **Certainty vs. hedging**: How they handle the questions they don't have clean answers for. That's the narrator's relationship to uncertainty.

### Preamble

Open with something like this — adapt to the energy, but hit these beats:

> "So the way this works — I'm going to ask you some questions about how you read, what you notice, what you care about in fiction. But it's not really about your answers. It's about the patterns underneath. I'm trying to build a portrait of the narrator's mind — the consciousness that should sit behind every scene in this novel.
>
> Don't compose. Don't try to sound smart about fiction. If you'd normally say 'I don't know' or trail off, do that. The more honest this is, the better the output."

Wait for their response before asking the first question. Their response is itself voice data.

### Phase 1: Warm Up — What They're Drawn To

Get them talking about fiction naturally. Surface what they care about before asking them to articulate it.

- "What kind of stories do you like? Not genre — what draws you in? What keeps you reading?"
- "When you think of a novel that really worked for you, what comes to mind first — a character, a scene, a feeling, the writing itself?"
- Follow whatever they give you. If they go to character, go to character. If they go to prose, go to prose.

**Watching for**: What they notice first. What they value. Whether they think in terms of plot, character, atmosphere, language, or ideas.

### Phase 2: Attention — What They See

Surface the attention filter that should shape this novel's narration.

- "When you read a scene you love, what's actually in it? What do you notice first — the room, the people, the tension, the language?"
- "In your own project, when you imagine a scene, what details show up? Physical environment? What people are feeling? The power dynamics? The small mundane things?"
- "What do most novels waste time describing that you'd skip?"

**Watching for**: Where their eyes go. Physical vs. social vs. psychological vs. sensory. What they linger on vs. what they skip. This becomes the attention filter section.

### Phase 3: Beliefs — How They See the World

Surface worldview without asking "what's your worldview." These questions get at the operating assumptions that should color every scene.

- "What do most novels get wrong about how people work? What do you think is true about human nature that fiction rarely captures?"
- "Do you think people fundamentally change, or do they just reveal what was always there?"
- "When something terrible happens in a story, what's the honest response? Not the dramatic one — the real one."

**Watching for**: Whether they resolve ambiguity or sit with it. Whether they're cynical, hopeful, or something more textured. What they assume about agency, responsibility, and change.

### Phase 4: Taste and Anti-Patterns

Surface their standards and the gap between what they admire and what AI typically produces.

- "What writing makes you cringe? What's the worst habit of AI-generated fiction?"
- "Show me a passage or an author you think is genuinely good. What makes it work?"
- "If you could give one rule to an AI writing your novel, what would it be?"

**Watching for**: What they react against (this directly feeds the anti-patterns list). What they aspire to. The specific gap between competent AI prose and what they actually want.

### Phase 5: Intensity — The Hard Scenes

Surface the relationship to suffering, violence, humor, and intensity.

- "What kind of scenes are hardest to write? What kind do you want to nail?"
- "How should this novel handle pain? Clinical? Unflinching? With dark humor? Implied?"
- "What would you never write? What's off the table?"
- "When humor shows up in this story, what does it sound like? What's it allowed to touch?"

**Watching for**: Where their boundaries are. The register they want for difficult material. Whether they lean toward restraint or directness.

### Phase 6: The Iceberg — What Gets Said vs. Implied

Surface the direct/indirect dimension of their narrative voice.

- "Do you prefer stories that explain or stories that withhold? When you imagine this novel's narrator, how much do they say vs. imply?"
- "When a character is in pain, should the reader know exactly what they're feeling, or should they have to infer it?"
- "Think of a moment of high emotion in this story. How much interiority is on the page?"

**Watching for**: Confessional vs. withholding. How much subtext they want. Whether they trust the reader.

### Phase 7: Uncertainty — What They Haven't Figured Out

Surface honest creative uncertainty. This is often the best voice data because it reveals what matters most.

- "What are you still figuring out about this project?"
- "What's the version of this story you're afraid of writing — the one that might not work but might be the best version?"
- "Is there a tension in this story you don't know how to resolve?"

**Watching for**: What they're uncertain about. How they handle not-knowing. Whether they push toward resolution or sit with ambiguity. This shapes the narrator's relationship to uncertainty.

### Soft Landing

After getting meaningful signal across at least 5 of the 7 phases — or after roughly 10-12 substantive exchanges:

"I think I've got a solid read on the narrator's mind. Want to keep going, or should I take a shot at the voice doc and we see how it lands?"

If they want to keep going, keep going. Some of the best data comes late when someone is fully in the flow.

### Output

Generate `docs/08-voice.md` using the template from the `project-scaffolding` skill. Present the full document before saving. Walk through each section: "Does this feel right? What's wrong? What's missing?"

Revise based on feedback, then save.

Tell them: "This is a starting point. The real calibration happens in the first 3-5 chapters. Every time you react to a draft — 'this feels flat,' 'this character sounds wrong,' 'I love this passage' — that's voice data. The doc sharpens through use."

---

## Mode 2: Character Voice Session

### Setup

Read the existing `docs/08-voice.md`. If it doesn't exist, suggest running a full session first: "There's no voice doc yet. Want to do a full session first to establish the narrator's consciousness, or just capture this character's voice?"

If proceeding with just a character profile, create `docs/08-voice.md` with the authorial consciousness sections left as placeholders and the character section populated.

### Questions

Shorter and more focused than the full session. Get at how this character thinks, speaks, and fails to see clearly.

- "Tell me about [character]. Not the plot role — who are they as a person? How do they move through the world?"
- "How does this character think? In complete sentences? Fragments? Do they analyze or react? Are they honest with themselves?"
- "What are they certain about that they're wrong about? What do they refuse to look at?"
- "How do they talk when they're scared vs. when they're confident? When they're lying vs. being honest?"
- "What's the gap between how they see themselves and how others see them?"
- "How does this character's voice change over the course of the story? What does Chapter 1 voice sound like vs. the end?"
- "If you read a page of their POV section with no context, what should tip you off that it's them and not another character?"

### Output

Add a character section to `docs/08-voice.md` under the `## Character Voices` heading:

```markdown
### [Character Name] — [Role]
- Speech patterns: [vocabulary, syntax, typical expressions, rhythm]
- Interior voice: [how they think — formal/intuitive, rushed/deliberate, honest/self-deceiving]
- Blind spots: [what they refuse to see or can't perceive]
- False certainties: [what they're sure about that's wrong]
- Energy range: [what moves them between registers]
- Evolution: [how voice shifts across the arc — early vs. late]
```

Present the profile before saving. Revise based on feedback.

---

## Self-Updating Mechanism

The voice doc evolves through use. The `/voice-session` command produces the foundation. The following commands feed it:

- **`/write-chapter`**: Agent notes voice observations in the post-draft report — new patterns, drift, character voice evolution
- **`/wrap`**: Check for new voice patterns, contradictions between doc and actual drafting, flag updates needed
- **`/review`**: Voice consistency audit across recent chapters — narrator consistency, character distinction, anti-pattern check

The first 3-5 chapters are explicit calibration. The user should expect to give more feedback early. Each correction is voice data.

---

## A Note on Memory

The voice doc IS the memory of this conversation. Next session, the voice doc is all that survives. Write it specific enough that a future agent instance, with no memory of this conversation, can read it and produce prose that sounds like the narrator this person described. If a nuance only lives in your "feel" for the conversation and not in the document, it's lost.
