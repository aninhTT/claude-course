---
module: 5
lesson: 2
title: "Scheduling & Automating Skills"
difficulty: intermediate
prerequisites: "5.01"
---

# Lesson 5.02: Scheduling & Automating Skills

## Learn

So far, you've been running skills manually — typing a command or describing a task. That's useful, but the real time savings come when skills run on their own, on a schedule, without you having to remember to trigger them.

### Three Ways to Trigger Skills

**1. Manual — Slash Commands**
You type `/morning-briefing` and the skill runs. You're in control of when and how.

Best for: On-demand tasks, things that need human judgment on timing, one-off workflows.

**2. Auto-Detection**
Claude recognizes that what you're asking about matches a skill and loads it automatically. You say "Can you prep me for my next meeting?" and Claude finds and runs your meeting-prep skill.

Best for: Skills that match natural conversation patterns, tasks you might forget you have a skill for.

**3. Scheduled — Automatic Recurring Tasks**
The skill runs automatically at set times. Your morning briefing runs every weekday at 8am without you lifting a finger.

Best for: Recurring tasks with predictable timing, daily/weekly rituals, anything you'd otherwise put a calendar reminder for.

### Scheduled Tasks in Cowork

Cowork now has **built-in scheduled tasks** — and it's one of the most powerful features for knowledge workers.

**How to set one up:**

1. Open Cowork and click **"Scheduled"** in the sidebar (or type `/schedule` in any task)
2. Click **"+ New task"**
3. Give it a **name** and **description**
4. Write the **prompt** — the instructions Claude will follow each time it runs
5. Set the **frequency**: Manual (on-demand only), Hourly, Daily, Weekdays, or Weekly
6. Choose a **time** for when it should run

That's it. Once created, the task runs automatically on your chosen schedule.

**What makes Cowork scheduled tasks special:**

- **Persistent** — They survive app restarts. Set it up once and it keeps running.
- **Self-improving** — After the first run, Claude often refines its own instructions based on what it learned — which connectors it used, where it found data, what worked. Subsequent runs tend to get better automatically.
- **Catch-up on missed runs** — If your computer was asleep or the app was closed, Cowork checks for missed runs from the last 7 days and catches up when you reopen.
- **Full tool access** — Scheduled tasks have access to all your connected tools — Slack, Gmail, Calendar, Granola, everything.

**One important limitation:** Tasks only run while your computer is awake and the Claude Desktop app is open. If your laptop is closed, the task waits until you're back.

> 💡 **Going deeper:** Claude Code also has a powerful `/loop` command for more advanced recurring automation. We'll cover that in Module 7 — for now, Cowork's Scheduled Tasks are the easiest way to get started.

### What Makes a Good Automated Task

Not every skill should be automated. Good candidates for scheduling have these traits:

- **Predictable inputs.** The task doesn't need you to provide information at runtime — it knows where to look.
- **Consistent outputs.** The result is roughly the same format every time — a summary, a list, a draft.
- **Graceful failure.** If something goes wrong (a data source is unavailable, no new items to process), the task handles it quietly instead of crashing.
- **Clear value on a schedule.** There's a reason it runs at that specific time — not just "because it can."

### Choosing the Right Trigger Pattern

| Trigger | Use When | Example |
|---------|----------|---------|
| Slash command | You want explicit control | `/deep-research quarterly earnings` |
| Auto-detection | The task comes up in conversation | "Help me prepare for the design review" |
| Scheduled | Same task, same time, every time | Morning briefing at 8am weekdays |

Many skills benefit from **multiple trigger types**. Your morning briefing might run automatically at 8am via a scheduled task, but you can also trigger it manually with `/morning-briefing` if you start early.

### Handling Failures in Automated Tasks

When a scheduled task fails, you might not notice for days. Build in safeguards:

- **Default fallbacks.** If data source A is unavailable, try source B, or produce a partial result.
- **Explicit "nothing to report" handling.** If there's no new data, say so — don't silently produce nothing.
- **Notification on failure.** If the task truly can't run, it should tell you (e.g., send a Slack message) rather than failing silently.

---

## Practice

Take one of your existing skills and set it up as a scheduled task in Cowork.

**Step 1:** Pick the skill that makes the most sense to automate. Ask yourself: "Do I do this at the same time regularly?" If yes, it's a good candidate.

**Step 2:** Decide on the schedule. When should it run? How often? Match it to a real pattern from your work.

**Step 3:** Open Cowork → click **"Scheduled"** in the sidebar → click **"+ New task"**. Set the name, write the prompt (you can reference your skill's instructions), and choose the frequency.

**Step 4:** Verify by checking the Scheduled sidebar — confirm the task appears and the next run time looks correct.

**Step 5:** Review your task's instructions for unattended execution. Since it will run without you, make sure:
- It knows where to find its inputs (don't assume you'll be there to point it)
- It handles cases where data might be missing
- The output goes somewhere useful (Slack message, saved file, etc.)

Update the task prompt if needed.

**Success Criteria:**
- Created at least one scheduled task in Cowork
- The schedule matches a real pattern from your work (not arbitrary)
- Verified the next run time is correct in the Scheduled sidebar
- Task instructions handle unattended execution gracefully

---

## Challenge

Design a complete automated system using 3 or more scheduled tasks that together form a coherent workflow. You can set these all up in Cowork's Scheduled Tasks.

**Example system — "Stay on Top of Everything":**

| Task | Schedule | Purpose |
|------|----------|---------|
| Inbox Scan | Every weekday at 8:00 AM | Scan email and Slack, surface what needs attention |
| Meeting Prep | Daily at 8:30 AM | Pull context and talking points for today's meetings |
| Weekly Summary | Friday at 4:00 PM | Compile the week's work into a shareable summary |

**Your challenge:**

1. Design a system of 3+ scheduled tasks with clear purposes
2. Document the system: what each task does, when it runs, and how they relate to each other
3. Set up at least one of the schedules for real in Cowork
4. Save your system design at `workspace/automated-system.md`

Think about: What information flows between them? Are there dependencies (does one need to run before another)? What happens if one fails — do the others still work?

> **Before you're done — Question It:** What did Claude assume? What's missing? What could break?

**Success Criteria:**
- Designed a system of 3+ scheduled tasks with clear schedules
- Each task has a reason for its specific timing
- Documented the system with relationships and data flow
- Set up at least one schedule for real in Cowork

> **Hint system:** Use `/hint` if you're stuck. First hint is a nudge, second is more specific, third nearly gives it away.
