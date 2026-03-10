---
module: 5
lesson: 5
title: "Context Files for Cowork"
difficulty: intermediate
prerequisites: "5.04"
---

# Lesson 5.05: Context Files for Cowork

## Learn

In the last lesson, you learned how CLAUDE.md shapes Claude's behavior in a folder. Now let's take that concept further — into Cowork specifically.

Here's the insight: **instead of writing better prompts, you can build a knowledge base about yourself.** Context files flip the usual AI approach on its head. Rather than crafting the perfect instruction every time, you create files that Claude reads before every task. One great markdown file is worth more than 50 random uploads.

### What Are Context Files?

Context files are markdown documents that live in a dedicated folder and tell Claude who you are, how you work, and what you've done before. When you point Cowork at this folder (or upload these files), Claude reads them first — and suddenly it's not a generic assistant. It's one that knows your voice, your priorities, and your preferences.

Think of it this way: CLAUDE.md tells Claude how to *behave*. Context files tell Claude who *you* are.

### Building Your Context Folder

A well-organized context folder has four parts:

**1. ABOUT ME** — Your foundational identity documents

This is where Claude learns who you are. Create an `about-me.md` that covers:
- Your role and what you're responsible for
- Your current priorities and what matters most right now
- Your communication style — how you write, how you want things to sound
- An example of work you're genuinely proud of (this is gold for voice matching)

You can also create a separate style guide — what some people call an "anti-AI writing style" doc. This tells Claude specifically what to avoid:
- No corporate buzzwords like "leverage" or "synergize"
- No filler phrases like "I hope this email finds you well"
- No bullet points when a paragraph would be better (or vice versa)
- Examples of what you DO want vs. what you DON'T want

**2. PROJECTS** — Active work organized by initiative

One subfolder per project, containing:
- Briefs, reference docs, and relevant materials
- Past drafts and finished work
- Anything Claude might need to produce context-aware output

This keeps things organized and means Cowork doesn't have to wade through irrelevant material to find what it needs.

**3. TEMPLATES** — Proven patterns worth reusing

Have a status update format your team loves? A meeting notes structure that works? A presentation outline that always lands? Put the *structure* here — not the content. Claude learns your preferred layouts and applies them to new work.

**4. CLAUDE OUTPUTS** — Where deliverables go

Give Claude a designated place to put finished work. This keeps things clean and makes it easy to find what Claude produced vs. what you uploaded as input.

### Global Instructions: Your Always-On Context

There's a powerful setting most people miss: **Global Instructions for Cowork.**

Navigate to **Settings → Cowork → Edit Global Instructions** and paste instructions that run before *every* Cowork task. This is where you tell Claude:

- Always read your About Me folder before starting any task
- Always check for relevant project context in the Projects folder
- Study the Templates folder before producing any deliverable
- Save all outputs to the Claude Outputs folder
- Use specific naming conventions (e.g., `project_content-type_v1.md`)

This eliminates repeating the same setup instructions in every prompt. It's like CLAUDE.md but specifically for Cowork sessions.

### Why This Matters

The blog post that inspired this lesson puts it well: the system philosophy inverts traditional AI usage. Instead of mastering prompt engineering, you build a searchable knowledge base about yourself and let Claude learn how to work with you.

With context files in place, your prompts can be incredibly simple:

> "Write the project update for Q1. Explore my context folder first."

Claude already knows your voice, your format preferences, your project details, and where to put the output. You didn't need a 500-word prompt — the context files did the work.

---

## Practice

Let's build your personal context folder — the one you'll actually use with Cowork going forward.

**Step 1: Create the folder structure.**

In this course workspace, create this structure:

```
workspace/my-cowork-context/
├── about-me/
├── projects/
├── templates/
└── outputs/
```

Ask Claude to create these folders for you.

**Step 2: Write your About Me doc.**

Create `workspace/my-cowork-context/about-me/about-me.md`. Include:
- Your name and role
- Your top 3 current priorities
- How you prefer to communicate (formal vs. casual, short vs. detailed, etc.)
- One example of work you're proud of — paste in a paragraph from a real doc, email, or message you wrote that represents your voice well

**Step 3: Create a style guide.**

Create `workspace/my-cowork-context/about-me/my-style.md`. Include at least 5 "do this, not that" examples. Think about:
- Words or phrases you never want Claude to use
- Your preferred level of formality
- How you structure emails, updates, or documents
- Any pet peeves about AI-generated text

**Step 4: Add one template.**

Think of a format you reuse regularly — a weekly update, a meeting summary, a project brief. Create it at `workspace/my-cowork-context/templates/` with the structure but not the content.

**Step 5: Test it.**

Open a new Cowork session, point it at your `my-cowork-context` folder, and give it a task — something you'd normally do, like drafting a message or writing an update. See if the output sounds more like you than a generic AI response.

**Success Criteria:**
- Created the 4-folder structure (about-me, projects, templates, outputs)
- Wrote an about-me document with role, priorities, and communication style
- Created a style guide with at least 5 preferences
- Added at least one reusable template
- Tested by running a Cowork task using the context folder

---

## Challenge

Take this to the next level: write **Global Instructions** for your Cowork setup.

Draft a set of instructions at `workspace/my-cowork-context/global-instructions-draft.md` that you could paste into Cowork's Global Instructions setting. Your instructions should tell Claude:

1. What to read before starting any task (which folders, which files)
2. How to use your templates (when to follow them vs. when to freestyle)
3. Where to save outputs and how to name them
4. Any specific rules about your preferences (from your style guide)
5. When to ask you questions vs. when to just execute

Then actually paste them into your Cowork settings: **Settings → Cowork → Edit Global Instructions**.

**Success Criteria:**
- Drafted Global Instructions that reference your context folder structure
- Instructions cover: what to read, how to use templates, where to save, naming conventions
- Pasted the instructions into Cowork's Global Instructions setting

> **Hint system:** Use `/hint` if you're stuck. First hint is a nudge, second is more specific, third nearly gives it away.

---

> **Congratulations on completing Module 5!** You've gone from building your first skill to mastering custom skills, scheduling, best practices, CLAUDE.md, and context files. You're officially an intermediate skill builder. Next up: Module 6, where you'll build your top use cases end-to-end.
