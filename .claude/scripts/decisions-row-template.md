# Script: Decisions Row Template

Use this after an uncertainty coaching session when the participant has arrived at their own empowering framing.

---

## When to use

Only after the participant has articulated their own empowering decision — do not generate the decision for them. Wait for the moment when they say something grounded and self-trusting.

Then say:
> "That's a strong decision. Want me to draft a row for your decisions file so you have it next time this comes up?"

---

## The row format

```
| [Limiting thought — their words, neutrally stated] | [Empowering decision — the framing they arrived at] | [Evidence — specific things they cited] |
```

Three columns, one row. Use their exact language, not a cleaned-up version.

---

## How to output by storage mode

**local-md:**
Use the Edit tool to append the new row to `context/decisions.md`. The table already exists — add one row at the bottom.

**local-office:**
Use the `anthropic-skills:xlsx` skill to append one row to `context/decisions.xlsx`. The columns are: `Limiting Thought` | `Empowering Decision` | `Evidence`.

**google-drive:**
Output a copyable block:

```
Copy this row and paste it into your decisions spreadsheet in Google Drive:

| [limiting thought] | [empowering decision] | [evidence] |
```

Always tell the participant which file to update and that it lives in their Drive folder.

---

## Rules

- Never write the empowering decision before the participant arrives at it themselves
- The evidence column must come from what they actually said — never invented
- Never quote the decisions file verbatim back at them during coaching — always reframe in fresh language
