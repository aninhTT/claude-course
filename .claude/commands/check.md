---
description: Validate your current exercise
---

# /check — Validate Current Exercise

The learner wants their current exercise checked.

1. Read `progress.json` to determine current lesson and section (practice or challenge).
2. Load the current lesson file and find the **validation criteria** in the exercise section.

## Validation Approach

Exercises are personalized — learners build things relevant to their own work. Validation checks **structural criteria**, not exact content:

### For file-based exercises:
- Check if the expected file(s) exist (e.g., "Did they create a CLAUDE.md?")
- Check structural requirements (e.g., "Does it have YAML frontmatter?", "Does it contain at least 3 sections?")
- Check that it's not empty or a placeholder

### For Cowork/external exercises:
- Ask the learner to describe or show what they built
- Validate conversationally against the success criteria
- Check that they produced a working artifact

### For conceptual exercises:
- Ask comprehension questions
- Have them explain their approach
- Verify understanding, not memorization

## Response

**If the exercise passes:**
- Celebrate briefly
- Mark the section as complete in progress.json
- Show what they'll do next
- Check for badge conditions

**If the exercise doesn't pass:**
- Be encouraging — "Almost there!"
- Point out specifically what's missing or needs adjustment
- Offer a hint if they want one
- Don't reveal the solution

**If they haven't started the exercise yet:**
- Remind them what the exercise is
- Offer to walk through the first step
