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

---

## Step 3 — Index known initiatives

List the contents of `context/initiatives/` using the Glob tool or directory listing. Exclude `_template/`. Note the initiative names internally as the **known initiatives list** for this session.

Do not read any initiative files yet — this is a lightweight index only.

Example internal note: *"Known initiatives: quantum-ai-edge, flintolabs-university"*

This list is used by two behaviors:
- **Initiative detection** — to notice when the user mentions a project not yet tracked
- **Context-aware reading** — to load the right initiative files when the user asks questions about known initiatives
