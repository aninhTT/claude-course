---
module: 7
lesson: 5
title: "Project Memory & Complex Workflows"
difficulty: advanced
prerequisites: "7.04"
---

# Lesson 7.05: Project Memory & Complex Workflows

## Learn

This lesson covers two advanced topics that go hand in hand: making Claude smarter over time through **project memory**, and building **complex multi-step workflows** that tackle large tasks across many tools and stages.

### Part 1: Project Memory

Here's the problem: every time you start a new Claude Code session, Claude starts fresh. It doesn't remember what you talked about yesterday, what decisions you made last week, or what it learned about your project over the past month. Your CLAUDE.md gives it instructions, and your skills give it workflows — but neither gives it **accumulated knowledge**. That's what project memory solves.

#### CLAUDE.md vs. Memory: What's the Difference?

- **CLAUDE.md** = **Instructions**. How Claude should behave. Its role, rules, and standards. Relatively stable.
- **Memory files** = **Accumulated knowledge**. What Claude has learned about your project through use. These grow and change over time.

Think of it this way: CLAUDE.md is the job description. Memory is the experience the employee gains on the job.

#### The LEARNINGS.md Pattern

The most straightforward memory pattern is a LEARNINGS.md file — a running log of things Claude has discovered, decisions that were made, and corrections that were applied:

```markdown
# Project Learnings

## Data Model
- The `users` table was deprecated in Q3 2025. Use `user_profiles` instead.
- Activation is defined as completing a first booking within 7 days of signup.
- The `revenue` column in BigQuery is in cents, not dollars.

## Team Preferences
- Sarah prefers bullet-point summaries, not narrative paragraphs.
- Status updates go to #growth-updates, not #general.

## Past Decisions
- 2025-11-15: Decided to exclude test accounts from all metrics.
- 2025-12-01: Switched from weekly to biweekly reporting cadence.

## Things That Didn't Work
- Tried summarizing all Slack channels at once — too noisy. Focus on 2-3 key channels.
- Auto-posting to Slack without review caused issues. Always draft first, then confirm.
```

