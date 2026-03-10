---
module: 2
lesson: 4
title: "Task Decomposition & Coordination"
difficulty: intermediate
prerequisites: "2.03"
---

# Lesson 2.04: Task Decomposition & Coordination

## Learn

So far, you've been giving Cowork single, self-contained tasks. That works great for many things — but some of the most valuable work involves **complex tasks** that need to be broken down before any agent (human or AI) can handle them well.

This lesson teaches you how to think about breaking work into pieces that Cowork can execute effectively.

### What Makes a "Good Size" for an Agent Task

Not every task is the right size for Cowork. A well-scoped agent task has these properties:

- **Specific scope** — Clear boundaries on what's included and what's not
- **Clear inputs** — Cowork knows exactly where to get the information it needs
- **Clear outputs** — The deliverable is well-defined (a document, a message, a list)
- **5-15 minutes of work** — Roughly the amount of work a capable person could do in 5-15 minutes. Too small and it's not worth the overhead. Too large and the quality drops.
- **Self-contained** — The task can be completed without waiting for other tasks to finish first (or, if it depends on something, that dependency is already complete)

### Good vs Bad Task Breakdowns

Let's look at a concrete example. Say you need to **prepare for a quarterly business review**.

**Bad: One giant task**
> "Prepare everything for my quarterly review next Tuesday."

This is way too broad. Cowork doesn't know what "everything" means, what format you need, what data to pull, or who the audience is. It will either produce something generic or get lost in the weeds.

**Bad: Tasks that are too small**
> "Find the Q1 revenue number from Slack."
> "Find the Q1 customer count from Slack."
> "Find the Q1 NPS score from email."

These are so granular that you're micromanaging. You'd spend more time writing and managing these tasks than doing the work yourself.

**Good: Well-scoped subtasks**
> 1. "Review my Slack channels and email from the last 2 weeks. Compile a list of key metrics, wins, and challenges that were discussed about our team's Q1 performance. Organize by theme."
> 2. "Check my Granola meeting notes from the last month. Pull out any strategic decisions, feedback from leadership, or commitments we made. List each with date and context."
> 3. "Using the outputs from tasks 1 and 2 (I'll paste them in), draft a 1-page executive summary for my quarterly review. Format: 3 wins, 3 challenges, 3 priorities for next quarter."

Each task is specific, has clear inputs and outputs, and is a reasonable amount of work.

### Anti-Patterns to Avoid

**Too vague:** "Look into the project and tell me what's going on." Cowork needs to know which project, what sources to check, and what kind of information you're looking for.

**Too broad:** "Analyze all of our team's communication from Q1." This is hours of work with no clear deliverable. Break it down by theme, time period, or source.

**Conflicting instructions:** "Be comprehensive but keep it short." "Check everything but only include what's important." These contradictions force Cowork to guess what you want.

**Missing context:** "Draft the update for Sarah." Cowork doesn't know who Sarah is, what update she's expecting, or what format she prefers — unless you tell it.

### The Power Move: Let Claude Break It Down for You

Here's a technique that flips everything we just covered on its head — in a good way.

Instead of you doing all the work of scoping a task perfectly, **tell Claude to ask you questions first.** Add this to any Cowork prompt:

> "Start by using the AskUserQuestion tool to gather enough context before you begin."

When you include this, something magical happens. Instead of Claude guessing at what you want, it pops up an interactive form — clickable buttons, multi-select options, the works. Claude interviews *you* to understand exactly what you need.

**Why this is powerful:**

- You don't need to think of every detail upfront
- Claude asks smart questions based on what it already knows about the task
- You click answers instead of typing paragraphs
- The result is much more targeted because Claude clarified the ambiguity before starting

**Here's what it looks like in practice:**

You write a brief prompt:
> "I need to prep a summary of our team's Q1 progress for the leadership meeting next Tuesday. Start by using AskUserQuestion to gather context."

Claude might ask you things like: Who's the audience? What format do you want? Which metrics matter most? What tone — data-heavy or story-driven? You click your answers in under a minute. Then Claude has exactly what it needs — without you writing a lengthy prompt.

