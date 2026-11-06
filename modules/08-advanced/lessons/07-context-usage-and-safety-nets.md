---
module: 8
lesson: 7
title: "Context, Usage & Safety Nets"
difficulty: advanced
prerequisites: "8.06"
---

# Lesson 8.07: Context, Usage & Safety Nets

## Learn

As your sessions get longer and your workflows get bigger, three questions start to matter: **How much can Claude keep in mind at once? What's using up my plan? And how do I undo something that went wrong?** This lesson gives you the tools for all three.

> Already comfortable with this topic? Skip ahead anytime with `skip` followed by the next lesson number.

### Part 1: Managing Context

Every session has a **context window** — the amount of information Claude can hold in mind at once (see the glossary). Everything goes in: your messages, Claude's replies, files it read, and tool results. In a long session, it fills up.

When the window gets close to full, Claude automatically **compacts** — it summarizes older parts of the conversation to make room. That usually works fine, but details can get lost along the way. These commands give you control:

| Command | What it does | When to use it |
|---------|--------------|----------------|
| `/context` | Shows what's taking up space in the context window | When Claude seems to be forgetting things, or a session feels slow |
| `/compact` | Summarizes the conversation now, on your terms | At a natural break. Add what to keep: `/compact keep the decisions and open questions` |
| `/clear` | Starts fresh in the same session | When you're switching to an unrelated task |
| `/btw` | Asks a quick side question without adding it to the main thread | "Wait, what does this term mean?" mid-task |

**Rule of thumb:** one session per task. When the task changes, start a new session or `/clear`. A focused session beats a long, crowded one.

### Part 2: Understanding Your Usage

Your Claude plan has usage limits. Some habits use far more than others — big files, long sessions, many parallel agents, heavy connectors.

- **`/usage`** breaks down what's driving your usage — by skill, subagent, plugin, and connector — and suggests fixes when something is using a lot.
- **Effort level** (`/effort`) controls how hard Claude thinks before answering: `low`, `medium`, `high`, `xhigh`, or `max`. Higher effort is slower and uses more, but helps with hard problems. For everyday tasks, the default is fine.
- **Model choice** works the same way. Bigger models are stronger but use more. **Fast mode** (`/fast`) gives you faster answers at a higher cost.

You don't need to watch usage constantly. Check `/usage` when you hit a limit or when a scheduled workflow seems expensive.

### Part 3: Safety Nets

**Rewind.** Press **Esc twice** (or type `/rewind`) to go back to an earlier point in the session. You can restore the **files**, the **conversation**, or **both**. It's the fastest way to undo an edit that went wrong, or to try a different approach from a clean starting point.

A few limits to know:
- Rewind tracks edits Claude makes with its file tools. Changes made by running shell commands (like deleting a file from the terminal) aren't tracked.
- It isn't a backup system. For work that matters, keep a real history — that's what GitHub is for (Lesson 8.02).

**Hooks (optional, for power users).** A hook is a small rule that runs automatically when something happens in Claude Code — for example, "send me a desktop notification whenever Claude needs my input" or "check formatting after every file edit." Hooks are set up in your settings (type `/hooks` to see yours). You don't need them to be productive. They're useful when you want something to happen *every* time, without relying on Claude to remember.

## Practice

Try each tool once so you know it's there when you need it.

**Step 1: Check your context.** In this session (or any long session), run `/context`. What's taking up the most space?

**Step 2: Ask a side question.** Use `/btw` to ask something unrelated to the current task. Notice it doesn't clutter the main conversation.

**Step 3: Compact on purpose.** Run `/compact` with an instruction about what to keep. Then ask Claude to summarize what it still knows about your progress.

**Step 4: Practice a rewind.** Ask Claude to make a throwaway change to a file in `workspace/` (like adding a silly line to a test file). Then press Esc twice, or type `/rewind`, and restore the file to before the change.

**Step 5: Look at your usage.** Run `/usage` and note one thing that's using more than you expected.

**Success criteria:** Ran `/context` and `/compact`, asked a `/btw` question, rewound a real file change, and checked `/usage`.

## Challenge

Pick one:

**Option A: Set up a notification hook.** Ask Claude to set up a hook that sends you a desktop notification when Claude needs your input or finishes a long task. Have Claude explain what it changed and where the setting lives. Then test it.

**Option B: Write your session hygiene rules.** Based on what you learned, write 3-5 personal rules for keeping sessions healthy (when to start fresh, when to compact, when to check usage). Add them to a CLAUDE.md you use for real work so Claude can remind you.

> **Before you're done — Question It:** What did Claude assume? What's missing? What could break?

**Success criteria:** Either a working hook that you tested, or 3-5 session hygiene rules saved in a real CLAUDE.md.

---

Next up — two short lessons on a different kind of power-user move: putting Claude to work toward a **goal** it keeps pursuing on its own until the job is done.
