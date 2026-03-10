---
module: 4
lesson: 2
title: "Copy a Use Case Skill"
difficulty: intermediate
prerequisites: "4.01"
---

# Lesson 4.02: Copy a Use Case Skill

## Learn

You've given Claude your full context. Now let's put it to work — by copying a real use case skill and using it as a springboard to identify YOUR top use cases.

### Why Copy Before You Create?

Starting from a blank page is hard. Starting from a working example is fast. The best way to learn what a use case skill looks like — and to spark ideas for your own — is to study one that already works.

Here's the flow:
1. **Copy a working skill** — Get a real skill into your workspace
2. **Read and understand it** — See how it's structured and what it does
3. **Run it** — See the output in action
4. **Use it as inspiration** — Ask "What would MY version of this look like?"

### What You'll Copy

We've shared a **use case skill** in the Skill Bank — the same place you got the brand design skill in Module 3. This time you'll copy a different skill, study it, and use it as inspiration for brainstorming your own use cases.

### The Prioritization Filter

Once you've seen what a use case looks like in practice, you'll brainstorm your own. Not every idea is worth building. Prioritize by:

1. **Frequency** — How often do you do this? (Daily > Monthly)
2. **Time cost** — How long does it take? (30 min > 5 min)
3. **Tedium** — How boring is it? (High tedium = high value to automate)
4. **Feasibility** — Can Claude actually do this well with your connected tools?

The sweet spot: **frequent, time-consuming, tedious, and feasible**.

## Practice

**Step 1: Get the use case skill.**

Go back to the Skill Bank you downloaded in Module 3:

**Google Drive:** https://drive.google.com/drive/folders/1IjvOYsbWyrVrkki8OWnnQxh1NYEmNt-Y?usp=sharing

**GitHub (if you have it):** https://github.com/aninhTT/skill-bank

Find the use case skill folder and drag it into your Claude Code session (or copy it in). Make sure you know what folder it lands in — check that it's in `workspace/skills/` or wherever you're keeping your skills.

> If you already downloaded the zip in Module 3, you already have it! Just find the use case skill folder in what you unzipped.

**Step 2: Read and understand it.**

Study the SKILL.md. Discuss with Claude:
- What does the frontmatter tell you?
- How many steps are there, and what does each one do?
- What inputs does it expect?
- What does it produce as output?
- What happens when something goes wrong?
- What would you change to make this fit YOUR team or workflow?

**Step 3: Make it yours.**

Remember the `my-context.md` file you created in Lesson 4.01? This is where it pays off. Feed your context file into Claude along with the use case skill and ask Claude to help you refine the skill for YOUR role and workflows. The generic use case skill is a great starting point — but a version that knows about your team, your tools, and your recurring tasks will generate much better ideas.

> Try something like: "Here's a use case skill and here's my context file. Help me modify this skill so it generates use cases specifically tailored to my role and workflows."

**Step 4: Brainstorm YOUR use cases.**

Now, using your context file from Lesson 4.01, work with Claude to brainstorm use cases for YOUR work. Think across three levels:

**Level 1: Individual Productivity** — Tasks you do alone that AI can speed up:
- Drafting recurring communications
- Compiling information from multiple sources
- Prepping for meetings
- Processing inbox/Slack backlog

**Level 2: Team Workflows** — Processes your team runs:
- Handoffs between team members
- Regular team reporting
- Knowledge management
- Onboarding

**Level 3: Automation Candidates** — Recurring tasks that could run on a schedule:
- Daily/weekly digests
- Monitoring for patterns
- Scheduled reports

Ask Claude to help you brainstorm at least 10 opportunities across all three levels, then score each on the four criteria (frequency, time cost, tedium, feasibility).

**Step 5: Pick your top 3.**

For your top 3 use cases, write a one-sentence description of what the AI-powered version would look like. Save everything as `workspace/use-case-ideas.md`.

**Success criteria:** Copied and studied the use case skill from the Skill Bank, brainstormed at least 10 use case ideas, scored them, and identified your top 3 with descriptions saved to workspace.

## Challenge

For your top use case, map out the full workflow:
- **Current state:** How do you do this today, step by step?
- **AI-assisted state:** How would it work with Cowork or Claude Code?
- **Which steps does AI handle?** Which stay human?

This comparison becomes the blueprint for what you'll build in Module 6.

**Success criteria:** Created a current vs. AI-assisted workflow comparison for your top use case.
