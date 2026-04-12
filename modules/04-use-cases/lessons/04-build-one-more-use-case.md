---
module: 4
lesson: 4
title: "Build One More Use Case"
difficulty: intermediate
prerequisites: "4.03"
---

# Lesson 4.04: Build One More Use Case

## Learn

You've brainstormed use cases, studied a working skill, and learned plan mode. Now it's time to design and build one more use case — reinforcing the full cycle from idea to working reality.

### The Use Case Template

Here's a template you can use for any use case you want to build. It forces you to think through every part before you start building:

```markdown
# Use Case: [Name]

## Summary
One sentence describing what this does and who it's for.

## Problem
What pain point does this solve? How are things done today?

## Solution
What does the AI-powered version look like?

## Tool Choice
- [ ] Claude Code (building/creating something)
- [ ] Cowork (executing a task)
- [ ] Both (plan in Code, execute in Cowork)

## Inputs
What context/data does this need? (Slack channels, email, calendar, files, etc.)

## Outputs
What does this produce? (Document, message, file, summary, etc.)

## Steps
1. Step one...
2. Step two...
3. Step three...

## Frequency
How often would this run? (On-demand, daily, weekly, etc.)

## Success Criteria
How do you know it worked? What does "good" look like?

## Future Improvements
What would make v2 even better?
```

### Why Templates Matter

Templates aren't just documentation — they're **thinking tools**. Filling out each section forces you to clarify your thinking before you start building. And once you have a solid use case template, turning it into a skill or Cowork task becomes much easier.

### From Template to Build

The template maps directly to what you'll build:
- **Inputs** become what you tell Claude to gather
- **Steps** become the workflow instructions
- **Outputs** become what Claude delivers
- **Error scenarios** (from Success Criteria) become your error handling

This is why planning first pays off — by the time you start building, you already know exactly what you're making.

## Practice

Build one more use case from your brainstorm list — this time from start to finish.

**Step 1:** Pick a use case from your `use-case-ideas.md` — ideally your #2 or #3 choice (you'll build your #1 in Module 6).

**Step 2:** Fill out the use case template. Save it to `workspace/` with a descriptive name (e.g., `use-case-meeting-prep.md`).

**Step 3:** Use plan mode (shift+tab in Claude Code) to plan the build. Give Claude the filled-out template and ask it to create a plan for building this as either a skill, a Cowork task, or both.

**Step 4:** Execute the plan. Build the use case — create the SKILL.md, set up the folder, write the instructions.

**Step 5:** Test it. Run the skill or task and see what happens. Does the output match your Success Criteria from the template?

**Step 6:** Iterate. Based on the test, make at least one improvement. Update the instructions, fix an edge case, or improve the output format.

> Remember: progress over perfection. Get a working v1, then improve it. You'll have more time to polish in Module 6.

**Success criteria:** Designed a use case using the template, built it as a skill or Cowork task, tested it at least once, and made at least one improvement based on testing.

## Challenge

Take the use case you just built and think about scale:

1. **Could this run on a schedule?** What would daily or weekly automation look like?
2. **Could a teammate use this?** What would you need to change to make it shareable?
3. **What's the v2?** If you had unlimited time, what would you add?

Write up your answers in the use case file as a "Future Vision" section.

> **Before you're done — Question It:** What did Claude assume? What's missing? What could break?

**Success criteria:** Added a "Future Vision" section to your use case file covering automation, shareability, and v2 improvements.
