---
module: 3
lesson: 1
title: "What Are Skills & Plugins?"
difficulty: beginner
prerequisites: "2.05"
videos:
  - url: "https://www.loom.com/share/2dff9697e5b8478da2f597aa4b76c0c7"
    title: "Skills Overview"
    duration: "~5 min"
    context: "Watch this for an overview of skills and plugins"
---

# Lesson 3.01: What Are Skills & Plugins?

## Learn

You've used Claude Code to build things and Cowork to execute tasks. But so far, every task has been one-off — you describe what you want, Claude does it, and that's it. What if you could save those workflows so Claude does them the same way every time you ask? That's where **skills** come in.

> Already comfortable with this topic? Skip ahead anytime with `skip` followed by the next lesson number.

There's a short video that walks through skills and plugins visually if you'd like to see them in action: https://www.loom.com/share/2dff9697e5b8478da2f597aa4b76c0c7

### What Is a Skill?

A **skill** is a reusable workflow written down in a SKILL.md file. Think of it like a saved playbook: you define the steps, and Claude follows them.

A skill can:
- **Load on its own** when what you're asking matches what it's for
- **Run when you ask** for it by name, in plain language
- **Run on a schedule**, like every weekday at 8am

### Think of It Like a Custom GPT or Gem — But Way More Powerful

If you've used Custom GPTs (ChatGPT) or Gems (Google), skills are like that — but significantly more powerful. Here's why:

- Skills can **access all your connected tools** (Slack, Gmail, Calendar, Jira, etc.)
- Skills can **read and write files** on your computer
- Skills can **run scripts and code** — not just chat
- Skills can **run on a schedule** automatically
- Skills work in **both Claude Code and Cowork**

A Custom GPT can only chat. A skill can actually *do things*.

### A Key Superpower: Auto-Loading

Claude is smart — it often knows when a skill applies based on what you're doing. If you have a skill for meeting prep and you mention an upcoming meeting, Claude may automatically load it. You don't always need to explicitly trigger skills.

That's why, in Cowork, you rarely need anything special to use a skill. You just ask in plain language — "prep me for my 2pm" — and Cowork picks up the right skill.

### What Is a Plugin?

Now that you know what a skill is, a plugin is easy. A **plugin** is a bundle: install one plugin and you get several things at once. A plugin can include:

1. **Skills** — often several related skills, like a set for sales or a set for recruiting
2. **Connectors** — integrations with tools like Slack, Gmail, Jira, or BigQuery. You set some of these up in Module 1.
3. **Subagents** — specialized helpers Claude can hand work to. You'll meet these in Module 8.

In Claude Code, plugins can also add things like **hooks** (rules that run automatically) — power-user features you don't need yet.

So: **a skill is one playbook. A plugin is a box of playbooks and the tools they need.**

### Where to Find Skills and Plugins

In the Claude app, open **Customize** to browse and manage your skills, connectors, and plugins in one place. Your organization can also share skills and plugins with everyone — some are available to install, and some come installed by default. You'll go deeper on this in the next lesson.

### Skills in Cowork vs Claude Code

Skills behave slightly differently depending on where you use them:

- **In Cowork**, you just ask. Cowork follows the skill's steps as part of a task — gathering information, generating output, and delivering results. No commands to remember.
- **In Claude Code**, you interact with skills more directly. You can trigger them with slash commands (like `/morning-briefing`), watch them run, and iterate on the results. It's more hands-on.

Both use the same SKILL.md format, so a skill you create works in either place.

> 💡 **What about slash commands?** In Claude Code, when you type `/` and see a list, those are commands. These days a slash command is simply a way to run a skill. Older "command" files still work, but new ones are written as skills.

### What's Ahead

This module gives you the primer — enough to understand skills, find them, copy one, and build your first. **Module 6 (Intermediate Skills)** goes much deeper into custom skill creation, connecting skills together, and advanced patterns.

> ⏭️ **Already familiar with skills?** Feel free to `/skip 3.03` to jump to building.

## Practice

Let's see what you already have — starting in Cowork, where you don't need any commands.

**Step 1: Open Cowork.** If you're taking this course in Cowork, just ask right here. If you're in Claude Code, start a new Cowork task the way you did in Module 2, then come back here to share what you found.

**Step 2: Ask what skills you have.** Type:

> "What skills do I already have available? For each one, tell me in one sentence what it does and when I'd use it."

**Step 3: Ask which ones came from a plugin.** Follow up with:

> "Which of these came from a plugin, and what else does that plugin include?"

**Step 4: Ask about your connectors.** Then ask: "What connectors do I have connected?"

**Step 5: Reflect.** Pick two skills from the list. When would each one be useful — daily, weekly, occasionally?

**Optional:** Back in Claude Code, type `/` to see many of the same skills listed as slash commands.

**Success criteria:** Asked Cowork what skills are available, can name at least 1 skill and 2 connectors, and can explain the difference between a skill and a plugin.

## Challenge

Think about your typical work week. Identify **one recurring task** you do at least weekly that follows the same steps each time. Describe how it could be captured as a skill:
1. What the task is
2. How it should start (you ask for it, it loads on its own, or it runs on a schedule)
3. What connectors/tools it would need
4. What the output should look like

Don't build it yet — just describe the concept.

> **Before you're done — Question It:** What did Claude assume? What's missing? What could break?

**Success criteria:** Described one potential skill idea with clear purpose, trigger, required tools, and expected output.
