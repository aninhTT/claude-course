---
module: 7
lesson: 1
title: "Prototyping with Claude Code"
difficulty: advanced
prerequisites: "6.04"
---

# Lesson 7.01: Prototyping with Claude Code

## Learn

One of Claude Code's most powerful capabilities is something that doesn't require any special configuration: **rapid prototyping**. You can take an idea — half-formed, rough, maybe just a "what if..." — and have a working demo in minutes.

This isn't about building production software. It's about making ideas tangible fast enough to learn from them.

### The Prototyping Mindset

When you're prototyping with Claude Code, shift your thinking:

- **Speed over polish.** Don't worry about perfect formatting, comprehensive error handling, or beautiful output. Get the core idea working first.
- **Iterate fast.** Try something, see what happens, adjust. Don't plan for an hour before building for five minutes.
- **Throw away what doesn't work.** A prototype that proves an idea doesn't work is still valuable — you learned something in minutes instead of days.
- **Talk through it with Claude.** Use plan mode to sketch the concept, then immediately start building. Claude is great at both thinking and doing.

### When to Prototype vs Build Properly

Not everything needs to be prototyped, and not every prototype needs to become a proper build. Here's how to think about it:

**Prototype when:**
- You're exploring an idea and don't know if it's worth investing in
- You want to learn something fast — how a workflow feels, whether a concept works, what the edge cases are
- You're testing feasibility: "Can Claude actually do this?"
- You want to show someone a concept rather than describe it
- Speed matters more than polish

**Build properly when:**
- The thing will be used in production by real people
- Reliability matters — it can't fail silently or produce bad output
- You need error handling, edge cases, and robustness
- Others will maintain or extend what you've built

The line between these two is often blurry, and that's fine. Many great tools start as prototypes. The key is knowing which mode you're in so you don't over-invest in something exploratory or under-invest in something important.

### What Makes a Good Prototype

A good prototype demonstrates the **core concept** — the one thing you're trying to test or show. It doesn't need to handle every edge case, support every input format, or look production-ready.

Ask yourself: "If I showed this to someone for 2 minutes, would they understand the idea?" If yes, the prototype has done its job.

### The Prototyping Process

Here's the process that works best with Claude Code:

1. **Plan mode** — Spend 2-3 minutes having Claude think through the approach. What are the key pieces? What's the simplest version that demonstrates the idea?
2. **Build fast** — Ask Claude to create the prototype. Don't overthink it — let Claude take a first pass and then adjust.
3. **Test** — Run it with real data if possible. Does the core concept work?
4. **Iterate** — Fix the most important issue, then test again. Each iteration should be quick.
5. **Get feedback** — Show it to someone (or ask Claude to role-play as a skeptical user).

### Going From Prototype to Production

When a prototype proves valuable and you want to make it real, the path looks like this:

- **Start with the user experience.** Before adding features, ask: what will someone see? What will they do? What will they get back?
- **Build the happy path first.** Get the main flow working before worrying about what happens when things go wrong.
- **Add complexity only if the core works.** If the basic version doesn't demonstrate the idea, adding features won't fix it.
- **Don't optimize prematurely.** If it works but it's slow, messy, or inelegant — that's fine for early iterations.
- **Document the gap.** Write a brief note answering: What would need to change to make this production-ready? How much additional effort would it take?

This "gap document" is valuable. It turns a prototype into a proposal.

### Debugging Best Practices

Things will break when you prototype. That's expected. Here's how to debug effectively with Claude:

**Share screenshots.** When something looks wrong, take a screenshot and share it with Claude. Visual context helps Claude understand the issue much faster than a text description alone.

**Ask Claude what it did and why.** When something goes wrong, don't just ask Claude to fix it — ask: "What did you do in that last step, and why?" Understanding Claude's reasoning helps you learn and prevents the same issue from happening again.

**Ask how it fixed the issue.** After Claude resolves a problem, ask: "How did you fix that? What was the root cause?" This builds your intuition for future debugging.

**Ask how to prevent it.** Take it one step further: "How can we make sure this doesn't happen again?" Claude might suggest adding error handling, changing the approach, or structuring things differently.

The pattern is: **break → understand → fix → learn → prevent.** Each debugging cycle makes you a better builder.

## Practice

Time to prototype something. The rules are simple:

**Step 1: Pick an idea.** Any idea. It could be:
- A tool that automates part of your workflow
- A template system for something you create repeatedly
- A simple app or dashboard concept
- An automation that connects two things that don't currently talk to each other
- Something fun or experimental — it doesn't have to be "useful" yet

**Step 2: Use plan mode to sketch the concept.** Spend 2-3 minutes having Claude think through the approach. What are the key pieces? What's the simplest version that demonstrates the idea?

**Step 3: Build it.** Ask Claude to create the prototype. Don't overthink it — let Claude take a first pass and then adjust.

**Step 4: Timebox to 15 minutes.** Set a timer. When it goes off, stop. Whatever you have at that point is your prototype.

**Step 5: Test with real data if possible.** Real Slack messages, real calendar events, real documents. Prototypes that run on real data are much more convincing than ones that use fake inputs.

The constraint is important. Prototyping is about speed and learning, not perfection.

**Success criteria:** Created a working prototype of any concept within `workspace/`. It doesn't need to be perfect — it needs to exist and demonstrate an idea.

## Challenge

Take your prototype and make it share-worthy. Not production-ready — but good enough that you could demo it to your team.

**Step 1:** Show your prototype to a colleague — or, if no one's available, describe it to Claude and ask it to role-play as a skeptical user. Get one piece of honest feedback.

**Step 2:** Use that feedback to improve the prototype in one focused iteration. Don't rebuild — improve.

**Step 3:** Clean up the rough edges. Fix any obvious issues, improve the output format, add a brief description of what it does and how to use it.

**Step 4:** Document the gap. Write a brief note in `workspace/` answering:
- What would need to change to make this production-ready?
- What edge cases are missing?
- How much additional effort would it take — hours, days, weeks?

> **Before you're done — Question It:** What did Claude assume? What's missing? What could break?

**Success criteria:** Iterated on the prototype based on feedback. Cleaned it up to demo quality. Documented what would be needed to make it production-ready.
