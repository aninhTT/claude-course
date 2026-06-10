---
module: 7
lesson: 7
title: "Working Toward a Goal"
difficulty: advanced
prerequisites: "7.06"
---

# Lesson 7.07: Working Toward a Goal

## Learn

So far, the way you've worked with Claude is turn by turn: you ask for something, Claude does it, and then it hands control back to you. For most work, that's exactly right.

But some jobs are big, repetitive, and have a clear finish line — and for those, stopping after every turn to say "keep going" gets tedious. That's what the **`/goal`** command is for.

> 📋 **Requires Claude Code v2.1.139 or later.** If you're on an older version, you can still learn the concept here — and you'll want it the next time you face a big, repetitive task.

### What `/goal` Is

With `/goal`, you set a **completion condition** — a description of what "done" looks like — and Claude keeps working, turn after turn, *without you re-prompting each step*, until that condition is met. Then the goal clears itself automatically.

You set it like this:

```
/goal every vendor in workspace/vendors.md is scored against all five criteria,
with every cell filled in and a one-line rationale for each score
```

That's it. Claude starts working toward that finish line on its own.

### How It Works (in Plain English)

Here's the clever part. After each turn, a quick **"checker"** — a separate, fast model — looks at what Claude has produced and asks one question: *"Is the condition met yet?"*

- If **no**, Claude keeps going — and the checker hands back a short reason for what's still missing, so the next turn knows what to work on.
- If **yes**, Claude stops and the goal is done.

While a goal is running, you'll see a `◎ /goal active` indicator showing how long it's been going. And because the checker leaves a short reason after every turn, you get a visible, turn-by-turn record of *how* Claude got to the finish line.

> 💡 That record is more than a status update — it's an **audit trail**. For the kinds of work we're about to talk about, being able to see "here's what was checked, here's what was found, here's why it passed" is half the value.

### Why This Is Powerful

Three things make `/goal` different from just asking Claude to "do this big thing":

1. **One instruction, many turns.** A job that would take a dozen back-and-forths becomes a single sentence. You set the finish line and step away.
2. **It works toward a *verifiable* finish line** — not "until Claude thinks it's done." Claude is an eager helper; left alone, it often stops early and declares victory. The checker keeps it honest against the condition *you* defined.
3. **The checker is a second set of eyes.** The model doing the work isn't the one deciding whether it's finished. That separation catches "good enough" work that a single pass would wave through.

### The One Rule That Makes or Breaks It

Here's the thing you have to internalize before goals are useful: **the goal has to be specified.**

The checker is fast and lightweight, and — this matters — it **can't run commands or open files**. It only sees what Claude has actually *surfaced in the conversation*. So your completion condition has to be something Claude's own output can **demonstrate**.

- ✅ "A table of all 40 vendors, every cell filled, each score with a rationale" — Claude produces the table, the checker can see it's complete.
- ❌ "The vendor research is thorough and high-quality" — the checker has no way to judge "thorough" or "high-quality."

We'll spend the whole next lesson on *how* to write a good condition. For now, just hold onto this: **a goal is only as good as the finish line you can show.**

### What You'd Actually Use This For

This is the heart of the lesson. `/goal` shines on work that is **large, repetitive, and has a clear, checkable finish line** — and a lot of that work is *not* technical. Here are real patterns, each with the kind of "finish line" you'd give it:

**🔍 Audit workflows / audit trails**
*Example: an access review or expense-compliance audit.*
Finish line: *every item in the list has been reviewed and tagged pass or flag, each with a reason, and all flagged items are collected in a summary table.* The per-turn reasons become your audit trail — you can show exactly what was checked and why each call was made.

**📊 Verified market-landscape research**
*Example: mapping every competitor in a segment.*
Finish line: *a comparison table covering all known players, every cell either filled or marked "not found," and every factual claim backed by a cited source in the output.* The "cited source" requirement is what makes it *verified* rather than just plausible.

**🏷️ Vendor evaluations**
Finish line: *each vendor scored against the same fixed set of criteria, all cells filled, ending with a ranked recommendation.*

