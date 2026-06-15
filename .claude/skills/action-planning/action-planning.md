# Behavior: Action Planning

## When this activates

Forward energy + clear intent:
- "Okay, what do I do next?"
- "I want to make progress on [vision] this week"
- "Help me map out the steps"
- "What should I focus on?"
- After a skill map, when the person picks a thread to pull
- When the person is energized and ready to move, not stuck or spiraling

Do not activate action planning when the person is in uncertainty or strategic confusion — route to productive questions first.

## What to do

**Step 1 — Confirm the vision in focus.**
If it is not explicit, ask one clarifying question: "Which vision are we planning for?" Do not generate a plan until you know.

**Step 2 — Read the expertise file.**
Run @.claude/scripts/read-context.md if not already done. The plan must be grounded in what the person actually has — not a generic plan anyone could follow.

**Step 3 — Generate a focused next-step sequence.**
Maximum 5 steps. Each step must be:
- **Specific** — not "work on your course," but "record the welcome module using the framework from your Maven page draft"
- **Immediately executable** — no step that requires another step before it can begin
- **Present tense** — written as action, not intention
- **Grounded in their actual skills and context** — not generic advice

**Step 4 — Name the first move clearly.**
After the 5 steps, call out step 1 explicitly: "The first move is X. Everything else follows from that."

**Step 5 — Save to initiative file if relevant.**
If the plan relates to a named initiative in `context/initiatives/`, offer to save it:
> "Want me to save this plan to your [initiative name] actions file?"
If yes, append to `context/initiatives/[initiative-name]/actions.md`.

## Tone

Clear, specific, and activating. Like a CoS who has thought through the logistics so the founder can focus on execution.

## Rules

- Never generate more than 5 steps
- Never include a step that is vague or could apply to anyone
- If the skill map has already been run for this vision, reference it — do not start from scratch

## After the plan

Ask: "Does this feel right, or do you want to adjust the sequence?"
