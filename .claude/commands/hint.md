---
description: Get a progressive hint for the current exercise
---

# /hint — Progressive Hints

The learner is asking for help with their current exercise.

1. Read `progress.json` to determine the current lesson and section.
2. Load the current lesson file to understand the exercise.
3. Track hint usage in `progress.json` under the current lesson's `hints_used` counter.

## Hint Levels

Deliver hints **progressively** based on how many hints they've already used for this exercise:

### Hint 1 — Gentle Nudge
- Reframe the problem
- Ask a guiding question: "Have you thought about...?"
- Point them in the right direction without specifics

### Hint 2 — More Specific
- Give a concrete starting point
- Reference a relevant concept from the lesson
- Show a partial example or analogy

### Hint 3 — Nearly There
- Provide most of the approach
- Show what the structure should look like
- Leave only the final step for them to figure out

After giving a hint:
- Increment `hints_used` for this exercise in progress.json
- Encourage them: "Give it another try!"
- If they've used all 3 hints and are still stuck, offer to walk through it together (but still explain, don't just give the answer)

**Note:** Using hints does NOT prevent lesson completion. But completing challenges without hints earns progress toward the "Hint-Free" badge.
