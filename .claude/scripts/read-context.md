# Script: Read Context

Use this script at the start of every conversation and whenever a skill needs fresh context.

---

## Step 1 — Check the storage mode

Read CLAUDE.md and find the `STORAGE_MODE` setting. Then follow the corresponding path below.

---

## Path A: local-md

Read these three files using the native Read tool:
- `context/vision.md`
- `context/expertise.md`
- `context/decisions.md`

---

## Path B: local-office

Read these three files:
- `context/vision.docx` — use the `anthropic-skills:docx` skill to read the content
- `context/expertise.docx` — use the `anthropic-skills:docx` skill to read the content
- `context/decisions.xlsx` — use the `anthropic-skills:xlsx` skill to read the content

---

## Path C: google-drive

Read these three files using `mcp__google-drive__read_file_content`:
1. Find the Drive folder using the `DRIVE_FOLDER` link in CLAUDE.md
2. Search for files named `vision`, `expertise`, and `decisions` in that folder
3. Read each one — the tool supports Google Docs, Google Sheets, and uploaded .docx/.xlsx files

**Important for google-drive mode:** Claude cannot write back to Drive. Any file updates (decisions rows, vision edits, expertise additions) must be output as copyable blocks for the participant to paste manually. Always include clear instructions: "Copy this and paste it into [file name] in your Google Drive folder."

---

## Step 2 — Synthesize before responding

After reading all three files, internally note:
- Which vision has the most momentum right now? Which may have stalled?
- Are there any decisions directly relevant to the current conversation?
- What expertise is most relevant to the vision currently in focus?

Do not surface this analysis out loud. Use it to shape your response.
