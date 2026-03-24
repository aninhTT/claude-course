---
module: 3
lesson: 4
title: "Build Your First Skill"
difficulty: intermediate
prerequisites: "3.03"
---

# Lesson 3.04: Build Your First Skill

## Learn

You've copied and customized a skill. Now it's time to build one from scratch. We're going to take something you've already done in this course and turn it into a reusable skill.

### The SKILL.md Pattern

A skill is just a markdown file with a clear structure:

```markdown
---
name: skill-name
description: "What this skill does in one sentence"
---

# Skill Name

## Steps

1. First, do this...
2. Then check for...
3. Compile the results into...
4. Output as...

## Error Handling

If step 2 fails, try...
If no data is found, respond with...
```

That's it. The frontmatter tells Claude what the skill is called and what it does. The steps tell Claude exactly how to execute it. Error handling tells Claude what to do when things go wrong.

### What We're Building: A Morning Briefing Skill

Remember the Cowork task from Module 2 — where you had Cowork index your Slack, email, and Granola for the last 2 days and compile what you need to know? We're going to turn that into a **reusable skill** called `morning-briefing`.

This means instead of typing out those instructions every time, you'll just run `/morning-briefing` and it happens automatically.

### Why This Matters

This is the core pattern of productivity with Claude: **do something once, then make it repeatable.** Every time you find yourself giving Claude the same instructions, that's a skill waiting to be created.

## Practice

You can build this skill in **either Cowork or Claude Code** — both work. The key difference:

- **In Cowork:** Describe what you want the skill to do. Include in your prompt: "Share the skill draft with me before you create the final file — I want to review and refine it first."
- **In Claude Code:** Switch to **plan mode** first (the dropdown in the chat input area). Claude will plan the skill structure, you'll review the plan, and then Claude builds it.

Either way, the goal is the same: don't just let Claude create the skill blindly. **Review before it finalizes.**

Let's build the morning-briefing skill step by step.

**Step 1: Create the SKILL.md file.**

Ask Claude to create a morning-briefing skill. Start with this prompt and customize it for your role:

> "Create a morning-briefing skill for me. **Share the draft with me before creating the final file** — I want to review it first. Here's what it should do:
>
> 1. Check my Slack messages and mentions from the last 2 days
> 2. Scan my Gmail inbox for anything time-sensitive or needing a response
> 3. Check my Granola meeting notes for recent decisions and action items
> 4. Compile everything into a summary organized by urgency:
>    - Needs action today
>    - Needs attention this week
>    - FYI / good to know
> 5. Send the summary as a Slack message to me
>
> Make it a proper SKILL.md with frontmatter, clear steps, and error handling.
> My role is [your role]."

Save it in `workspace/` (or in `.claude/commands/` if you want it as a slash command right away).

**Step 2: Review the draft.**

Read what Claude shared with you. Check:
- Are the steps clear and specific?
- Does it use the right connectors?
- Is the output format what you want?
- Is there error handling (what if Slack is down? What if there are no new messages)?

**Step 3: Customize and refine.**

Tell Claude to adjust anything that doesn't match your needs. Maybe you want it to also check your calendar. Maybe you want a different output format. Iterate until you're happy, then have Claude create the final file.

**Step 4: Test it.**

Run the skill and see what happens. Does it produce the summary you expected?

**Success criteria:** Created a morning-briefing SKILL.md with frontmatter, at least 4 workflow steps, error handling, and a clear output format. Reviewed the draft before finalizing. Tested it at least once.

## Challenge

Make your morning-briefing skill even better:

1. Add a slash command trigger so you can run it with `/morning-briefing`
2. Add a section for **customization** — make it easy to change the timeframe (last 1 day vs last 2 days) or the delivery method (Slack vs document)
3. Test running it both ways: manually via slash command AND by just asking Claude "give me my morning briefing" to see if it auto-loads

**Success criteria:** Skill works via slash command, has customization options, and Claude can auto-detect when to use it.

---

> 🎉 **Midway milestone!** You've completed the first half of the course. Nice work! You've gone from understanding the tools to actually building reusable skills.
>
> If you have a moment, filling out this quick form helps us improve the course: https://forms.gle/74iMkRWDVPw5ffQP9
