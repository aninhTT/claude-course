# Claude Code & Cowork Interactive Course

An interactive course that runs **inside Claude Code itself** — no separate LMS, no slides, no videos to sit through. Open this folder in Claude Code and Claude becomes your personal tutor, walking you through everything from first conversation to advanced automation.

## What This Course Covers

This course is focused on **Claude Code and Cowork** — the two interfaces where Claude works directly with your files, tools, and workflows. It starts from the absolute basics and progresses through intermediate and beginning-advanced skills:

- **Fundamentals:** What Claude Code is, how to connect your tools, why folder structure matters, your first builds
- **Cowork:** Background tasks, delegating work, task decomposition
- **Skills & Plugins:** How to find, copy, and build skills that extend what Claude can do
- **Use Case Thinking:** Identifying the highest-value ways to use AI in your specific role
- **Intermediate Skills:** Custom skill creation, scheduling, best practices, context management
- **Building:** Hands-on sessions building real use cases with Claude as your reviewer
- **Advanced:** Prototyping, GitHub, terminal workflows, multi-agent orchestration, codifying judgment

### What This Course Does NOT Cover

This course does not cover **Claude Chat** (the conversational interface). Chat is a similar experience to ChatGPT and other chat-based AI tools — if you've used one, you'll feel at home. We have other offerings that cover chat interfaces more in depth. If you're looking for a primer on how to get the most out of chat-style AI, check out the [30 Days of AI series](https://thumbtack.haystack.so/resources/0041286c-fdad-442a-b4db-dfd57e08ae53).

## Quick Start

1. **Download this folder** — Clone the repo or download as a zip
2. **Open the folder in Claude Code** — In the app: "Open Folder" → select this folder. In terminal: `cd` into it and run `claude`
3. **Start learning** — Claude greets you automatically and guides you from there

That's it. Claude becomes your tutor the moment you open this folder.

## Course Commands

| Command | What it does |
|---------|-------------|
| `/course` | Show the course menu with all modules and your progress |
| `/lesson` | Start or resume your current lesson |
| `/skip 2.03` | Jump to any specific lesson |
| `/progress` | See detailed stats, badges, and completion |
| `/hint` | Get a hint for the current exercise |
| `/check` | Validate your current exercise |
| `/exit` | Graceful off-ramp with summary and feedback |

## Modules

| Module | Focus | Lessons |
|--------|-------|---------|
| 1. Fundamentals | Claude Code vs Chat vs Cowork, connectors, folders | 5 |
| 2. Cowork | Task execution, indexing, data analysis | 4 |
| 3. Skills & Plugins Primer | What they are, finding/copying, building your first | 4 |
| 4. Use Case Thinking | Feed context, copy & study skills, plan mode, build use cases | 4 |
| 5. Intermediate Skills | Custom skills, scheduling, best practices, CLAUDE.md, context files | 5 |
| 6. Building Your Use Cases | Hands-on building with Claude's review & feedback | 4 |
| 7. Advanced | Prototyping, GitHub, terminal, multi-agent, evaluation loops | 6 |

**32 lessons total.** Each takes 5-10 minutes. Lessons have 3 sections: **Learn** (concepts) → **Practice** (guided build) → **Challenge** (optional stretch goal). You build real things useful to your work — no contrived exercises.

## How It Works

- Claude reads the `CLAUDE.md` file in this folder and transforms into your course tutor
- Your progress saves automatically in `progress.json` — close and come back anytime
- Videos are included as optional demos throughout — not required to progress
- Ask Claude questions anytime — it's your tutor for the whole course
- Skip ahead anytime with `/skip` if you already know the material

## Folder Structure

```
claude-course/
├── CLAUDE.md          ← The "brain" that makes Claude your tutor
├── progress.json      ← Your saved progress
├── modules/           ← All course content (7 modules, 32 lessons)
├── workspace/         ← Build your projects here (early modules)
├── playground/        ← Free experimentation sandbox
└── reference/         ← Cheat sheet, glossary, troubleshooting
```

## Resetting Progress

Your progress is stored in `progress.json`. To start fresh, delete the file or reset all values to `false` — Claude will treat you as a new learner on the next session.

## Need Help?

- **During the course:** Just ask Claude! It's your tutor.
- **Technical issues:** Check `reference/troubleshooting.md`
- **Course feedback:** Use the `/exit` command to share feedback via survey

---

*Built by Thumbtack L&D*