**📋 Due diligence checklists**
Finish line: *every item on the checklist answered with supporting evidence, and any gaps explicitly flagged.*

**👥 Sourcing & screening a large candidate pool**
Finish line: *every candidate in the list scored against the rubric, ranked, each with a one-line rationale.*

**📚 Literature reviews**
Finish line: *every source summarized with the same fields (method, finding, limitation), themes synthesized across them, and every claim attributed to a source.*

**The common thread:** the job is big and repetitive, the finish line is something you can *see* in the output, and you benefit from the trail of reasoning along the way. That last part is why audits, due diligence, and verified research are such a natural fit.

### What `/goal` Is NOT Good For

Just as important as knowing where it shines — knowing where it doesn't. Don't reach for a goal when:

- **The finish line is subjective.** "Make this report great," "research the market thoroughly." The checker can't judge "great" or "thorough." If you can't describe done in a way you could *see*, it's not a goal.
- **Completion can't be shown in the output.** "The CRM is fully updated" — if the proof lives in a system the checker can't see, it can't confirm it. The result has to land in the conversation.
- **It needs human judgment or real-world events at each step.** Waiting on a legal sign-off, a vendor's reply, or a payment to clear. A goal can't wait for the world; it just keeps taking turns.
- **It's a quick one-off.** If it's a single, simple task, just ask. A goal is overhead you don't need.
- **You want to review each turn before continuing.** Some work *should* have you in the loop every step. That's fine — that's just normal turn-by-turn work.

> ⚠️ **One caution even for good goals:** a vague or unbounded condition can run a long time (and spend tokens) chasing a finish line it can never confirm. Always give a goal a clear finish line *and* a bound — more on that next lesson. And remember **"Always Verify Output"**: a goal that reports "done" was confirmed by a fast checker reading the transcript, not by ground truth. You still give the result a real look.

---

## Practice

Before you write a goal (that's the next lesson), let's make sure you can spot where one belongs. This is a thinking exercise — no goal to write or run yet.

**Step 1: List 2–3 tasks from your own work that fit the goal "sweet spot."**

Think about what you do that is large, repetitive, and has a clear, checkable finish line. Audits, reviews, research matrices, screening, anything where you process a *list of things* the same way. For each one, write a single sentence describing what "done" would look like.

**Step 2: Name one task that does NOT fit — and why.**

Find something from your work that *sounds* like a goal but isn't — maybe the finish line is subjective, maybe completion lives somewhere the checker couldn't see, maybe it needs a human decision partway through. One sentence on why it doesn't fit.

**Step 3: Map your fitting tasks to a pattern.**

For each task in Step 1, jot which use-case pattern it resembles (audit, verified research, vendor eval, due diligence, candidate screening, literature review — or a cousin of one).

Save your notes to `workspace/goal-fit.md`.

**Success criteria:**
- 2–3 tasks identified that genuinely fit the goal sweet spot, each with a one-line "done" description
- 1 task identified that does NOT fit, with a clear reason why
- Each fitting task mapped to a use-case pattern

---

## Challenge

Sharpen your judgment by sorting a mixed bag.

**Step 1:** Write down (or have Claude generate) a list of 6–8 candidate tasks — a deliberate mix of good fits and poor fits. Pull from your real work if you can.

**Step 2:** Sort each into **"good fit for a goal"** or **"poor fit"** and justify the call in one sentence. The interesting ones are the near-misses: a task that's *almost* a goal except for one thing (subjective finish line, completion you can't see, a human decision in the middle).

**Step 3:** For the poor fits, note what you'd do *instead* — normal turn-by-turn work, a one-off ask, or a task that needs to be reshaped before it could ever be a goal.

> **Before you're done — Question It:** What did Claude assume? What's missing? What could break?

**Success criteria:**
- 6–8 tasks sorted into good fit / poor fit
- Each call justified in a sentence
- For poor fits, a note on what to do instead

> **Hint system:** Use `/hint` if you're stuck. First hint is a nudge, second is more specific, third nearly gives it away.

Next up — the skill that makes all of this work: **writing a goal that actually holds up.**
