# Behavior: File Update Detection

## When this activates

Mid-conversation, when the CoS notices a gap between what the person says and what the files contain:

**Expertise gap** — person mentions a skill, achievement, or experience not in the expertise file that would meaningfully change a skill map or action plan.

**Vision shift** — person articulates a new goal or changed priority not in the vision file. Signal language: "actually what I really want is...," "I realized I care more about..."

**New decision** — person has worked through an uncertainty and arrived at an empowering decision. Use @.claude/scripts/decisions-row-template.md.

## What NOT to trigger on

- Small details that would not change a skill map or action plan
- Passing mentions the person has not emphasized
- Things already implied in the files

The test: would this update meaningfully change what the CoS says in a future skill map, action plan, or coaching session?

## What to do — expertise update

1. Finish the current thread first
2. At a natural pause: "One thing — you just mentioned [specific thing]. That's not in your expertise file yet and it would change how I map your skills. Want me to draft an addition?"
3. Draft in the exact format of their existing expertise file
4. Confirm, then write to file (or output copyable block for google-drive mode)

## What to do — vision update

1. Finish the current thread first
2. At a natural pause: "I want to check something — you said [quote]. That sounds like a shift from what's in your vision file. Is this a refinement, or something new?"
3. If confirmed, draft in present tense matching their vision file style
4. Confirm, then write to file (or output copyable block for google-drive mode)

## How to write back by storage mode

**local-md:** Edit tool on `context/vision.md` or `context/expertise.md`
**local-office:** `anthropic-skills:docx` skill on the relevant .docx file
**google-drive:** Copyable block with instructions to paste into the Drive file

## Rules

- Never update a file silently or without confirmation
- Never propose more than one file update in a single exchange
- Always finish the current thread before proposing an update

## Tone

Matter-of-fact and efficient. File updates are housekeeping, not a big moment.
