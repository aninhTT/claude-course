---
module: 5
lesson: 1
title: "Feed Claude Your Context"
difficulty: intermediate
prerequisites: "4.05"
---

# Lesson 5.01: Feed Claude Your Context

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
- **In a GitHub repo** *(advanced)* — your context files in a repo you keep up to date (great for taking your context everywhere)

For this module, we'll put your context in a dedicated file so Claude can reference it throughout your use case brainstorm.

### Advanced Option: Keep Your Context in a GitHub Repo

If you want your context to go wherever you go, keep it in your own GitHub repo. Here's why that's useful:

- **It travels with you.** Any AI tool that can read a repo or a file can use it — Claude, ChatGPT, Gemini, Codex, and others. You're not locked into one tool.
- **You update it in one place.** When your role, team, or priorities change, edit the repo once and every tool gets the new version.
- **Claude can help maintain it.** Ask: "Update my context repo with what changed on my team this quarter."
- **You get a history.** GitHub keeps every version, so you can see how your work has changed over time.

This is a more advanced setup. You'll need GitHub access (Lesson 3.03 explains how to get it), and Module 8 covers GitHub basics. Keep the repo **private**, and only put in what you'd be comfortable sharing with any AI tool you use. Thumbtack's AI Expectations still apply.

## Practice

Let's create your personal context file.

**Step 1:** Create a file called `my-context.md` in `workspace/`. Start by telling Claude about yourself in a natural way — your role, team, main responsibilities.

**Step 2:** Add your workflows. Describe 3-5 things you do regularly — daily, weekly, or monthly. Be specific: "Every Monday I compile updates from 4 team leads via Slack and email into a status doc for leadership."

**Step 3:** Add your pain points. What takes too long? What's tedious? What do you wish you didn't have to do manually? Be honest — these are your best use case opportunities.

**Step 4:** Review the file with Claude. Ask: "Based on this context, what jumps out as the best opportunities for AI assistance?"

**Success criteria:** Created a my-context.md file in workspace/ with role description, at least 3 workflows, and at least 2 pain points. Had Claude review it.

## Challenge

Expand your context file with a "tools and systems" section. List every tool you use regularly and how it fits into your work. Then ask Claude: "Given my tools and workflows, where are the biggest gaps that Claude Code or Cowork could fill?"

**Bonus (advanced):** If you have GitHub access, put your `my-context.md` in a private GitHub repo of your own. Then try pointing a different AI tool at it and see how much better its first answer is.

> **Before you're done — Question It:** What did Claude assume? What's missing? What could break?

**Success criteria:** Added tools/systems section to context file and got Claude's gap analysis.
