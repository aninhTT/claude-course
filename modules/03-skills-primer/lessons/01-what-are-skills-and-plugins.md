---
module: 3
lesson: 1
title: "What Are Skills & Plugins?"
difficulty: beginner
prerequisites: "2.04"
videos:
  - url: "https://www.loom.com/share/2dff9697e5b8478da2f597aa4b76c0c7"
    title: "Skills Overview"
    duration: "~5 min"
    context: "Watch this for an overview of skills and plugins"
---

# Lesson 3.01: What Are Skills & Plugins?

## Learn

You've used Claude Code to build things and Cowork to execute tasks. But so far, every task has been one-off — you describe what you want, Claude does it, and that's it. What if you could save those workflows so they run again with a single command? That's where **plugins** come in.

There's a short video that walks through skills and plugins visually if you'd like to see them in action: https://www.loom.com/share/2dff9697e5b8478da2f597aa4b76c0c7

### What Are Plugins?

**Plugins** is the umbrella term for all the extensions that make Claude Code and Cowork more powerful. There are three types:

1. **Skills** — Reusable workflows defined in SKILL.md files. Think of them like saved playbooks. You define the steps, and Claude follows them. Skills can be triggered with a slash command (like `/daily`), auto-loaded when relevant, or scheduled to run on their own.

2. **Commands** — Slash commands that trigger specific actions. Some are built into the system, others come from skills you create. When you type `/` and see a list, those are commands.

3. **Connectors** — Integrations with external tools (Slack, Gmail, Google Calendar, Jira, BigQuery, Granola, etc.) via MCP. They give Claude eyes and hands for your tools. You already set these up in Module 1.

### Think of It Like a Custom GPT or Gem — But Way More Powerful

If you've used Custom GPTs (ChatGPT) or Gems (Google), skills are like that — but significantly more powerful. Here's why:

- Skills can **access all your connected tools** (Slack, Gmail, Calendar, Jira, etc.)
- Skills can **read and write files** on your computer
- Skills can **run scripts and code** — not just chat
- Skills can **run on a schedule** automatically
- Skills work in **both Claude Code and Cowork**

A Custom GPT can only chat. A skill can actually *do things*.

### Skills in Cowork vs Claude Code

Skills behave slightly differently depending on where you use them:

- **In Cowork**, skills run as part of autonomous task execution. Cowork follows the skill's steps as part of a task — indexing tools, generating output, delivering results without needing your input.
- **In Claude Code**, you interact with skills more directly. You trigger them with slash commands, watch them execute, and iterate on the results. It's more hands-on.

Both environments use the same SKILL.md format, so a skill you create works in either place.

### A Key Superpower: Auto-Loading

Claude is smart — it often knows when a skill applies based on what you're doing. If you have a skill for meeting prep and you mention an upcoming meeting, Claude may automatically load it. You don't always need to explicitly trigger skills.

That said, you can also:
- **Trigger manually** with a slash command (e.g., `/morning-briefing`)
- **Schedule to run** automatically on a recurring basis (e.g., every weekday at 8am)

### What's Ahead

This module gives you the primer — enough to understand skills, find them, copy one, and build your first. **Module 4 (Intermediate Skills)** goes much deeper into custom skill creation, connecting skills together, and advanced patterns.

> ⏭️ **Already familiar with skills?** Feel free to `/skip 3.03` to jump to building.

## Practice

Let's take stock of what you already have and what's available.

**Step 1: List your connectors.** What tools did you connect in Module 1? If you're not sure, ask Claude: "What connectors do I have available?"

**Step 2: Find available skills.** In Claude Code, type `/` to see available slash commands — many of these are skills. Also ask Claude: "What skills are available to me?"

**Step 3: Reflect.** For each skill you found, consider: When would this be useful? Daily, weekly, occasionally?

**Success criteria:** Can identify at least 2 connectors and 1 skill/command in their environment.

## Challenge

Think about your typical work week. Identify **one recurring task** you do at least weekly that follows the same steps each time. Describe how it could be captured as a skill:
1. What the task is
2. What trigger makes sense (slash command, scheduled, auto-load)
3. What connectors/tools it would need
4. What the output should look like

Don't build it yet — just describe the concept.

**Success criteria:** Described one potential skill idea with clear purpose, trigger, required tools, and expected output.
