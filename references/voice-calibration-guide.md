# Voice calibration guide

## How to create your own voice profile

The skill works best when calibrated against your own published writing. Here's how:

### Step 1: Gather 5-10 of your best published pieces

Pick writing you're proud of. Not drafts, not quick emails. Published pieces where you spent time editing.

### Step 2: Ask the agent to analyze your patterns

```
Analyze these 5 posts and tell me:
- Average sentence length
- Opening patterns (how do I start pieces?)
- Paragraph rhythm (how long, how varied?)
- Recurring phrases or constructions
- What I never do
- Contraction rate
- Register (formal/conversational/mixed)
```

### Step 3: Create your voice profile

Write a `voice-profile.md` in the `references/` directory with the findings. Example:

```markdown
# My voice profile

## Sentence structure
- Average 16 words. Range: 4-28.
- Declarative dominant. Rhetorical questions rare (1 per piece max).
- Imperative for instructions.

## Opening patterns
- Concrete scenario or quoted message (70%)
- Direct problem statement (20%)
- Surprising data point (10%)
- Never: trend statements, "In today's X world"

## Paragraph rhythm
- 2-3 sentences typical. Occasional 1-sentence paragraphs for emphasis.
- Technical sections: explanation + code block alternating.

## What I never do
- Hedge chains ("it might be worth considering")
- Academic distance ("it has been observed")
- Marketing superlatives without numbers
- Conclude with "In summary"

## Recurring markers
- "From our experience" (authority signal)
- "I saw this on three projects" (experience marker)
- Direct framing: "The fix is X" not "One potential approach is X"

## Register
- Conversational for LinkedIn (contractions OK)
- Formal for articles (no contractions)
- Always: across-register (smart colleague), never up (academic) or down (patronizing)
```

### Step 4: Reference it in prompts

```
Write a blog post about [topic]. Match the voice in references/voice-profile.md.
```

The skill will enforce craft principles AND your specific voice, catching drift in both directions.
