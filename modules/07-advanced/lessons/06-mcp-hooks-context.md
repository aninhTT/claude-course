---
module: 7
lesson: 6
title: "The Loop: Codifying Judgment"
difficulty: advanced
prerequisites: "7.05"
---

# Lesson 7.06: The Loop — Codifying Judgment

## Learn

In Module 5, you learned about Cowork's Scheduled Tasks for recurring automation. Now we're going to go deeper with Claude Code's **`/loop` command** — and more importantly, the powerful concept behind it: **codifying your judgment so Claude can evaluate, assess, and continuously improve something on your behalf.**

### What Is `/loop`?

The `/loop` command in Claude Code runs a prompt on a recurring interval, right in your terminal:

```
/loop 5m check if the deploy finished
/loop 1h scan the inbox for urgent customer issues
/loop 30m review the latest draft against our brand guidelines
```

How it works:
- **You set the interval** — every 5 minutes, every hour, once a day
- **You write the prompt** — the instructions Claude follows each time
- **Claude runs it automatically** — repeating on schedule until you stop it or close the session

Key characteristics:
- **Session-scoped** — Lives in your terminal session; when you close it, the loop stops
- **Auto-expires** — Loops automatically stop after 3 days for safety
- **Full Code access** — Can read/write files, run commands, check Git, use MCP servers

> This is different from Cowork's Scheduled Tasks (which persist across restarts and use the visual sidebar). `/loop` is best when you want **focused, temporary automation** with full developer tooling — or when you want to run an evaluation cycle.

### The Real Power: Codifying Judgment

Here's where it gets interesting. The most powerful use of `/loop` isn't just "check this thing every 5 minutes." It's **teaching Claude your standards so it can evaluate something the way you would.**

Think about what you do at work that involves judgment:
- A recruiter evaluates candidates against a role's requirements
- A QA engineer checks a feature against acceptance criteria
- A lawyer flags risks in a contract against a compliance checklist
- A sales rep evaluates leads against targeting criteria
- A financial analyst checks a proposal against budget constraints
- A content creator reviews drafts against brand and style guidelines

In every case, the person has a **rubric** — a set of criteria they apply, often in their head, to assess whether something meets the bar. The rubric might be formal (a written checklist) or informal (gut feel from years of experience). Either way, it's judgment.

**`/loop` lets you externalize that rubric and run it repeatedly.**

### How It Works in Practice

Here's the pattern:

1. **Write the rubric** — Define what "good" looks like. Be specific: what passes, what fails, what needs improvement, and what the criteria are.
2. **Point it at the thing to evaluate** — A document, a codebase, a dataset, a process output.
3. **Run it in a loop** — Claude evaluates, identifies gaps, suggests improvements (or makes them), and re-evaluates.
4. **Each pass gets closer to the bar** — Because the rubric is explicit, Claude knows exactly what to aim for.

**Example — Content Quality Loop:**

```
/loop 10m Review the blog post draft at workspace/blog-draft.md against
these criteria: (1) Matches Thumbtack brand voice - professional but
approachable, (2) Has a clear hook in the first paragraph, (3) Includes
at least one data point or specific example per section, (4) Ends with
a clear CTA, (5) Under 800 words. Score each criterion pass/fail, fix
any failures, and save the updated draft.
```

Each time the loop runs, Claude re-reads the draft, scores it against the rubric, fixes what's lacking, and saves the result. After a few passes, the draft meets every criterion.

### Real-World Examples

**Recruiter — Hiring Process Evaluation:**
Write a rubric for what a good job posting looks like (clear role description, inclusive language, realistic requirements, compelling company pitch). Point `/loop` at a folder of draft postings. Claude evaluates each one, flags issues, and suggests rewrites.

**QA Engineer — Acceptance Criteria Check:**
Define your acceptance criteria as a rubric (feature works on mobile, handles edge cases, error messages are user-friendly, accessibility passes). Run a loop that checks the latest build against each criterion and generates a test report.

**Sales Rep — Outreach Quality:**
Write targeting criteria and outreach guidelines (right persona, personalized first line, clear value prop, appropriate ask, correct tone). Run a loop against draft outreach messages to score and improve them before they go out.

**Financial Analyst — Constraint Validation:**
Define your budget constraints, compliance requirements, and risk thresholds. Run a loop that evaluates a proposal or model against those constraints and flags anything out of bounds.

**The common thread:** You already have judgment about what good looks like. `/loop` lets you write it down once and apply it repeatedly, consistently, at scale.

