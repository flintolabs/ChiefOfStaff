# Chief of Staff

Your personal strategic adviser in Claude Code. It reads your vision, your expertise, and your past decisions — and uses them to give you grounded, specific coaching and planning every session.

---

## Before you start — pick a storage mode

Your CoS needs to read three files about you: your **vision**, your **expertise**, and your **decisions**. You choose where those files live.

Open `CLAUDE.md` and find this line near the top:

```
STORAGE_MODE: local-office
```

Change it to whichever mode fits you:

| Mode | Your files | Write-back |
|---|---|---|
| `local-office` | `context/vision.docx`, `context/expertise.docx`, `context/decisions.xlsx` | ✓ CoS can update them automatically |
| `local-md` | `context/vision.md`, `context/expertise.md`, `context/decisions.md` | ✓ CoS can update them automatically |
| `google-drive` | Your existing Google Drive folder | Read-only — CoS gives you text to paste |

**Recommended for most people: `local-office`** — familiar file formats, full read and write.

---

## Setup for each mode

### local-office (Word + Excel)

Files are already created for you in the `context/` folder. Open each one and fill it in:

1. **`context/vision.docx`** — Write your visions in present tense, as if already achieved. One heading per vision.
2. **`context/expertise.docx`** — Describe your skills, background, and domain knowledge. One heading per area.
3. **`context/decisions.xlsx`** — Fill in the three columns: what the limiting thought is, what decision you made about it, and what evidence supports that decision. Start with 2–3 rows.

### local-md (Markdown)

Same three files, plain text format:

1. **`context/vision.md`**
2. **`context/expertise.md`**
3. **`context/decisions.md`**

Open each file — instructions are inside.

### google-drive

1. Connect Google Drive to Claude Code: go to **Settings → Connections** and toggle on Google Drive
2. In `CLAUDE.md`, uncomment the `DRIVE_FOLDER` line and paste your Google Drive folder link:
   ```
   DRIVE_FOLDER: [paste your folder link here]
   ```
3. Your Drive folder should contain your `vision`, `expertise`, and `decisions` files

> **Note:** In google-drive mode, your CoS can read your files but cannot write back to them. After coaching sessions, it will give you a formatted row to copy and paste into your decisions spreadsheet manually.

---

## How to use your CoS

### Just talk to it

Open a new session in this project and say anything. Your CoS reads your files at the start of every conversation and responds to wherever you are.

```
good morning
```
```
I'm feeling stuck on my university partnership strategy
```
```
I don't know if I'm the right person to be building this
```

It will route to the right behavior automatically — no commands needed.

### Or use a slash command to go directly to a behavior

Type `/cos` to see all available commands:

| Command | What it does |
|---|---|
| `/cos-morning` | Morning briefing — check in on your visions |
| `/cos-plan [vision]` | Action plan — up to 5 specific next steps |
| `/cos-map-skills [vision]` | Skill map — how your expertise connects to a vision |
| `/cos-coach` | Uncertainty coaching — work through self-doubt |
| `/cos-questions` | Productive questions — reframe a strategic sticking point |
| `/cos-network [vision]` | Network map — who you need and how to reach them |
| `/cos-metrics [vision]` | Metrics — 2–3 concrete signals to track progress |
| `/cos-update-files` | Capture any skill or vision updates from this session |
| `/cos-help` | Show example questions and all available commands |

---

## How to add an initiative

When you are working on a specific initiative (a course launch, a partnership program, a product), you can give it its own folder so your CoS can save plans and notes there.

1. Copy the template folder:
   ```
   context/initiatives/_template/  →  context/initiatives/your-initiative-name/
   ```
2. Open `overview.md` and fill in what the initiative is and where things stand
3. Reference it in conversation: `/cos-plan your-initiative-name`

Your CoS will save action plans to `actions.md` and running notes to `notes.md` inside that folder.

---

## Keeping your files current

Your CoS is only as good as what's in your files.

- **Update your vision file** when your goals shift or clarify
- **Update your expertise file** when you complete a significant project or step into a new role
- **Update your decisions file** after any session where you work through doubt and arrive at a stronger position — your CoS will draft the row for you at the end of the session

Your CoS will notice when something you mention isn't in your files yet and offer to add it.
