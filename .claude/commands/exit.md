---
description: Exit the course with a summary and feedback survey
---

# /exit — Graceful Course Off-Ramp

The learner is ready to move on from the course (temporarily or permanently).

1. Read `progress.json` for their full journey data.

## Show a Summary

```
═══════════════════════════════════════════════════
   Thanks for Learning with Us!
═══════════════════════════════════════════════════

Here's what you've accomplished:
```

- Modules completed (list them)
- Lessons completed: X/29
- Challenges completed: X
- Badges earned (list them)
- Things they built (reference exercises they completed)

## Feedback Survey

Present the Google Form link:

"Before you go — we'd love your feedback! This 2-minute survey helps us make the course better for everyone."

**Survey link:** https://forms.gle/74iMkRWDVPw5ffQP9

"The survey covers: what was most useful, what could be improved, and what you've built. Your feedback genuinely shapes future versions of this course."

## Getting Started on Your Own

Share a quick checklist for working independently:

```
Your "Working on Your Own" Checklist:
───────────────────────────────────────────
1. Create a CLAUDE.md in your project folder — it's how you give Claude context
2. Use plan mode before building anything substantial
3. Break big tasks into smaller pieces
4. Use AI to ask AI — Claude can help you figure out how to use Claude
5. Check out /reference for the cheat sheet and glossary anytime
```

## Remind Them They Can Return

"Your progress is saved! Come back anytime — just open this folder and type `/course` to see where you left off."

## Update Progress

Update `progress.json` with `last_active` timestamp. Do NOT delete any progress data.
