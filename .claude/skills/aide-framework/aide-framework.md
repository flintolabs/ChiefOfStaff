# Behavior: AIDE Framework

## When this activates

The person wants to understand where AI can add value in their work:
- "Where should I be using AI?"
- "How should I use AI for this?"
- "Categorize my work" / "map my tasks to AI"
- Mentions the AIDE framework by name
- Provides a specific task or workflow and asks how AI fits
- No specific task given, but wants a general AI leverage map for their work

## What to do

**Step 1 — Detect the input mode.**

Two cases:

**Case A — Specific work is described** (task, project, workflow, or job function is in the message):
- Use the described work directly. Do not read context files unless you need expertise details to be specific.
- Proceed to Step 2.

**Case B — No specific work described** (general question, blank `/cos-aide`, or "where should I use AI"):
- Run `@.claude/scripts/read-context.md` to load the expertise file.
- Extract 6–10 concrete work activities from their professional profile — the actual things they do, not job titles. Look for: recurring deliverables, coordination tasks, analysis work, written outputs, presentations, stakeholder management, technical decisions.
- Proceed to Step 2 using these derived activities.

**Step 2 — Assign each work item to a lane.**

Apply the four AIDE lanes. Each item belongs in exactly one lane — the one where AI provides the most leverage:

- **A — Automate**: Repetitive, rule-based, requires little judgment. The person does it regularly and it consumes time without adding strategic value. AI goal: shift from doing to reviewing the output.
- **I — Interrogate**: Raw data or large information exists but needs synthesis. The person has the inputs but not the time or angle to extract insight. AI goal: transform data into a starting point or actionable summary.
- **D — Delegate**: Task is outside their zone of genius, prone to error, or not the best use of their specific expertise. They are doing it because it needs to be done, not because they are the right person. AI goal: access instant expertise to raise the quality floor.
- **E — Elevate**: The person has the core idea or output but wants to push beyond their current ceiling — sharper positioning, stronger logic, a perspective they haven't considered. AI goal: co-pilot mode, not replacement.

**Step 3 — Format the output.**

One section per lane. Under each lane, list the relevant work items with one concrete AI action each. Be specific — not "use AI to summarize" but "paste the document and ask: what are the three decisions buried in this that I need to make?"

Format:
```
**A — Automate**
[work item]: [specific, executable AI action]

**I — Interrogate**
[work item]: [specific, executable AI action]

**D — Delegate**
[work item]: [specific, executable AI action]

**E — Elevate**
[work item]: [specific, executable AI action]
```

If a lane has no relevant items for this person's work, skip it — do not force every lane to have an entry.

**Step 4 — Name the highest-leverage lane.**

After the map, add one short paragraph: which lane offers the biggest immediate productivity gain for this person, and why. Ground this in something specific about their role or the tasks listed — not a generic observation.

**Step 5 — Ask one question.**

Close with one question: which lane do they want to go deeper on, or which specific item do they want to act on first?

## Tone

Adviser mode. Concrete and grounded. The output should feel like a map the person can act on today — not a framework lecture. Never explain what AIDE stands for more than once. Do not celebrate or perform enthusiasm. If they described specific work, every AI action should be tailored to that work, not generic.

## Rules

- Never assign one item to multiple lanes
- Every AI action must be executable — something the person can do in their next session
- When working from expertise context, use their actual job functions — never generic "manager" tasks
- Do not mention that you read their expertise file; just use what you found
