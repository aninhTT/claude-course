# Claude Code & Cowork Interactive Course

An interactive course that runs **inside Claude itself** — works in both **Claude Code** and **Claude Cowork**, with no separate LMS, no slides, and no videos to sit through. Open this course in either Code or Cowork and Claude becomes your personal tutor, walking you through everything from first conversation to advanced automation.

> **Works in both Code and Cowork.** The course is built so the experience is identical in either interface. In Claude Code, open the folder. In Claude Cowork, just upload the zip of this course and it runs exactly the same way it does in Code.

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

This course does not cover **Claude Chat** (the conversational interface). Chat is a similar experience to ChatGPT and other chat-based AI tools — if you've used one, you'll feel at home. Cowork and Code are different experiences given they build locally on your computer, unlike chat interfaces.

## Quick Start

Use whichever interface you prefer — the course works the same in both.

**In Claude Code:**

1. **Download this folder** — Clone the repo or download as a zip
2. **Open the folder in Claude Code** — In the app: "Open Folder" → select this folder. In terminal: `cd` into it and run `claude`
3. **Start learning** — Claude greets you automatically and guides you from there

**In Claude Cowork:**

1. **Download this course as a zip** — Use the green "Code" button on GitHub → "Download ZIP" (or zip your local copy)
2. **Upload the zip to Claude Cowork** — Cowork unpacks the course and reads its instructions automatically
3. **Start learning** — Claude greets you and guides you exactly as it does in Code

That's it. Claude becomes your tutor the moment you open the course — in Code or Cowork.

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

> **Heads up — slash commands only work in Claude Code.** In **Claude Cowork**, slash commands don't work — just ask in plain language for what you want, like "show me the course menu," "give me a hint," or "skip to lesson 2.03." Either way, Claude knows what you mean.

## Modules

| Module | Focus | Lessons |
|--------|-------|---------|
| 1. Fundamentals | Claude Code vs Chat vs Cowork, connectors, folders | 6 |
| 2. Cowork | Task execution, indexing, data analysis | 4 |
| 3. Skills & Plugins Primer | What they are, finding/copying, building your first | 5 |
| 4. Use Case Thinking | Feed context, copy & study skills, plan mode, build use cases | 4 |
| 5. Intermediate Skills | Custom skills, scheduling, best practices, CLAUDE.md, context files | 6 |
| 6. Building Your Use Cases | Hands-on building with Claude's review & feedback | 4 |
| 7. Advanced | Prototyping, GitHub, terminal, multi-agent, evaluation loops, goals | 8 |

**37 lessons total.** Each takes 5-10 minutes. Lessons have 3 sections: **Learn** (concepts) → **Practice** (guided build) → **Challenge** (optional stretch goal). You build real things useful to your work — no contrived exercises.

## How It Works

- Claude reads the `CLAUDE.md` file in this course and transforms into your course tutor — this works the same whether you open the folder in Claude Code or upload the zip to Claude Cowork
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
