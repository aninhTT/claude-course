---
module: 4
lesson: 3
title: "Plan Mode"
difficulty: intermediate
prerequisites: "4.02"
videos:
  - url: "https://www.loom.com/share/45414690b4254ca6a62d3f65b2c24d43"
    title: "Plan Mode in Claude Code"
    duration: "~5 min"
    context: "Watch this to see plan mode in action"
---

# Lesson 4.03: Plan Mode

## Learn

This might be the most important lesson in the course: **plan mode**.

### The Golden Rule

**If you plan to build anything in Claude Code — plan first.**

Plan mode is a feature unique to Claude Code (Cowork does NOT have it). It's how you get Claude to think through an approach before writing any code or creating any files.

### Why Plan Mode Matters

Without plan mode, here's what happens:
1. You ask Claude to build something
2. Claude starts building immediately
3. Halfway through, you realize it's going in the wrong direction
4. You've wasted time and context

With plan mode:
1. You ask Claude to build something
2. Claude thinks through the approach, identifies decisions, and presents a plan
3. You review, give feedback, adjust
4. Claude builds with a clear, approved plan
5. The result is much closer to what you wanted on the first try

### How to Use Plan Mode

In Claude Code, you can enter plan mode by:
- Asking Claude to "plan" or "think about" something before building
- Using the plan mode toggle in the interface
- Saying something like "Before you build this, let's plan it out"

In plan mode, Claude will:
- Explore the relevant files and context
- Identify key decisions and trade-offs
- Present a structured plan with steps
- Ask for your input on decisions
- Wait for your approval before implementing

### When to Use Plan Mode

- **Always** before building something new
- **Always** before making significant changes
- **Always** when the task has multiple possible approaches
- You can skip it for tiny, obvious changes (fixing a typo, adding one line)

### Plan Mode vs Cowork

Remember: **Cowork does NOT have plan mode.** This is where Plan Mode becomes your best friend in Claude Code — it forces goal clarification before execution. But Cowork doesn't have these guardrails in the same way. With Cowork, you need to be very clear about what you're looking for upfront. That's why it's helpful to have Cowork interview you to help clarify what your actual goal is before it starts working.

Here's a practical pattern: when you start a Cowork task, state your goal, then ask Cowork to state it back to you and help you clarify before it does anything. This "state it back" loop is the Cowork equivalent of Plan Mode — it surfaces misunderstandings before Cowork spends time executing in the wrong direction.

For Claude Code, Plan Mode handles this for you. Plan in Code, then hand the execution to Cowork if appropriate.

There's a great demo of plan mode in action: https://www.loom.com/share/45414690b4254ca6a62d3f65b2c24d43

## Practice

Let's use plan mode for one of your use cases from Lesson 4.02.

**Step 1:** Take your top use case idea from `workspace/use-case-ideas.md`.

**Step 2:** Ask Claude to enter plan mode and plan how to build it. Frame it like: "I want to build [your use case]. Before we build anything, let's plan it out. What would the approach look like?"

**Step 3:** Review Claude's plan. Give it feedback:
- What looks right?
- What's missing?
- What should change?

**Step 4:** Iterate on the plan until you're happy with the approach. Don't build yet — just plan.

**Success criteria:** Used plan mode to create a plan for their top use case. Plan was iterated on at least once based on their feedback.

## Challenge

Use plan mode for a second use case from your list. This time, explicitly ask Claude to present 2-3 different approaches and the trade-offs of each. Pick the best one and refine the plan.

> **Before you're done — Question It:** What did Claude assume? What's missing? What could break?

**Success criteria:** Created a plan with multiple approaches, evaluated trade-offs, and selected a final approach.
