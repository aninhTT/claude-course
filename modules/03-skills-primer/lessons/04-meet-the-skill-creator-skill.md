---
module: 3
lesson: 4
title: "Meet the Skill Creator Skill"
difficulty: beginner
prerequisites: "3.03"
---

# Lesson 3.04: Meet the Skill Creator Skill

## Learn

Before you build your first skill from scratch, there's a tool that's going to make it a lot easier: the **skill-creator skill**. It's a meta-skill — a skill that helps you build other skills.

Here's what makes it powerful: instead of staring at a blank SKILL.md file trying to remember the right structure, you describe what you want in plain language and the skill-creator generates a properly structured skill for you. It knows the SKILL.md format, the right frontmatter fields, how to write clear workflow steps, and how to structure error handling.

### What the Skill Creator Does

When you trigger it, the skill-creator will:

1. Ask you what workflow you want to build
2. Help you scope it clearly (is this one skill or two?)
3. Generate a complete SKILL.md with proper structure
4. Walk you through reviewing and refining it

It's also a great study tool — the skills it generates show you exactly what a well-structured SKILL.md looks like.

### Installing It

The skill-creator is a pre-made skill available in the skill bank. To install it:

**In Claude Code:**
1. Open Claude Code settings
2. Go to Skills (or Plugins)
3. Find "skill-creator" in the available skills list
4. Add it to your session

**In Cowork:**
1. Open Cowork
2. Go to your skills panel
3. Search for "skill-creator"
4. Add it to your skill library

Once installed, you can trigger it two ways:
- **Slash command:** `/skill-creator`
- **Natural language:** Just say "I want to build a skill that..." and Claude will auto-detect and use it

### What the Trigger Description Looks Like

Every skill has a `description` field in its YAML frontmatter — this is what Claude reads to decide when to auto-detect the skill. Here's roughly what skill-creator's trigger looks like:

```yaml
description: >
  Create new skills, modify and improve existing skills, and measure skill performance.
  Use when users want to create a skill from scratch, edit, or optimize an existing skill...
```

Notice how it's written as a use-case description, not a list of features. This is what makes auto-detection work — Claude matches your request against this description. You'll use the same pattern when you write your own skills.

### What Happens Next

In the next lesson (3.05), you'll build your first skill from scratch. When you get there, try using the skill-creator to scaffold it — you'll see the structure it produces and then customize it for your specific workflow.

---

## Practice

Let's get the skill-creator installed and make sure it works.

**Step 1:** Install the skill-creator skill using the instructions above (Claude Code settings or Cowork skill panel).

**Step 2:** Confirm it loaded by running:
```
/skill-creator
```
Or just say: "I want to build a skill."

**Step 3:** When it responds, observe the structure: How does it ask for your workflow? What questions does it ask? What does the generated SKILL.md look like?

You don't need to build a full skill right now — just explore. Run it with a simple test idea and see what it produces.

**Success Criteria:**
- Skill-creator is installed and responds to `/skill-creator` or a natural language trigger
- You've seen at least one generated skill scaffold
- You recognize the SKILL.md structure from what you've learned

---

## Challenge

Use the skill-creator to generate a skeleton for a task you do every week. Pick something real — not a throwaway example.

**The goal isn't to finish the skill.** Just get the scaffold and review it:
- Does the structure make sense for your workflow?
- Are the steps in the right order?
- What would you change?

Save the generated SKILL.md to `workspace/skills/` with a folder name that follows verb-noun convention (e.g., `workspace/skills/draft-standup/SKILL.md`).

You'll polish this skill properly in later lessons — for now, just get a real foundation in place.

**Success Criteria:**
- Generated a skill scaffold for a real weekly task
- Saved it to `workspace/skills/`
- Identified at least 2 things you'd want to change or improve

> **Hint system:** Use `/hint` if you're stuck. First hint is a nudge, second is more specific, third nearly gives it away.
