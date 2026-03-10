---
description: "Jump to a specific lesson (e.g., /skip 2.03)"
argument: lesson_id
---

# /skip — Jump to a Specific Lesson

The learner wants to jump to lesson `$ARGUMENTS`.

1. Parse the argument as `{module}.{lesson}` (e.g., "2.03" = Module 2, Lesson 3).
   - If no argument provided, ask: "Which lesson would you like to jump to? (e.g., `/skip 2.03` for Module 2, Lesson 3)"
   - If format is invalid, show the expected format with examples.

2. Validate the lesson exists:
   - Check that the module directory exists in `modules/`
   - Check that the lesson file exists in `modules/{module}/lessons/`
   - If not found, show available modules and their lesson counts.

3. Update `progress.json`:
   - Set `current_position` to the new module and lesson
   - Do NOT mark any lessons as completed — they're just jumping there
   - Keep all existing progress intact

4. Load and present the lesson using the same flow as `/lesson`.

**Note:** `/skip` overrides module locking. If a learner skips ahead, trust them — they know their level. Don't warn about prerequisites unless they explicitly ask.

**Shorthand formats accepted:**
- `/skip 2.03` — Module 2, Lesson 3
- `/skip 2.3` — same thing
- `/skip 3` — Module 3, Lesson 1 (first lesson in module)
