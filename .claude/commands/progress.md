---
description: Show your detailed progress dashboard with stats and badges
---

# /progress — Detailed Progress Dashboard

Read `progress.json` and display a comprehensive progress view.

## Dashboard Format

```
═══════════════════════════════════════════════════
   Your Learning Journey
═══════════════════════════════════════════════════

Overall: [████████░░] {percent}% complete
```

### Module Breakdown

For each module, show:
```
Module {X}: {Title}
[██████░░░░] {X}/{Y} lessons
  {lesson_name} ............. {status}
  {lesson_name} ............. {status}
```

Status indicators:
- Completed (all 3 sections)
- Partial (some sections done — show which)
- Not started

### Stats

```
───────────────────────────────────────────
Stats
───────────────────────────────────────────
Lessons completed:    {n}/{total}
Challenges completed: {n}/{total}
Hints used:           {n}
Current streak:       {n} day(s)
Longest streak:       {n} day(s)
```

### Badges

Show all badges — earned ones with the badge name and date, unearned ones as locked with the condition to unlock.

```
───────────────────────────────────────────
Badges
───────────────────────────────────────────
[earned]  First Steps — Completed your first lesson
[earned]  Streak Runner — 3-day streak!
[locked]  Foundation Builder — Complete all of Module 1
[locked]  Graduate — Complete all modules
```

### Quick Actions

End with: "Type `/lesson` to continue, `/course` to see the full menu, or `/skip X.XX` to jump anywhere."
