---
module: 3
lesson: 3
title: "Copy Your First Skill"
difficulty: beginner
prerequisites: "3.02"
videos:
  - url: "https://www.loom.com/share/26c3141dd7884bd4a8de1f7fcbcef6b6"
    title: "What Copying a Skill Looks Like"
    duration: "~3 min"
    context: "Here's what copying a skill looks like. It uses a different skill from the one in this lesson, but it gives you a sense for working with skills."
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

Want to see what copying a skill looks like first? Here's a quick demo (~3 min): https://www.loom.com/share/26c3141dd7884bd4a8de1f7fcbcef6b6. It uses a different skill from the one you'll copy below, but the steps are the same.

### Where to Put Copied Skills

Each skill lives in its own folder with a SKILL.md file inside, in one of two places:
- **`.claude/skills/`** in your project folder — Available in that project
- **`~/.claude/skills/`** in your home directory — Available everywhere

(You may also see skills saved as single files in `.claude/commands/` — that's the older format, and it still works. This course's own commands live there.)

For this exercise, we'll put skills in the course's `workspace/` folder so you can see them clearly.

### The Skill You'll Copy: Clean Draft

**Clean Draft** reviews the quality of AI output. Paste in a draft — from Claude, ChatGPT, Codex, or written by hand — and it turns it into something a busy reader can read once and act on.

It makes two passes:
- **Structure:** puts the recommendation first, narrows the options to two or three (each with its cost), names an owner for every ask, and cuts what the reader doesn't need.
- **Sentences:** one idea per sentence, plain words, a named actor, and no stock AI phrases like "Here's the thing," "move the needle," or "Hope this helps."

It edits form, not facts. If the draft is missing an owner, a date, or a recommendation, it flags the gap for you instead of inventing one. A built-in readability checker reviews the draft before and after.

In short: **Clean Draft helps you avoid AI slop.** Use it on docs, pull requests, emails, Slack posts — anything you're about to send to another person.

### Getting the Skill

Clean Draft is listed in Thumbtack's AI Marketplace: https://ai-marketplace-sbqrdzy4sa-uw.a.run.app/?tool=curated%3Askill%3Aclean-draft

The Marketplace page links to the skill's home on Thumbtack's GitHub: https://github.com/thumbtack/shared-skills/tree/main/users/tsalman/clean-draft

You'll copy it from GitHub, so you'll need access to Thumbtack's GitHub. If you don't have it yet, request GitHub access and complete the certification training. You'll use GitHub again later in the course, so it's worth setting up.

Once you have access, the easiest path is to ask Claude:

> "Copy the clean-draft skill from https://github.com/thumbtack/shared-skills/tree/main/users/tsalman/clean-draft into `workspace/skills/clean-draft/`. Include the scripts folder."

Or clone the whole shared skills repo yourself and find the skill in `users/tsalman/clean-draft/`:

```
git clone https://github.com/thumbtack/shared-skills
```

## Practice

You're going to copy **Clean Draft**, study how it's built, and then run it on something real.

**Step 1: Get the skill.**

Ask Claude to copy it in from GitHub (see **Getting the Skill** above). If you cloned the repo yourself, ask Claude to copy `users/tsalman/clean-draft/` into your workspace.

Then check where it lands. It should be in `workspace/skills/clean-draft/`, with `SKILL.md`, `README.md`, and a `scripts/` folder inside. Make sure the `scripts/` folder came along — the skill needs it for its readability checker.

**Step 2: Read and analyze the skill.**

Open the SKILL.md and study it carefully. Discuss with Claude:

- What does the frontmatter description tell you? When should this skill load — and when should it *not*?
- How many steps are in the workflow, and what does each one do?
- What inputs does the skill expect?
- What does it give you back?
- What happens when the draft is missing something, like an owner or a date?
- What's in the `scripts/` folder, and why would a skill include a script?
- Could you modify this skill for your own work? What would you change?

**Step 3: Identify the patterns.**

Look at how the skill is structured. Notice:
- Each step in the workflow is a single, clear action
- Inputs and outputs are explicitly defined
- It's clear about its limits — it edits form, not facts, and says what it won't do
- The description is specific enough that Claude knows exactly when to use it

These patterns are what make a skill reliable and reusable.

**Step 4: Run the skill!**

Now actually use it on something you need anyway. Try one of these:

- **A doc** you're drafting — a brief, a proposal, a recap
- **A pull request description**, if you write code
- **An email or Slack post** you're about to send
- **Something Claude wrote for you** earlier in this course — the perfect test for AI slop

For example:

> "Use the clean-draft skill on this email to my team. The audience is the other team leads: [paste your draft]"

Compare the before and after. Read the list of **gaps** it flagged. Those are things only you can fill in.

> 💡 **About the checker:** Clean Draft runs a small Python script to check readability. If Claude says it can't run the script, it can still do both editing passes — or ask Claude to help you get the checker working.

**Success criteria:** Copied the Clean Draft skill (including its `scripts/` folder) into your workspace, read through it carefully, can explain what each section does, ran it on a real draft, and reviewed the gaps it flagged.

## Challenge

Now customize the copied skill. Make at least 3 changes that make it more useful for your specific work:

- Add phrases your team overuses to the list of things to cut
- Set a default audience (for example, "assume this goes to my team's leads")
- Add a rule for the kind of writing you do most — launch emails, PR descriptions, weekly updates
- Change the output, like making "review only, don't rewrite" the default
- Adjust the trigger phrases in the description so it loads when you'd expect

After customizing, run it again on the same draft and compare the output to the original.

> **Before you're done — Question It:** What did Claude assume? What's missing? What could break?

**Success criteria:** Made at least 3 meaningful customizations to the copied skill and tested the modified version.