### Starting Simple

You don't need a 50-point rubric to start. The easiest way in:

1. **Pick something you already evaluate repeatedly.** What do you review, check, or QA regularly at work?
2. **Write down 3-5 criteria.** What do you actually look for? Be specific — not "is it good?" but "does it have X, Y, and Z?"
3. **Point Claude at it.** Use `/loop` to run the evaluation, or even just do it once manually to test the rubric.
4. **Refine the rubric.** After seeing Claude's evaluation, you'll notice criteria you forgot or ones that need to be more specific. Update and run again.

> 💡 **Pro tip:** Start with a manual run first. Before setting up the loop, just give Claude your rubric and something to evaluate. See if the output matches your judgment. If it doesn't, refine the rubric until it does — then automate.

---

## Practice

Build your first evaluation loop. This is a three-part exercise.

**Step 1: Choose your evaluation target.**

Pick something from your actual work that you evaluate or review regularly. Some ideas:
- Written content you produce (emails, reports, posts)
- Work product you review from others
- A process output you QA
- Documents or proposals you check against criteria

**Step 2: Write your rubric.**

Create a file at `workspace/my-rubric.md` that defines what "good" looks like. For each criterion, specify:
- **What it is** (e.g., "Clear subject line")
- **What passing looks like** (e.g., "Under 10 words, conveys the key ask")
- **What failing looks like** (e.g., "Vague, generic, or missing entirely")

Aim for 3-5 criteria to start. Keep them concrete and assessable.

**Step 3: Run the evaluation.**

Give Claude something to evaluate against your rubric. You can do this as a one-time prompt first:

> "Here's my rubric [paste or reference the file]. Here's the thing to evaluate [paste or reference the document]. Score each criterion pass/fail. For any failures, explain what's wrong and suggest a specific fix."

Review Claude's assessment. Does it match your judgment? If not, refine the rubric and try again.

**Step 4 (optional): Set up the loop.**

If you're working in Claude Code's terminal, set up the actual loop:

```
/loop [interval] Evaluate [target] against the rubric at workspace/my-rubric.md.
Score each criterion, fix failures, and save the improved version.
```

**Success criteria:**
- Created a rubric with 3-5 specific, assessable criteria
- Ran at least one evaluation using your rubric
- Reviewed Claude's assessment and compared it to your own judgment
- Refined the rubric based on what you learned

---

## Challenge

Create a **judgment codification system** — a rubric that's robust enough to run reliably without you supervising every pass.

**Step 1:** Take your rubric from Practice and level it up:
- Add edge cases (what about partial passes?)
- Add a scoring scale (not just pass/fail — maybe 1-5)
- Add priorities (which criteria matter most?)
- Add instructions for what to do when something fails (fix it? flag it? escalate?)

**Step 2:** Test it on 3 different inputs. Does the rubric hold up across different examples, or does it only work for one case?

**Step 3:** Write a `/loop` prompt that runs the full evaluation autonomously. Include:
- Where to find the thing to evaluate
- The rubric to apply
- What to do with the results (save a report, fix the issues, both)
- How to handle edge cases

**Step 4:** Save everything at `workspace/evaluation-system/`:
```
workspace/evaluation-system/
  rubric.md          # Your criteria
  loop-prompt.md     # The /loop command and instructions
  sample-report.md   # An example evaluation output
```

> **Before you're done — Question It:** What did Claude assume? What's missing? What could break?

**Success criteria:**
- Rubric handles edge cases and uses a scoring scale
- Tested on 3+ different inputs with consistent results
- Loop prompt is self-contained and could run without supervision
- System is documented and saved

> **Hint system:** Use `/hint` if you're stuck. First hint is a nudge, second is more specific, third nearly gives it away.

---

## Congratulations — You've Completed the Course!

You started with the basics: understanding what Claude Code is, connecting your tools, having your first conversation. You learned Cowork for background tasks, built skills, discovered the plugin ecosystem, and designed use cases tailored to your actual work. You went deeper with building real use cases, getting feedback, and polishing your work. And in this final module, you've prototyped ideas, deployed to GitHub, mastered the terminal, orchestrated multiple agents, set up project memory, and learned to codify your judgment into automated evaluation systems.

The entire Claude Code & Cowork course is now complete.

Please take a few minutes to fill out the completion survey — your feedback directly shapes future iterations of this course and helps the L&D team understand what worked, what didn't, and what to build next:

**https://forms.gle/74iMkRWDVPw5ffQP9**

Thank you for investing the time. Now go build something great.
