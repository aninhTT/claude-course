---
module: 1
lesson: 3
title: "Why Folders Matter"
difficulty: beginner
prerequisites: "1.02"
videos:
  - url: "https://www.loom.com/share/e23de5c1e5f84dfda7b98ca4346685b3"
    title: "Importance of Folders"
    duration: "~3 min"
    context: "Watch this to understand why folder structure is so important"
---

# Lesson 1.03: Why Folders Matter

## Learn

Here's something that surprises most people: **folders are the foundation of everything** in Claude Code and Cowork. This isn't just about file organization — it's about how Claude understands your work.

> Already comfortable with this topic? Skip ahead anytime with `skip` followed by the next lesson number.

### The Mental Model

When you open a folder in Claude Code, Claude reads the files in that folder to understand context. The most important file? **CLAUDE.md** — a special file at the root of your folder that tells Claude how to behave.

Think of it this way:
- **The folder** = Claude's workspace (what it can see and work with)
- **CLAUDE.md** = Claude's instructions (how it should behave in this workspace)
- **Other files** = Claude's context (what it knows about your project)

### What Is a Markdown File?

You'll see `.md` files throughout this course — CLAUDE.md, SKILL.md, MODULE.md. The `.md` stands for **Markdown**, which is a simple text format that's easy for both humans and computers to read.

Markdown lets you write structured text using simple symbols: `#` for headings, `**` for bold, `-` for bullet points. You don't need to learn any code — if you can write a text message, you can write Markdown. Claude reads and writes Markdown natively, which is why it's the standard for instructions, skills, and documentation.

**CLAUDE.md is just a Markdown file named CLAUDE.md.** Claude looks for this specific filename when it opens a folder. That's what makes it special — not the format, but the name and location.

### You're Living Inside This Right Now

Here's the fun part: **this course is a folder.** The reason Claude is acting as your tutor right now? There's a CLAUDE.md file in this course folder that says "You are a course tutor." That's it. That's the magic.

When you opened this folder, Claude read that CLAUDE.md and became your instructor. When you open a different folder, Claude becomes whatever that folder's CLAUDE.md tells it to be.

### How Cowork Uses Folders

Cowork also reads from folders. When you point Cowork at a folder and give it a task, it uses the folder's contents as context. The better organized your folder, the better Cowork performs.

### Why This Matters for You

Every project, workflow, or workspace you create should be a folder with:
1. A clear structure
2. A CLAUDE.md that gives Claude context about the project
3. Any relevant files Claude might need

This is the pattern you'll use for everything — from simple task automation to complex project workflows.

There's a quick video that shows why folder structure matters so much: https://www.loom.com/share/e23de5c1e5f84dfda7b98ca4346685b3

## Practice

Let's explore the course folder itself as a learning example.

**Step 1:** Look at the structure of this course folder. Ask Claude to show you what's in this directory. See if you can identify the key pieces: CLAUDE.md, progress.json, the modules folder, the workspace, the reference materials.

Now answer this: If you wanted to create a folder that made Claude act as a meeting prep assistant, what would you put in its CLAUDE.md?

**Success criteria:** Learner has explored the course folder structure and can articulate what goes in a CLAUDE.md file and why.

## Challenge

Here's a challenge: **go physically find this course folder on your computer.** Open your file explorer (Finder on Mac, File Explorer on Windows) and navigate to wherever you opened this folder from. Open it up and look at all the files and folders inside.

Browse around — open the `modules/` folder, peek at a few `.md` files in a text editor, look at the `workspace/` and `reference/` folders. This is what a Claude Code project looks like under the hood. Everything Claude is reading and responding to is just files in this folder.

Understanding how to find and browse the actual files on your computer is a skill you'll use constantly — whether it's checking what Claude created, organizing your projects, or sharing your work with others.

> **Before you're done — Question It:** What did Claude assume? What's missing? What could break?

**Success criteria:** Found the course folder on your computer, browsed the file structure, and opened at least one .md file in a text editor to see what's inside.
