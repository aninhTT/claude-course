---
module: 7
lesson: 4
title: "Multiple Sessions & Agent Workflows"
difficulty: advanced
prerequisites: "7.03"
---

# Lesson 7.04: Multiple Sessions & Agent Workflows

## Learn

This lesson brings together two related concepts: managing multiple sessions (something you first encountered in Module 2) and designing deliberate multi-agent workflows. We'll start with the fundamentals and then go deeper into advanced orchestration patterns.

### Session Management Basics

Both Cowork and Claude Code can run multiple sessions simultaneously. You're not limited to one task at a time. You can have several Cowork sessions running in parallel, or a mix of Cowork and Claude Code sessions, each doing different work.

**In the Claude app, you can:**
- **Start a new session** at any time — each session is independent and has its own context
- **Switch between sessions** using the sidebar — click on any active session to see its progress or output
- **Run sessions in parallel** — one session doesn't block another

Each session maintains its own conversation history and context. They don't automatically share information with each other — if you need output from one session in another, you'll need to copy it over or use a shared folder.

### When Multiple Sessions Help

- **Tasks are independent** — If two tasks don't depend on each other, run them in parallel
- **You're doing different types of work** — One Cowork session researches while you build in Claude Code
- **Time-sensitive projects** — Parallelize the prep work to get everything ready faster
- **Comparing approaches** — Run two sessions with different instructions and see which output is better

### When Multiple Sessions Add Complexity

- **Tasks depend on each other** — If Task B needs Task A's output, run them sequentially
- **Tasks touch the same resources** — Two sessions editing the same document will create conflicts
- **The overhead isn't worth it** — For a 5-minute task, managing multiple sessions exceeds the time saved

### Practical Multi-Session Patterns

**Pattern 1: Review + Implement**
- **Session A (Cowork):** Research and compile information
- **Session B (Claude Code):** Start building with what you already know
- When Session A finishes, feed its output into Session B

**Pattern 2: Spec + Build + Test**
- **Session 1 (Cowork):** Gather requirements from Slack, emails, meeting notes
- **Session 2 (Claude Code):** Build based on the spec
- **Session 3 (Cowork):** Review the build against the original requirements

**Pattern 3: Orchestrator**
- **Main session (Claude Code):** Your command center — plan work, kick off tasks, review output
- **Cowork Sessions A, B, C:** Handle parallel research or execution tasks

### Advanced: Multi-Agent Orchestration

Beyond basic multi-session management, you can deliberately design workflows where multiple Claude Code agents work on related parts of a problem, then bring their results together.

**Why multiple agents?**

A single Claude Code session is powerful, but it has limits. It works in one context, follows one thread of thought, and processes one thing at a time. Multiple agents let you:

- **Specialize.** One agent focuses on research, another on drafting, another on analysis. Each can be given context and instructions tailored to its specific role.
- **Parallelize.** Instead of doing three 10-minute tasks in sequence (30 minutes), run them simultaneously (10 minutes).
- **Separate concerns.** Keep messy, exploratory work in one session while maintaining a clean, focused session for the final output.

### Orchestration Patterns

**Coordinator + Workers**
One agent acts as the coordinator — it breaks the task down, delegates subtasks to other agents, and assembles the final result.

*Example:* A coordinator agent receives "Prepare a weekly team update." It delegates: Agent A scans Slack for team highlights, Agent B reviews completed Jira tickets, Agent C checks the calendar for upcoming deadlines. The coordinator merges their outputs into a single update.

**Independent Agents, Merged Results**
Multiple agents work independently on different aspects of the same problem, and you (or a final agent) merge the results manually.

*Example:* You're preparing for a meeting. Agent A researches the attendees' recent activity. Agent B compiles relevant documents and data. You take both outputs and prepare your talking points.

**Pipeline (Sequential Handoff)**
Agents work in sequence, each building on the previous agent's output.

*Example:* Agent A drafts a project proposal from rough notes. Agent B reviews the draft for completeness and adds missing sections. Agent C formats it and checks for consistency.

### Practical Considerations

- **Context isolation:** Each agent has its own context. This is usually a feature, not a bug — it means each agent can focus without distraction. But you need to be explicit about what each agent needs to know.
- **Conflict avoidance:** If two agents try to modify the same file simultaneously, you'll get conflicts. Design your workflows so agents work on different files.
- **Result merging:** The outputs from multiple agents need to come together somehow. Plan for this step — it's where multi-agent workflows either shine or fall apart.

## Practice

Design and run a multi-agent workflow.

**Step 1: Choose a task** that has at least two naturally separable subtasks. Some ideas:
- Research a topic across multiple sources and compile findings
- Draft a document where one agent handles content and another handles data/evidence
- Prepare for a meeting where one agent reviews communications and another gathers background
- Audit a process where different agents check different aspects

**Step 2: Design the workflow.** Decide:
- How many agents do you need?
- What does each agent do?
- What context does each agent need?
- How will you merge the results?

**Step 3: Run it.** Launch your agents (using separate Claude Code sessions, Cowork tasks, or a combination). Give each one clear, specific instructions about its role and what output you expect.

**Step 4: Merge the outputs.** Bring the results together. Was the merge step smooth? Did the outputs complement each other or overlap?

**Success criteria:** Successfully ran 2+ agents on related tasks and merged their outputs into a combined result.

## Challenge

Build a reusable multi-agent workflow — one you could run again next week, next month, whenever you need it.

**Step 1:** Based on your Practice experience, refine the workflow. What worked? What would you change?

**Step 2:** Document the pattern. Create a file in `workspace/` (call it something like `multi-agent-workflow.md`) that describes:
- **Purpose:** What problem does this workflow solve?
- **Agents:** How many, and what role does each play?
- **Context:** What does each agent need to know to do its job?
- **Coordination:** How do the agents' outputs come together?
- **How to run it:** Step-by-step instructions for kicking off the workflow
- **Expected output:** What does the final merged result look like?

**Step 3:** Test the documentation by running the workflow one more time using only the documented instructions. Does the documentation capture everything someone would need?

> **Before you're done — Question It:** What did Claude assume? What's missing? What could break?

**Success criteria:** Documented a reusable multi-agent pattern with clear roles, coordination steps, and instructions. Saved in `workspace/`.
