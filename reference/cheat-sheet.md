# Claude Code & Cowork Cheat Sheet

## Quick Reference

### Core Agreements

1. **Use AI to Ask AI** — Stuck? Ask Claude first. That's literally what it's here for.
2. **Progress Over Perfection** — Keep moving forward. Done is better than perfect.
3. **Speed Bumps = Learning** — Unexpected results aren't failure — they're how you learn these tools.
4. **Be Okay with the Imperfect** — AI isn't always perfect on the first try. The skill is in iterating.
5. **Always Verify Output** — Claude is confident even when wrong. Check assumptions, catch gaps, and test edge cases before trusting any output.

These sit alongside Thumbtack's [AI Expectations](https://thumbtack.haystack.so/resources/c8602dcc-0898-4f92-ae93-243ee7d696ba), including **Own the outcomes**: share work only once it's ready for its audience.

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

> **In Claude Code:** these also work as slash commands (`/course`, `/lesson`, etc.) — in the app or terminal.
> **In Claude Cowork:** slash commands don't work — just ask in plain language ("show me the course menu," "give me a hint," "skip to lesson 2.03"). Claude understands either way.

### When to Use What

| Need | Tool | Example |
|------|------|---------|
| Think through something | **Chat** | Brainstorm ideas, outline a doc, rewrite text |
| Get a task done | **Cowork** | Index emails, compile a summary, draft messages |
| Build something | **Claude Code** | Create skills, tools, templates, prototypes |
| Make something to share | **Artifact** | Doc, deck, one-pager, dashboard, animation |

### Key Concepts

**CLAUDE.md** — The file that tells Claude how to behave in a folder. Put it at the root.

**SKILL.md** — A reusable workflow file. Has YAML frontmatter + numbered steps.

**Plan Mode** — Think before you build. Claude Code only — Cowork lays out a plan but has no plan mode. Always plan first!

**Plugin** — A bundle of extensions: skills, connectors, subagents, and more. Manage them under **Customize**.

**Connectors/MCP** — Integrations that give Claude access to your tools (Slack, Gmail, Calendar, etc.)

**Sessions** — Each conversation is a session. You can have multiple open at once.

**Artifact** — A shareable doc, deck, design, dashboard, or animation with its own link. Starts private. For Thumbtack branding, say "Use the Thumbprint design." (Module 4)

**Approval modes** — How often Cowork asks before acting: Manual, Auto, or Skip. Claude Code's modes are Manual, Accept edits, Plan, and Auto.

**/goal** — A Claude Code command that sets a completion condition and keeps Claude working until it's met. Great for large, repetitive work with a verifiable finish line — audits, vendor evals, verified research. The goal must be specific and demonstrable in the output. (Module 8)

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
- Switch modes: mode selector next to the message box (Shift+Tab in the terminal)
- Undo: press Esc twice, or type `/rewind`
- Browser pane: Cmd+Shift+B (Mac) / Ctrl+Shift+B (Windows)
- Split view: Option-click (Mac) / Alt-click (Windows) a session in the sidebar

### Discernment Checklist

Ask these after every Claude output:

1. **What did Claude assume?** — Identify unstated assumptions
2. **What's missing?** — Look for gaps in context, edge cases, or requirements
3. **What could break?** — Think about real-world failure scenarios
4. **Does it match my goal?** — Compare output to your original intent
5. **Would I trust this from a colleague?** — Apply the same review standard you'd use for human work

For deeper evaluation, use the [AIRCRAFT Judgment Rubric](https://coda.io/d/_d65keLkjPAQ/AI-RCRAFT-Judgment-Rubric_suFNbe1a).

### Common Patterns

**Daily Digest:** Cowork indexes Slack + email + calendar → sends summary to Slack
**Meeting Prep:** Claude Code reads calendar → pulls Granola notes → creates prep doc
**Weekly Review:** Chain: pull meeting notes → compile action items → draft status update
**Skill Builder:** Plan in Code → build SKILL.md → test → deploy
