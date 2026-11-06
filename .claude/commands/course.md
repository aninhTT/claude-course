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

Then show all 8 modules with status indicators:

- **Completed modules:** `[completed]` with completion checkmark
- **Current/unlocked modules:** `[in-progress]` or `[unlocked]`
- **Locked modules:** `[locked]` (need 3+ lessons in previous module)

For each module, show:
- Module number and title
- Lesson count and how many completed
- Brief one-line description

**Module list:**
1. **Fundamentals** (6 lessons) — Claude Code vs Chat vs Cowork, connectors, folders, first build
2. **Cowork** (5 lessons) — Task execution, data analysis, task decomposition, Claude in Chrome & Slack
3. **Skills & Plugins Primer** (5 lessons) — Skills, plugins, building your first reusable skill
4. **Artifacts** (5 lessons) — Docs, slides, designs, dashboards, motion, and sharing
5. **Use Case Thinking** (4 lessons) — Feed context, plan mode, design & build use cases
6. **Intermediate Skills** (6 lessons) — Custom skills, scheduling, best practices, CLAUDE.md, context files
7. **Building Your Use Cases** (4 lessons) — Hands-on building with Claude's review & feedback
8. **Advanced Claude Code** (9 lessons) — Prototyping, GitHub, terminal, multi-agent, memory, loops, context, goals

After the dashboard, show:
- Any earned badges
- Quick actions: "Type `/lesson` to continue where you left off, or `/skip X.XX` to jump to any lesson."
- If they haven't started: suggest starting with Module 1

If this is a **brand new learner** (no progress.json), show the welcome content from `modules/00-welcome/welcome.md` first, then the dashboard.
