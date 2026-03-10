---
description: Start or resume your current lesson
---

# /lesson — Start or Resume Current Lesson

1. Read `progress.json` to find `current_position` (module and lesson number).
2. Load the corresponding lesson file from `modules/{module}/lessons/{lesson}.md`.
3. Read the lesson's YAML frontmatter for metadata (title, difficulty, prerequisites, videos).
4. Determine which section the learner is on:
   - If `learn` is not complete → start with the **Learn** section
   - If `learn` is done but `practice` is not → start with **Practice**
   - If `practice` is done but `challenge` is not → start with **Challenge**
   - If all sections complete → congratulate and advance to next lesson

## Presenting the Lesson

Show a lesson header:
```
───────────────────────────────────────────
Module {X} · Lesson {Y}
{Lesson Title}
Difficulty: {difficulty} | Est. 5-10 min
───────────────────────────────────────────
```

### For Learn sections:
- Present the teaching content **conversationally** — break it into chunks, not a wall of text
- Ask comprehension questions between chunks
- If the lesson has videos in frontmatter, mention them naturally at appropriate moments
- After the learner has engaged with the content, mark `learn: true` in progress.json
- Transition to Practice

### For Practice sections:
- Give **one instruction at a time**
- Wait for the learner to complete each step before giving the next
- Validate their work exists (check files, ask to see output)
- After successful completion, mark `practice: true` in progress.json
- Transition to Challenge

### For Challenge sections:
- Present the challenge prompt
- Step back — let them work independently
- Only help if they use `/hint`
- When they say they're done or ask you to check, validate against the success criteria in the lesson
- Mark `challenge: true` and update stats

After completing all three sections of a lesson:
- Update progress.json (advance current_position, update stats)
- Check for badge conditions
- Show a brief completion message
- Offer to continue to the next lesson
