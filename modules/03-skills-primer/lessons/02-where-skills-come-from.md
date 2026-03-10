---
module: 3
lesson: 2
title: "Where Skills Come From"
difficulty: beginner
prerequisites: "3.01"
---

# Lesson 3.02: Where Skills Come From

## Learn

Before you build a skill from scratch, you should know: **you don't always have to start from zero.** Skills come from three places, and knowing all three saves you a ton of time.

### 1. Skills Already Created (Pre-Made)

Some skills come built-in or are available through your organization's setup. These are ready to use — just find them and run them.

To discover what's already available:
- Type `/` in Claude Code to see all available slash commands
- Ask Claude: "What skills are available to me?"
- Browse `.claude/` directories for SKILL.md files

The course commands you've been using (`/course`, `/lesson`, `/hint`) are themselves skills — they follow the exact same SKILL.md pattern.

### 2. Copy Someone Else's Skill

This is often the fastest path. If a colleague has built a skill that's useful — or you find one online — you can **copy it and make it your own.**

How to copy a skill:
- **Pull the folder in** — If someone shares their skill folder, just drag it into your `.claude/` directory
- **Clone a GitHub repo** — If the skill lives on GitHub, clone it. Claude can help: "Clone this repo for me: [URL]"
- **Copy the SKILL.md file** — At its simplest, just copy the SKILL.md file into your `.claude/commands/` folder

The beauty of copying: **you can always modify it.** Someone's morning briefing skill might check Slack and email — but maybe you also want it to check Granola. Copy it, then tweak it. This is the fastest way to get a working skill that fits your needs.

### 3. Build Custom From Scratch

When no existing skill fits, you build your own. You'll do this in Lessons 3 and 4. Building from scratch gives you full control but takes more effort.

**The smart approach:** Start by looking for something to copy. Modify if possible. Only build from scratch when you need something truly custom.

### Reading a SKILL.md File

When you find a skill (yours or someone else's), here's what to look for:

- **Name/Description** — What it does in plain language
- **Steps** — The actual workflow Claude follows
- **Trigger** — How it's activated (slash command, auto-load, schedule)
- **Connectors needed** — What tools it uses

Reading a SKILL.md before running it is a good habit. No surprises.

> ⏭️ **Already know this?** Skip ahead to Lesson 3 to start copying your first skill: `/skip 3.03`

## Practice

Let's explore all three sources of skills.

**Step 1: Find pre-made skills.** Type `/` in Claude Code and browse what's available. List at least 3 skills or commands you see. For each one, note: what it does and when you'd use it.

**Step 2: Read a SKILL.md.** Pick one skill and ask Claude to show you its full definition. Read through the steps. Note:
- What does it do step by step?
- What connectors does it use?
- What's the output?

**Step 3: Find a skill to copy.** Ask Claude: "Are there any existing skills or templates I could copy and customize for [describe what you need]?" See what Claude suggests.

**Success criteria:** Found and listed at least 3 available skills, read one SKILL.md in detail, and identified one skill they could copy/customize.

## Challenge

Find a skill that's **close to something you need but not quite right.** Describe:
1. What the skill does well
2. What you'd change (at least 2 modifications)
3. Whether you'd copy-and-modify it or build from scratch

This is direct prep for the next lesson where you'll actually copy a skill.

**Success criteria:** Identified a specific skill and described at least 2 concrete modifications to make it fit their use case.
