---
module: 5
lesson: 1
title: "Creating Custom Skills"
difficulty: intermediate
prerequisites: "4.04"
---

# Lesson 5.01: Creating Custom Skills

## Learn

In Module 3, you built your first skill — probably a morning briefing or something similar. That was the primer. Now we go deeper into what makes a skill actually good, and how to build ones that you'll rely on every day.

### What Is a Skill, Really?

A skill is a reusable set of instructions stored as a SKILL.md file. When triggered, Claude reads those instructions and follows them step by step. Think of it as a recipe — anyone (or any Claude session) can pick it up and execute it consistently.

What makes a skill different from just typing instructions into chat:

- **Reusable** — run it again tomorrow without retyping anything
- **Triggerable** — activate it with a slash command or let Claude auto-detect when it's relevant
- **Shareable** — hand it to a teammate and they get the same workflow
- **Consistent** — same steps every time, reducing variability

### The SKILL.md Anatomy

A well-structured SKILL.md has these parts:

**YAML Frontmatter**
```yaml
---
name: "Weekly Team Summary"
description: "Generates a summary of the team's work from the past week"
command: "/weekly-summary"
---
```

The frontmatter tells Claude (and humans) what this skill does at a glance. The `command` field creates a slash command trigger.

**Workflow Steps**
Numbered, clear instructions that Claude follows in order. Each step should be a single action or decision.

```markdown
## Steps

1. Check the current date and calculate the date range for the past 7 days.
2. Search Slack channels #team-updates and #shipped for messages from the past week.
3. Search Jira for issues that were moved to "Done" in the past week.
4. Group the findings by team member.
5. Write a summary with these sections:
   - Highlights (top 3 accomplishments)
   - Completed work (grouped by person)
   - Blockers or carry-overs
6. Format the summary for posting in Slack.
```

**Error Handling**
What should Claude do when something goes wrong? This is the part most people skip — and then wonder why their skill fails silently.

```markdown
## Error Handling

- If a Slack channel is not accessible, note it in the summary and continue with available channels.
- If Jira is unreachable, ask the user if they want to proceed with Slack data only.
- If no updates are found for a team member, list them under "No updates this week" rather than omitting them.
```

**Inputs and Outputs**
What does the skill need to run? What does it produce?

```markdown
## Inputs
- Time range (defaults to past 7 days)
- Team channel name (defaults to #team-updates)

## Output
- Formatted summary ready to paste into Slack
```

### Designing Good Skills

The difference between a skill you use once and a skill you use every week comes down to design:

- **Scope it clearly.** A skill can absolutely have many steps — that's fine. What matters is that each step serves a single, well-defined purpose. Don't try to cram a bunch of unrelated tasks into one skill. A 15-step skill that does one job well is great. A 5-step skill that tries to do three different things is a mess. When in doubt: if you're describing what the skill does and need the word "and" connecting two different goals, consider splitting it. Use Claude to help you scope — describe what you want and let Claude help you decide if it's one skill or two.
- **Clear inputs and outputs.** A skill that needs you to explain what it should do every time isn't saving you time.
- **Graceful failure.** The real world is messy — channels get renamed, APIs time out, data is missing. Plan for it.
- **Test it immediately.** Don't write a 50-step skill and test it for the first time a week later. Build incrementally.

### Iterating on Skills

Your first version will not be perfect. That's fine. The pattern is:

1. Write v1 with the core workflow
2. Run it and see what happens
3. Notice what's missing or wrong
4. Update the instructions
5. Repeat

Most good skills go through 3-5 iterations before they're solid.

---

## Practice

Build a custom skill that's actually useful for your daily work. This should be **different** from whatever you built in Module 3.

> 💡 **Remember your use-case skill!** In Module 4, you copied and customized a use-case skill that knows about your role and workflows. If you're not sure what to build here, run that skill first — it'll generate tailored ideas based on your context. It's a great way to pick your next skill.

**Ideas to consider:**
- **Meeting prep:** Pull context from calendar, recent Slack threads, and docs before a meeting
- **Email triage:** Scan inbox, categorize messages, draft responses for routine ones
- **Daily standup draft:** Gather what you did yesterday, what's planned today, any blockers
- **Project status update:** Pull data from multiple sources into a formatted update
- **Research summary:** Given a topic, search internal docs and summarize findings

**Step 1:** Pick a workflow you do at least weekly. Something that takes 10-30 minutes manually.

**Step 2:** Create the SKILL.md file at `workspace/skills/your-skill-name/SKILL.md`. Include:
- YAML frontmatter with name, description, and a slash command
- At least 4 numbered workflow steps
- An error handling section with at least 2 failure scenarios

**Step 3:** Read through your skill as if you were Claude encountering it for the first time. Are the steps clear? Is anything ambiguous?

**Step 4:** Test it by triggering the slash command or describing the task to Claude.

**Success Criteria:**
- Created a SKILL.md with proper YAML frontmatter (name, description, command)
- Includes at least 4 clear workflow steps
- Has an error handling section with at least 2 scenarios
- Tested the skill at least once

---

## Challenge

Your skill has a slash command — that's one way to trigger it. But good skills can also be auto-detected: Claude recognizes when the skill is relevant based on what you're asking.

**Your challenge:**

1. Make sure your skill's `description` field is clear enough that Claude could match it to a natural language request. For example, if someone says "Can you prep me for my 2pm meeting?" Claude should recognize that your meeting-prep skill is relevant.

2. Test triggering it **both ways:**
   - Via the slash command directly
   - By describing the task naturally in chat (without mentioning the skill name)

3. If auto-detection doesn't work, iterate on your skill's description and name until it does.

**Success Criteria:**
- Skill triggers correctly via slash command
- Skill auto-loads when you describe the task in natural language
- Both methods produce the same workflow

> **Hint system:** Use `/hint` if you're stuck. First hint is a nudge, second is more specific, third nearly gives it away.
