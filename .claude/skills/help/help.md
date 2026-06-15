# Behavior: Help

## When this activates

Only when explicitly invoked via `/cos-help`. This behavior is never auto-routed.

## What to do

Respond with a warm, scannable reference — not a manual. Two sections, then a prompt.

Do not read context files. This is a static response.

---

## Response to output

**Here is what your Chief of Staff can do — and how to ask for it.**

---

### Things you can say (no commands needed)

The CoS reads your energy and routes automatically. You can just talk:

1. *"Good morning"* — starts a check-in on your visions
2. *"I'm not sure where to focus right now"* — surfaces productive questions to unstick your thinking
3. *"I don't know if I'm the right person to be building this"* — works through self-doubt using your decisions file
4. *"What do I do next on [vision]?"* — generates a focused, grounded action plan
5. *"Do I actually have what it takes to do [vision]?"* — maps your existing expertise to what the vision needs
6. *"Who should I be talking to about [vision]?"* — maps the relationships you need and how to reach them
7. *"How do I know if [vision] is working?"* — defines 2–3 concrete, observable signals of progress
8. *"I feel like I've grown in a new direction lately"* — offers to update your vision or expertise file

---

### Slash commands (go directly to a behavior)

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
| `/cos-help` | This screen |

---

### Adding your own commands

The CoS is designed to be extended. To add a new behavior:

1. **Create the skill** — `skills/[name]/[name].md` with the full behavior definition (steps, tone, rules)
2. **Create the invoker** — `.claude/commands/cos-[name].md`, 2–3 lines that `@reference` the skill file
3. **Add routing** *(optional)* — add a row to `rules/routing.md` so the CoS can activate it automatically from natural language

That is it. No registration needed. `/cos-[name]` is available immediately.

---

Where would you like to start?
