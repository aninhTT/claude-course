---
module: 6
lesson: 3
title: "Build Session: Your Second Use Case"
difficulty: intermediate
prerequisites: "6.02"
---

# Lesson 6.03: Build Session: Your Second Use Case

## Learn

Time for build #2. But this time, there's a twist: you're going to **integrate the review pattern during the build**, not just after it.

In Lesson 6.01, you built first and reviewed later. That works, but it often means rework — you find issues at the end and have to go back and fix them. A better approach:

### Build-Review-Improve Loops

Instead of: Build everything --> Review --> Fix

Try: Build step 1 --> Review --> Improve --> Build step 2 --> Review --> Improve --> ...

After each major step, pause and ask Claude:
- "Before we move on, does this step look right?"
- "Is there anything that could go wrong with what we just built?"
- "Does this output match what the next step needs as input?"

This catches issues early and produces a higher-quality build in less total time. Think of it as quality control on the assembly line, not just inspection at the end.

### What "Higher Quality" Looks Like

By the end of this lesson, your second build should be noticeably better than your first:
- Fewer gaps and edge cases
- Clearer instructions (if it's a skill)
- More reliable output
- Better error handling

The improvement comes from the process, not from being more careful. The review pattern does the heavy lifting.

## Practice

Build your second use case from the Module 5 plans.

**Step 1:** Open a new session (separate from the course session).

**Step 2:** Share the build plan with Claude. Ask it to break the build into distinct steps.

**Step 3:** Build step by step. After each major step, ask Claude to review before moving on:
- "Does this look right?"
- "What could go wrong here?"
- "Is the output of this step what we need for the next step?"

**Step 4:** Make improvements based on each review before continuing to the next step.

**Step 5:** When the build is complete, do a final end-to-end test with real data.

**Step 6:** Come back to this course session. Describe what you built and how the build-review process went.

**Success criteria:** Built your second use case using the build-review-improve loop at each major step. Tested with real data.

## Challenge

Compare build #1 and build #2 side by side.

**Step 1:** Open both builds (or their descriptions/notes). Ask Claude to compare them on:
- Completeness — Does each build handle the full use case?
- Reliability — How likely is each to fail or produce bad output?
- Clarity — If someone else looked at this, would they understand it?
- Quality of output — Is the actual result useful and well-formatted?

**Step 2:** Document the differences. What's better about build #2? What specific improvements came from the integrated review process?

**Step 3:** Reflect: Did the build-review-improve loop save time overall, even though each step took slightly longer? Would you use this process for future builds?

Save your comparison in `workspace/build-comparison.md`.

> **Before you're done — Question It:** What did Claude assume? What's missing? What could break?

**Success criteria:** Compared both builds across multiple dimensions. Documented specific improvements from the review process. Saved comparison in workspace/.
