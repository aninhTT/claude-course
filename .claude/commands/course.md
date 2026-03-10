---
description: Show the course menu with all modules and your current progress
---

# /course — Course Dashboard

Read `progress.json` to get the learner's current state.

Display a **course dashboard** with the following format:

```
═══════════════════════════════════════════════════
   Claude Code & Cowork Course
   by Thumbtack L&D
═══════════════════════════════════════════════════

Welcome back, {learner_name}!

Your Progress: [████████░░] {percent}% complete
Lessons: {completed}/{total} | Challenges: {challenges}/{total_challenges}
Current streak: {streak_days} day(s)
```

Then show all 6 modules with status indicators:

- **Completed modules:** `[completed]` with completion checkmark
- **Current/unlocked modules:** `[in-progress]` or `[unlocked]`
- **Locked modules:** `[locked]` (need 3+ lessons in previous module)

For each module, show:
- Module number and title
- Lesson count and how many completed
- Brief one-line description

**Module list:**
1. **Fundamentals** (5 lessons) — Claude Code vs Chat vs Cowork, connectors, folders, first build
2. **Cowork** (5 lessons) — Task execution, indexing, parallel agents, multiple sessions
3. **Skills & Plugins Primer** (3 lessons) — Skills, plugins, building your first reusable skill
4. **Use Case Thinking** (5 lessons) — Feed context, plan mode, design & build use cases
5. **Intermediate Claude Code** (5 lessons) — CLAUDE.md deep dive, custom skills, memory, workflows
6. **Advanced Claude Code** (6 lessons) — Prototyping, GitHub, terminal, multi-agent, MCP/hooks

After the dashboard, show:
- Any earned badges
- Quick actions: "Type `/lesson` to continue where you left off, or `/skip X.XX` to jump to any lesson."
- If they haven't started: suggest starting with Module 1

If this is a **brand new learner** (no progress.json), show the welcome content from `modules/00-welcome/welcome.md` first, then the dashboard.
