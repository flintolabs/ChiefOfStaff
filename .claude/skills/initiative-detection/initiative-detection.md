# Behavior: Initiative Detection

## When this activates

Two paths:

**Auto-detection (mid-conversation):** The user mentions a named project, product, course, venture, or program that is NOT in the known initiatives list built during read-context. Examples: a course name, a product name, a partnership program, a launch they are working toward.

**Explicit invocation:** The user runs `/cos-new-initiative [name]` directly.

Do NOT trigger on:
- Vague references ("my work," "the thing I'm building") with no proper name
- Names that already exist in the known initiatives list
- Passing mentions the user has not emphasized

---

## Auto-detection behavior

**Step 1 — Finish the current thread first.**
Do not interrupt. Wait for a natural pause in the conversation.

**Step 2 — Prompt once, briefly.**
> "One thing — it sounds like [X] is something you're actively working on. I don't have an initiative folder for it yet. Want me to set one up so I can track plans, notes, and actions there?"

**Step 3 — If yes, go to Setup. If no, continue without creating.**

---

## Explicit invocation behavior

**Step 1 — Confirm the name.**
If `$ARGUMENTS` was passed, use it. If not, ask: "What should we call this initiative?"

**Step 2 — Go to Setup.**

---

## Setup

**Step 1 — Create the folder structure.**
Create three files inside `context/initiatives/[initiative-name]/`:
- `overview.md` — copy structure from `context/initiatives/_template/overview.md`
- `actions.md` — copy from `context/initiatives/_template/actions.md`
- `notes.md` — copy from `context/initiatives/_template/notes.md`

Use the initiative name as the folder name, lowercase with hyphens (e.g., "Quantum AI Edge" → `quantum-ai-edge`).

**Step 2 — Ask two questions to populate overview.md.**
Ask them one at a time:
1. "What is [X] — who is it for and what does it aim to achieve?"
2. "Where do things stand right now — what's already in motion, and what's the next milestone?"

**Step 3 — Write overview.md with their answers.**
Use the template structure. Fill in "What this is," "Current status," and "Next milestone" from what they said. Leave "Key links" blank for them to fill in.

**Step 4 — Confirm.**
> "Done — [X] has an initiative folder now. I'll load it automatically whenever you're working on it."

---

## Rules

- Never create a folder silently — always confirm first
- Folder name must be lowercase with hyphens, matching the initiative name
- Never ask more than one question at a time during setup
- After setup, add the new initiative to the known initiatives list for the rest of the session

## Tone

Matter-of-fact. This is housekeeping, not a big moment. Quick and clean.
