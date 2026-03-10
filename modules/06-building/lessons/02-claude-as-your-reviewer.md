---
module: 6
lesson: 2
title: "Claude as Your Reviewer"
difficulty: intermediate
prerequisites: "6.01"
---

# Lesson 6.02: Claude as Your Reviewer

## Learn

Here's one of the most powerful patterns in working with AI: **using Claude to review what Claude built.**

After you build something — a skill, a workflow, a template, an automation — you can turn around and ask Claude to critique it. This isn't a contradiction. Claude is excellent at identifying gaps, edge cases, and improvements when you explicitly ask it to take a critical perspective. It's the difference between "build me a thing" and "now tell me what's wrong with the thing."

### The Review Prompts

Here are the most effective ways to get Claude to review your work:

**Gap analysis:**
> "Review this skill and point out any gaps. What scenarios does it not handle? What inputs would break it?"

**Edge case identification:**
> "What could go wrong with this workflow? Think of 5 ways it might fail or produce bad output."

**User perspective:**
> "If you were a new user of this, what would confuse you? What instructions are unclear or missing?"

**Improvement suggestions:**
> "Rate this build on a scale of 1-10 for completeness and reliability. Then suggest 3 specific improvements."

**Comparison review:**
> "Here's what this is supposed to do [paste the use case design]. Here's what I built [paste the build]. How well does the build match the design? What's missing?"

### Why This Works

When you ask Claude to build something, it's in "builder mode" — focused on making something work. When you ask Claude to review something, it shifts to "critic mode" — focused on finding problems. These are genuinely different cognitive approaches, and the combination is more powerful than either alone.

This pattern scales to anything: documents, emails, project plans, presentations, code. Build it, then review it.

### Making Review a Habit

The best builders review continuously, not just at the end. After each major step in a build, pause and ask Claude: "Before we move on, is there anything wrong with what we just did?" This catches issues early when they're cheap to fix, rather than late when they require rework.

### Using the Skill Creator Plugin as a Reviewer

There's a powerful plugin called **Skill Creator** that can critique and improve your skill builds. Here's how to use it:

**Step 1:** Install the Skill Creator plugin. Go to your Claude settings and browse available plugins. Look for "Skill Creator" and install it.

**Step 2:** Once installed, you can use it to review any skill you've built. Try:

> "/skill-creator Review my skill at [path to your SKILL.md]. Tell me what's strong, what's weak, and how to improve it."

The Skill Creator will analyze your skill's structure, instructions, error handling, and naming — and give you specific feedback on how to make it better.

This is one practical way to have Claude act as your reviewer: use specialized tools that know what "good" looks like for specific types of work.

## Practice

Take your build from Lesson 6.01 and run it through Claude's review process.

**Step 1:** Share your build with Claude (in this course session or a new session). Give Claude the full context: what the use case is, what you built, how it works.

**Step 2:** Ask Claude to perform three reviews:

1. **Gap review:** "Point out 3 gaps or weaknesses in this build."
2. **Improvement review:** "Suggest 3 specific improvements, ranked by impact."
3. **Rating:** "Rate this build on a scale of 1-10 for completeness, reliability, and usefulness. Explain each rating."

**Step 3:** Pick at least 2 of Claude's suggestions and implement them. Go back to your build session and make the improvements.

**Step 4:** After implementing the improvements, ask Claude to re-review. Did the rating improve?

**Success criteria:** Ran 3 review prompts on the Lesson 6.01 build. Implemented at least 2 suggestions. Got a re-review showing improvement.

## Challenge

Create a reusable **review prompt** — a template you can use on any future build. Think of it as a "build quality checklist" powered by Claude.

Your review prompt should:
- Work for any type of build (skills, workflows, templates, automations)
- Cover at least 4 dimensions (e.g., completeness, clarity, reliability, edge cases, usability)
- Include specific questions for each dimension
- Ask for a rating and prioritized improvements

Save it as `workspace/review-prompt.md` (or as a skill if you're feeling ambitious).

Test it on your build from Lesson 6.01 to make sure it produces useful feedback.

**Success criteria:** Created a reusable review prompt template that covers 4+ dimensions. Tested it on an existing build and verified it produces actionable feedback. Saved in workspace/.