**The universal Cowork prompt template:**

This works for roughly 80% of tasks:

> "I want to [TASK] to [SUCCESS CRITERIA]. Ask me questions using the AskUserQuestion tool first. I want to refine the approach with you before you execute."

That's it. Short prompt, big results — because Claude does the decomposition work for you.

> **Pro tip:** You can combine both approaches. Break a big project into subtasks manually, but for each individual subtask, let Claude ask clarifying questions before executing. Best of both worlds.

### Shared Context Between Tasks

When you break work into subtasks, the output of one task often becomes the input for another. Here are two ways to handle this:

1. **Sequential handoff:** Run Task A, take its output, and paste it into the instructions for Task B. This gives you a chance to review and edit between steps.

2. **Shared folder:** Have both tasks work from the same folder. Task A saves its output as a file, and Task B reads from that file. This works well when you trust the intermediate output.

For now, the sequential handoff is simpler and gives you more control. We'll cover more advanced coordination in the next lesson.

### Conflict Avoidance

One critical rule: **never have two agents editing the same thing at the same time.** If two Cowork sessions are both trying to update the same document or send messages to the same channel, you'll get conflicts, duplicates, or overwritten work.

Instead, give each task its own clear territory:
- Different files or documents
- Different sections of a larger project
- Different communication channels
- Read-only access for research tasks, write access for only one task at a time

## Practice

Take a complex task from your real work and break it down into Cowork-sized subtasks.

**Step 1: Pick a complex task.**

Choose something that feels too big for a single Cowork session. Examples:
- Prepare for a quarterly review or team presentation
- Onboard yourself to a new project by gathering all context
- Compile a competitive analysis or market research summary
- Create a project retrospective from meeting notes and Slack threads
- Prepare a briefing packet for a visiting executive or new team member

**Step 2: Break it into 3-4 subtasks.**

For each subtask, write out:
- **Objective:** What should this subtask produce?
- **Sources:** Where does Cowork get the information?
- **Output:** What's the deliverable and format?
- **Dependencies:** Does this task depend on another task's output?

Write these out clearly — you could give each one directly to Cowork as instructions.

**Step 3: Run at least one of the subtasks — with the "ask me" technique.**

Pick the subtask that has no dependencies (or the first one in the chain). When you give it to Cowork, add: "Start by using the AskUserQuestion tool to gather context before you begin."

Notice how Claude's questions help refine the task. Click through the answers and see how the output compares to what you would have gotten without the clarifying questions.

**Step 4: Evaluate your breakdown.**

- Were the subtasks the right size?
- Did the first subtask's output feel like it would feed well into the next one?
- Would you split or merge any of the subtasks differently?

**Success criteria:** Broke a complex task into 3 or more well-scoped subtasks, each with clear instructions (objective, sources, output, dependencies), and ran at least one through Cowork using the "ask me questions" technique.

## Challenge

Think bigger. Identify a **multi-person workflow** on your team — something that involves multiple people doing different parts of a larger process.

Examples:
- Sprint planning (PM writes specs, designers mock up, engineers estimate)
- Incident response (identify issue, investigate, communicate, resolve)
- Content publishing (research, draft, review, publish, distribute)
- Hiring process (source candidates, screen, interview, debrief)
- Customer escalation handling (triage, investigate, respond, follow up)

**Step 1: Map out the workflow.**

Write down the steps, who does what, and how information flows between steps.

**Step 2: Identify where Cowork could help.**

For each step, decide: Is this a Cowork task, a human task, or a hybrid?

- **Cowork tasks:** Research, compilation, drafting, summarization, data gathering
- **Human tasks:** Decisions, judgment calls, relationship-sensitive communication, creative strategy
- **Hybrid:** Cowork does the prep, human does the finishing

**Step 3: Design the handoffs.**

For each transition from Cowork to human (or vice versa), describe:
- What does Cowork hand off?
- What format is it in?
- What does the human need to do with it?

**Success criteria:** Designed a workflow with clear human/Cowork task assignments and well-defined handoffs between them. The design reflects realistic understanding of what Cowork is good at and what requires human judgment.
