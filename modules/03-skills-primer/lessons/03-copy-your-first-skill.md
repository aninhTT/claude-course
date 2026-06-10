---
module: 3
lesson: 3
title: "Copy Your First Skill"
difficulty: beginner
prerequisites: "3.02"
videos:
  - url: "https://www.loom.com/share/26c3141dd7884bd4a8de1f7fcbcef6b6"
    title: "Brand Guidelines Skill Demo"
    duration: "~3 min"
    context: "Watch this to see what the brand design skill does in action"
---

# Lesson 3.03: Copy Your First Skill

## Learn

The fastest way to get a working skill is to copy one that already exists and customize it. In this lesson, you'll do exactly that — copy a real skill, understand its structure, and then actually run it.

> Already comfortable with this topic? Skip ahead anytime with `skip` followed by the next lesson number.

### The Copy-and-Customize Flow

1. **Find the skill** — Get the source (folder, GitHub repo, or shared file)
2. **Copy it into your environment** — Put it where Claude can find it
3. **Read and understand it** — Know what it does before you change anything
4. **Run it** — See it in action
5. **Customize it** — Modify the steps, connectors, output, or trigger to fit your needs

### Where to Put Copied Skills

Skills go in one of two places:
- **`.claude/commands/`** in your project folder — Available in that project
- **`~/.claude/commands/`** in your home directory — Available everywhere

For this exercise, we'll put skills in the course's `workspace/` folder so you can see them clearly.

### Getting Skills from Others

We've shared a small **Skill Bank** with sample skills you can copy. There are two ways to get them:

**Option A: Download from Google Drive (recommended for most people)**

Download the zip folder from here: https://drive.google.com/drive/folders/1IjvOYsbWyrVrkki8OWnnQxh1NYEmNt-Y?usp=sharing

Then unzip it on your computer. You'll see individual skill folders inside.

**Option B: Clone from GitHub (if you have GitHub)**

If you already have a GitHub account (if you're not sure, you probably don't — and that's totally fine), you can clone the shared skills repo:

```
git clone https://github.com/thumbtack/shared-skills
```

The sample skills live in `users/amies-skill-bank/` inside the repo — you can also [browse them on GitHub](https://github.com/thumbtack/shared-skills/tree/main/users/amies-skill-bank).

> Most Thumbtack employees don't have GitHub set up yet. If that's you, just use Option A — the Google Drive download. You'll learn about GitHub in Module 7 if you're interested.

## Practice

You're going to copy a real skill — the **Brand Design skill** from the Skill Bank — study how it's built, and then run it.

Here's a quick video showing what this skill does: https://www.loom.com/share/26c3141dd7884bd4a8de1f7fcbcef6b6

**Step 1: Get the skill.**

If you downloaded the zip folder, find the brand design skill folder inside. Drag the entire folder into your Claude Code session — Claude will copy it into your workspace. Make sure you know where it lands! Check that it's in `workspace/skills/` or wherever you want to keep it.

If you cloned the repo, navigate to the brand design skill folder inside `users/amies-skill-bank/`.

Either way, make sure the SKILL.md file is somewhere Claude can see it in this session.

**Step 2: Read and analyze the skill.**

Open the SKILL.md and study it carefully. Discuss with Claude:

- What does the frontmatter tell you about this skill?
- How many steps are there, and what does each one do?
- What inputs does the skill expect?
- What does the skill produce as output?
- What happens if something goes wrong? How does it handle errors?
- Could you modify this skill for your own work? What would you change?

**Step 3: Identify the patterns.**

Look at how the skill is structured. Notice:
- Each step is a single, clear action
- Error handling covers realistic failure scenarios
- Inputs and outputs are explicitly defined
- The description is specific enough that Claude (or a person) could follow it

These patterns are what make a skill reliable and reusable.

**Step 4: Run the skill!**

Now actually use it — have it do something. Try one of these:

- **Build a deck** for an upcoming meeting using Thumbtack's brand guidelines
- **Create a one-page PDF** about Thumbtack — what it is, what it does
- **Write and lay out a blog post** following the brand style

Give it a real task and see what it produces. Notice how the skill's instructions guide Claude's output.

**Success criteria:** Copied the brand design skill into your workspace, read through it carefully, can explain what each section does, and ran the skill to produce real output.

## Challenge

Now customize the copied skill. Make at least 3 changes that make it more useful for your specific work:

- Change the output format
- Add or remove a step
- Change which connectors it uses
- Adjust the trigger (slash command name)
- Modify the instructions to match your team's style

After customizing, run it again and compare the output to the original.

> **Before you're done — Question It:** What did Claude assume? What's missing? What could break?

**Success criteria:** Made at least 3 meaningful customizations to the copied skill and tested the modified version.
