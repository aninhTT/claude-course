---
module: 4
lesson: 1
title: "Feed Claude Your Context"
difficulty: intermediate
prerequisites: "3.04"
---

# Lesson 4.01: Feed Claude Your Context

## Learn

Claude gets dramatically better when it understands who you are, what you do, and how you work. In this lesson, you're going to give Claude a deep briefing on yourself — and then use that context for the rest of this module.

### Why Context Matters

Think about delegating to a new team member. If you just say "handle this," they'll struggle. But if you spend 10 minutes explaining your role, your team, your priorities, and your workflows — they become 10x more effective.

Same with Claude. The more context you provide about:
- **Your role** — what you do day-to-day
- **Your team** — who you work with and how
- **Your workflows** — recurring processes, meetings, communication patterns
- **Your pain points** — what takes too long, what's tedious, what you wish was automated
- **Your tools** — what you use and how it all fits together

...the better Claude can brainstorm use cases, build relevant tools, and actually help with your real work.

### Where to Put Context

There are a few places context can live:
- **In the conversation** — tell Claude directly (great for one-time use)
- **In a CLAUDE.md file** — persists across sessions in that folder (great for projects)
- **In context files** — separate files Claude can reference (great for detailed background)

For this module, we'll put your context in a dedicated file so Claude can reference it throughout your use case brainstorm.

## Practice

Let's create your personal context file.

**Step 1:** Create a file called `my-context.md` in `workspace/`. Start by telling Claude about yourself in a natural way — your role, team, main responsibilities.

**Step 2:** Add your workflows. Describe 3-5 things you do regularly — daily, weekly, or monthly. Be specific: "Every Monday I compile updates from 4 team leads via Slack and email into a status doc for leadership."

**Step 3:** Add your pain points. What takes too long? What's tedious? What do you wish you didn't have to do manually? Be honest — these are your best use case opportunities.

**Step 4:** Review the file with Claude. Ask: "Based on this context, what jumps out as the best opportunities for AI assistance?"

**Success criteria:** Created a my-context.md file in workspace/ with role description, at least 3 workflows, and at least 2 pain points. Had Claude review it.

## Challenge

Expand your context file with a "tools and systems" section. List every tool you use regularly and how it fits into your work. Then ask Claude: "Given my tools and workflows, where are the biggest gaps that Claude Code or Cowork could fill?"

**Success criteria:** Added tools/systems section to context file and got Claude's gap analysis.
