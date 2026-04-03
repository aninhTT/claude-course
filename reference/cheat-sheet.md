# Claude Code & Cowork Cheat Sheet

## Quick Reference

### Core Agreements

1. **Use AI to Ask AI** — Stuck? Ask Claude first. That's literally what it's here for.
2. **Progress Over Perfection** — Keep moving forward. Done is better than perfect.
3. **Speed Bumps = Learning** — Unexpected results aren't failure — they're how you learn these tools.
4. **Be Okay with the Imperfect** — AI isn't always perfect on the first try. The skill is in iterating.

### Course Commands

Type these as a message to navigate the course:

| Command | Action |
|---------|--------|
| `course` | Course menu + progress |
| `lesson` | Continue current lesson |
| `skip 2.03` | Jump to any lesson |
| `progress` | Detailed stats + badges |
| `hint` | Help with current exercise |
| `check` | Validate current exercise |
| `exit` | Leave course with summary |

> **CLI users:** These also work as slash commands (`/course`, `/lesson`, etc.) in the terminal.

### When to Use What

| Need | Tool | Example |
|------|------|---------|
| Think through something | **Chat** | Brainstorm ideas, outline a doc, rewrite text |
| Get a task done | **Cowork** | Index emails, compile a summary, draft messages |
| Build something | **Claude Code** | Create skills, tools, templates, prototypes |

### Key Concepts

**CLAUDE.md** — The file that tells Claude how to behave in a folder. Put it at the root.

**SKILL.md** — A reusable workflow file. Has YAML frontmatter + numbered steps.

**Plan Mode** — Think before you build. Claude Code only (not Cowork). Always plan first!

**Plugin** — Umbrella term for anything that extends Claude: skills, commands, and connectors.

**Connectors/MCP** — Integrations that give Claude access to your tools (Slack, Gmail, Calendar, etc.)

**Sessions** — Each conversation is a session. You can have multiple open at once.

### CLAUDE.md Template

```markdown
# Project Name

You are [role]. Your job is to [purpose].

## Key Context
- This project is about...
- The team works in...
- Important conventions: ...

## Rules
- Always do X before Y
- When the user asks about Z, check file A first
- Format output as...
```

### SKILL.md Template

```markdown
---
name: skill-name
description: "What this skill does"
---

# Skill Name

## Steps

1. First, do this...
2. Then check for...
3. Compile the results into...
4. Output as...

## Error Handling

If step 2 fails, try...
```

### Good Cowork Task Template

```
Task: [Clear one-line objective]
Sources: [What to check — Slack, email, calendar, Granola, files]
Timeframe: [How far back to look]
Output: [What to produce — summary, message, doc]
Deliver to: [Where to send it — Slack DM, file, etc.]
```

### Prompting Tips

- **Be specific:** "Draft a status update for my team about Q1 progress" > "Help with work"
- **Give context:** "I'm a PM on the marketplace team" changes everything
- **Iterate:** "Make it shorter" or "Focus more on the budget" — refine, don't restart
- **Plan first:** For any build, use plan mode before writing anything
- **One thing at a time:** Don't ask for 5 things in one message

### Keyboard Shortcuts (Claude Code App)

- New session: Check app menu
- Switch sessions: Session sidebar
- Plan mode: Toggle in interface or ask "let's plan this first"

### Common Patterns

**Daily Digest:** Cowork indexes Slack + email + calendar → sends summary to Slack
**Meeting Prep:** Claude Code reads calendar → pulls Granola notes → creates prep doc
**Weekly Review:** Chain: pull meeting notes → compile action items → draft status update
**Skill Builder:** Plan in Code → build SKILL.md → test → deploy
