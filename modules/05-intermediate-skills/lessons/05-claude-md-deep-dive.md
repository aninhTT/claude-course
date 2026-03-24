---
module: 5
lesson: 5
title: "CLAUDE.md Deep Dive"
difficulty: intermediate
prerequisites: "5.04"
---

# Lesson 5.05: CLAUDE.md Deep Dive

## Learn

Every time Claude opens a folder, the first thing it does is look for a CLAUDE.md file. This single file shapes how Claude behaves, what it knows about your project, and what rules it follows. You've seen it in action already — the CLAUDE.md in this course folder is what turns Claude into your tutor right now.

Understanding CLAUDE.md deeply is the foundation for everything else in this module, because skills build on top of it.

### What Goes in a CLAUDE.md

A great CLAUDE.md has four key sections:

**1. Role Definition**
Tell Claude who it is in this context. Be specific — "You are a senior data analyst working on the Thumbtack marketplace team" is far better than "You are helpful."

**2. Project Context**
What does Claude need to know about this project to be useful? Key files, architecture, team conventions, terminology. Think of it as the onboarding doc you'd give a new teammate.

**3. Behavioral Instructions**
Rules for how Claude should act. These are the guardrails: what to do, what not to do, how to handle specific situations. The more specific, the better.

**4. Tool & Resource References**
What tools are available? What files should Claude read or reference? Where does data live? This connects Claude to the actual resources in your environment.

### Patterns from Real Projects

Here are patterns that work well in practice:

- **Start with the most important context.** Claude reads top-to-bottom, and earlier content has stronger influence.
- **Use headers and structure.** Just like a human reader, Claude navigates structured documents better than walls of text.
- **Be specific about what NOT to do.** "Never modify files in the /config directory without asking" is more useful than "Be careful with config files."
- **Reference actual file paths.** "See `docs/api-spec.md` for the API contract" gives Claude something concrete to work with.
- **Include examples.** Show Claude what good output looks like for your context.

### How CLAUDE.md Interacts with Skills

When a skill runs, it inherits the CLAUDE.md context from the folder it's in. This means:

- Skills in a folder with a strong CLAUDE.md automatically get project context
- You don't need to repeat project details in every skill
- The CLAUDE.md sets the "baseline personality" that skills build on

### Common Mistakes

- **Too vague:** "Be helpful and smart" tells Claude nothing useful.
- **Too long:** A 2,000-line CLAUDE.md buries the important stuff. Aim for under 200 lines for most projects.
- **Contradictory rules:** "Always be concise" followed by "Always explain your reasoning in detail" creates confusion.
- **No structure:** A flat list of 50 bullet points is hard for Claude (and humans) to parse.
- **Forgetting to update:** A CLAUDE.md that describes last quarter's project structure actively misleads Claude.

### A Real Working Example

Want to see a CLAUDE.md in action? You're living inside one right now. The course's own CLAUDE.md (at the root of this course folder) defines Claude's role as your tutor, sets teaching rules, manages progress tracking, and defines all the commands you've been using. It's a real, working example of everything we just covered.

---

## Practice

Time to write your own CLAUDE.md for a real project.

Think of a project you work on — it could be a codebase, a documentation folder, a data analysis workspace, or anything you use regularly.

**Step 1:** Create a new file at `workspace/my-project-claude.md`.

**Step 2:** Write a **Role Definition** section. Who should Claude be when working in this project? What expertise should it bring?

**Step 3:** Write a **Project Context** section. What are the key things Claude needs to know? Important files, team conventions, terminology?

**Step 4:** Write at least **5 Behavioral Instructions**. Be specific — think about what you'd tell a new teammate on day one. What should they always do? What should they never do?

**Step 5:** Add a **References** section pointing to key files or resources (even if they're hypothetical for now).

**Success Criteria:**
- Created a CLAUDE.md with a clear role definition
- Included meaningful project context
- Has at least 5 specific behavioral instructions
- References relevant files or resources

> **Feeling comfortable?** You can always skip ahead with `/skip` or type `/course` to see the full menu.

---

## Challenge

Now put your reviewer hat on. Look at the CLAUDE.md you just created in the Practice step and critique it yourself.

**Step 1:** Re-read your CLAUDE.md with fresh eyes. Pretend you're Claude encountering it for the first time.

**Step 2:** Ask yourself:
- Is the role definition specific enough, or could it apply to anyone?
- Are the behavioral instructions actionable? Could Claude actually follow them?
- Is anything missing that a new teammate would need to know?
- Are there any contradictions?

**Step 3:** Ask Claude to critique it too:

> "Read my CLAUDE.md at `workspace/my-project-claude.md` and give me honest feedback. What's strong? What's vague? What's missing? How would you improve it?"

**Step 4:** Improve your CLAUDE.md based on the feedback.

**Success Criteria:**
- Reviewed their own CLAUDE.md critically
- Got feedback from Claude
- Made at least 2 improvements based on the critique

> **Reminder:** `/course` shows the full menu, `/skip` jumps ahead, and there's a cheat sheet at `reference/cheat-sheet.md`.
