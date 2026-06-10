---
module: 7
lesson: 8
title: "Writing a Good Goal"
difficulty: advanced
prerequisites: "7.07"
---

# Lesson 7.08: Writing a Good Goal

## Learn

In the last lesson you learned what `/goal` is and where it shines. Now for the skill that actually makes it work: **writing a completion condition that holds up.**

This is where most goals succeed or fail. A great goal runs unattended to a clean finish. A sloppy one either stops too early, never stops, or finishes "successfully" while missing the point. The difference is entirely in how you write the condition.

> In this lesson you'll *write and critique* a goal — not run one. The skill we're building is knowing what a good goal looks like.

### The Anatomy of a Goal That Holds Up

A strong completion condition has four parts. Not every goal needs all four, but the best ones usually have them:

**1. One measurable end state.**
A single, concrete finish line you could point at: a filled-in table, an empty queue, every item tagged. Avoid bundling three different "dones" into one goal — pick the one that means the work is complete.

> ✅ "Every row in `workspace/candidates.md` has a score and a one-line rationale"
> ❌ "The candidates are reviewed and the good ones are shortlisted and the hiring manager is updated" *(three finish lines — split them)*

**2. A stated check — how Claude should prove it.**
Tell the goal how "done" should show up in the output. This is what the checker reads.

> "...and the result is a single markdown table where no cell is blank"

**3. Constraints that must not change.**
Guardrails for things that should stay put on the way to the finish line.

> "...don't invent data — if a source doesn't state it, mark the cell 'not found'"

**4. A bound.**
A safety limit so a goal can't run forever. Add a turn or time clause right in the condition.

> "...or stop after 20 turns and report what's still incomplete"

### The Test That Catches Most Bad Goals

Before you trust any condition, run it through one question:

> **Could a checker that can't run commands or open files confirm this is done — using only what Claude wrote in the conversation?**

Remember from last lesson: the checker is fast, lightweight, and blind to anything outside the transcript. If your finish line lives in a file the checker can't open, a system it can't query, or a quality judgment it can't make, it will never confirm — and your goal runs in circles.

So: make the *proof* land in the output. "Tests pass" works only if Claude pastes the test results. "The table is complete" works because the table is right there to read.

### The Three Ways Goals Go Wrong

Watch for these — they're the usual suspects:

- **Vague.** "Research the competitive landscape thoroughly." No measurable finish, no way to check. *Fix:* name the exact table and what fills it.
- **Unobservable.** "The vendor database is fully updated." The proof is in a system the checker can't see. *Fix:* require the result to be surfaced in the conversation.
- **Unbounded.** A perfectly good finish line with no turn or time limit — fine if it's reachable, costly if it isn't. *Fix:* always add "or stop after N turns."

### How You'd Set It (for reference)

When you *do* run a goal, it's just three commands:

```
/goal <your completion condition>      # set it; Claude starts working
/goal                                  # check status: turns, tokens, last reason
/goal clear                            # stop it before it finishes
```

The condition can be quite long — up to about 4,000 characters — so don't be afraid to spell out the end state, the check, the constraints, and the bound in full. Precision here is what lets you walk away.

---

## Practice

Write one real, well-formed goal. Not run it — *write* it, then make it good.

**Step 1: Pick a use case.**

Choose one of the patterns from Lesson 7.07 — audit, verified market research, vendor eval, due diligence, candidate screening, literature review — or one of the fitting tasks you listed in `workspace/goal-fit.md`.

**Step 2: Sketch the artifact first.**

Before the condition, sketch what Claude would actually fill in. For a vendor eval, that's the scorecard columns. For research, the table headers. For an audit, the per-item fields. A goal is much easier to write once you know the shape of the thing it produces.

**Step 3: Write the full completion condition.**

Include all four parts:
- the **measurable end state**,
- the **stated check** (how "done" shows up in the output),
- the **constraints** that must not change,
- a **bound** (e.g., "or stop after 20 turns").

**Step 4: Run it through the test.**

Ask yourself the key question: *could a checker that can't open files or run commands confirm this is done from the output alone?* If not, rewrite it so the proof lands in the conversation.

**Step 5: Critique and refine.**

Read it once more for the three failure modes — vague, unobservable, unbounded. Tighten anything soft.

Save both the artifact sketch and the final condition to `workspace/my-goal.md`.

> **Do not run the goal.** The point of this exercise is to practice what a good goal looks like — a condition you'd trust to run unattended.

**Success criteria:**
- A complete, well-formed sample goal with all four parts
- A sketch of the artifact it would produce
- Passes the "demonstrable in output" test
- A short self-critique noting how you tightened it

---

## Challenge

Take it one level up — pick **one**:

**Option A — Fix a broken goal.** Write a deliberately vague goal (e.g., "make our vendor research really solid"), then rewrite it into a sharp, bounded, observable one. Keep both versions side by side and annotate exactly what you changed and why.

**Option B — Build a reusable template.** Turn your Practice goal into something a teammate could adapt for their own work. Include:
- the completion condition (with placeholders for the specifics),
- the artifact template it fills,
- a short **"how to verify the result afterward"** note (because a goal reporting "done" still needs a human look),
- a **"when NOT to use this"** line.

Save your work to `workspace/goal-workflow/`.

> **Before you're done — Question It:** What did Claude assume? What's missing? What could break?

**Success criteria:**
- (A) A clear before/after with annotated changes, **or** (B) a reusable template with condition, artifact, verification note, and a "when not to use" line
- The final goal is measurable, observable, and bounded

> **Hint system:** Use `/hint` if you're stuck. First hint is a nudge, second is more specific, third nearly gives it away.

---

## Congratulations — You've Completed the Course!

You started with the basics: understanding what Claude Code is, connecting your tools, having your first conversation. You learned Cowork for background tasks, built skills, discovered the plugin ecosystem, and designed use cases tailored to your actual work. You went deeper with building real use cases, getting feedback, and polishing your work. And in this final module, you've prototyped ideas, deployed to GitHub, mastered the terminal, orchestrated multiple agents, set up project memory, learned to codify your judgment into automated evaluation systems, and discovered how to put Claude to work toward a goal.

The entire Claude Code & Cowork course is now complete.

Please take a few minutes to fill out the completion survey — your feedback directly shapes future iterations of this course and helps the L&D team understand what worked, what didn't, and what to build next:

**https://forms.gle/74iMkRWDVPw5ffQP9**

Thank you for investing the time. Now go build something great.