Key features: organized by category, specific and actionable, dated when relevant, and includes negative knowledge (what didn't work).

#### Context Files: Background Claude Can Reference

Beyond LEARNINGS.md, create context files that provide deeper background on specific topics:

- **`context/data-dictionary.md`** — Column definitions, table descriptions, metric formulas
- **`context/team-roster.md`** — Who's on the team, their roles, their preferences
- **`context/project-plan.md`** — Current goals, milestones, timeline
- **`context/style-guide.md`** — Templates, formatting standards, communication norms

Your CLAUDE.md can simply say: "Refer to files in `context/` for project background and data definitions."

#### How Memory Stays Fresh

- **Manual updates** — After each session, review what Claude learned and add key items to LEARNINGS.md
- **Ask Claude to update** — At the end of a session, say: "What did you learn today that I should add to LEARNINGS.md?"
- **Periodic review** — Every few weeks, scan your memory files. Remove outdated entries, consolidate related items.

#### The Full Memory Stack

```
my-project/
  CLAUDE.md           # Instructions and rules
  LEARNINGS.md        # Accumulated knowledge
  context/
    data-dictionary.md  # Reference material
    team-roster.md      # Team info
    style-guide.md      # Formatting standards
  logs/
    execution-log.md    # What's been run and when
  .claude/
    commands/           # Skills
```

### Part 2: Complex Workflows

You now have the building blocks: CLAUDE.md shapes behavior, skills define reusable workflows, and memory files give Claude persistent knowledge. The final piece is combining these into **complex, multi-step workflows**.

#### What Makes a Workflow Complex?

A simple skill is self-contained: gather data, format it, output it. A complex workflow has:

- **Multiple stages** — Each stage produces an intermediate result the next stage depends on
- **Multiple tools** — Different connectors at different points (Calendar, Slack, Gmail, BigQuery, etc.)
- **Decision points** — The workflow branches based on what it finds
- **Significant output** — The final result is a substantial artifact

#### Chaining Skills Together

The most practical way to build complex workflows is to chain existing skills. Each skill handles one stage, and the output of one becomes the input for the next.

Example — a "Weekly Review" workflow:

**Stage 1: Gather** — Pull meeting notes from Granola, scan key Slack channels, check Gmail for flagged emails

**Stage 2: Compile** — Extract action items, identify key decisions, note blockers

**Stage 3: Draft** — Write a structured status update with sections for Accomplishments, Decisions, Action Items, and Blockers

**Stage 4: Deliver** — Draft a Slack message with the summary, hold for review before posting

#### Claude Code vs. Cowork: Choosing Your Runtime

**Use Claude Code when:**
- You want to watch each step execute and intervene if needed
- The workflow involves creating or editing files
- You need to iterate on intermediate results

**Use Cowork when:**
- The workflow is well-tested and runs reliably without intervention
- You want it to run in the background
- You want to schedule it to run automatically

Many workflows start in Claude Code (where you iterate and refine) and graduate to Cowork (where they run autonomously once proven).

#### Handling Failures Gracefully

- **Fail forward** — If one stage fails, capture what you have and continue. A partial result is better than no result.
- **Checkpoint results** — After each major stage, save intermediate results. If the workflow fails at Stage 3, you don't have to redo Stages 1 and 2.
- **Set time limits** — "If gathering data takes more than 2 minutes, proceed with what you have."
- **Clear reporting** — When something goes wrong, the workflow should tell you exactly what failed and what it did about it.

#### Keeping Context Manageable

- **Summarize between stages** — Don't carry raw data forward if a summary will do.
- **Use intermediate files** — Write stage results to a file, then reference the file in the next stage.
- **Scope each step tightly** — "Get the top 5 most important items" is better than "Get everything."

## Practice

This practice has two parts — one for memory, one for workflows.

### Part A: Set Up Project Memory

**Step 1: Create LEARNINGS.md.** Write a `workspace/LEARNINGS.md` file with initial entries. Think about a real project and populate it with:
- At least 3 factual learnings (data definitions, system details, team preferences)
- At least 2 past decisions with dates
- At least 1 "thing that didn't work" entry

**Step 2: Create a context file.** Pick one type that would be most useful:
- A data dictionary, team roster, project plan, or style guide

Create it at `workspace/context/[your-choice].md` with real or realistic content.

**Step 3: Test the memory.** Ask Claude to read your LEARNINGS.md and context file, then ask it a question that requires that knowledge. Does Claude use the information?

### Part B: Build a Multi-Step Workflow

**Step 1: Design the workflow.** Write the full flow before building: what are the stages, what does each produce, what's the final output? Save the design at `workspace/workflow-design.md`.

**Step 2: Build it.** Create a SKILL.md for your workflow at `workspace/my-workflow.md`. It should chain at least 2 distinct stages and include error handling.

**Step 3: Test it.** Run the workflow with Claude. Does the output of Stage 1 feed cleanly into Stage 2? Is the final result useful?

**Success criteria:** Created a LEARNINGS.md and context file with substantive content. Built a multi-step workflow that chains at least 2 stages, with error handling and a useful final output.

## Challenge

Design a complete memory strategy and scheduling plan for a complex project.

**Step 1: Memory strategy.** Document it in `workspace/memory-strategy.md` with:
- File inventory — what files would you create?
- Update cadence — how often would each file be updated?
- CLAUDE.md integration — how would your CLAUDE.md reference these memory files?
- Boundary decisions — what belongs in memory vs. CLAUDE.md vs. external docs?

**Step 2: Workflow scheduling.** Plan when your workflow should run:
- Frequency — daily, weekly, on a specific day?
- Timing — morning, end of day, Friday afternoon?
- What it does with the output — Slack channel, email, file?
- What happens if it fails — retry, alert, save partial results?

For example, a Friday afternoon weekly review at 4:00 PM would use cron expression: `0 16 * * 5`

Save your scheduling plan in `workspace/workflow-schedule.md`.

> **Before you're done — Question It:** What did Claude assume? What's missing? What could break?

**Success criteria:** Documented a memory strategy with file inventory, update cadence, and boundary decisions. Designed a scheduling plan with timing, output destination, and failure handling.
