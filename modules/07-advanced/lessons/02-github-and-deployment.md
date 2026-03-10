---
module: 7
lesson: 2
title: "GitHub & Deployment"
difficulty: advanced
prerequisites: "7.01"
---

# Lesson 7.02: GitHub & Deployment

## Learn

You've been building things — skills, prototypes, workflows. Now let's talk about how to share, store, and deploy them. That means GitHub.

> 💡 **Don't have GitHub?** No worries — this lesson is optional for non-developers. Feel free to skip it and come back later if you ever need it. Use `/skip 7.03` to jump to the next lesson, or `/course` to see the full menu.

### What Is GitHub?

GitHub is a place to store, share, and version-control files. While developers use it for code, it works for anything text-based: skills, templates, documentation, configuration files, prototypes. Think of it as a combination of:

- **A filing cabinet** that keeps every version of every file you've ever saved
- **A collaboration tool** where others can see your work, suggest changes, or use what you've built
- **A deployment platform** where things you build can be shared or run

You don't need to be a developer to use GitHub. You need to understand about four concepts.

### Basic Git Concepts (Just Enough to Be Useful)

**Repository (repo):** A folder for your project on GitHub. It contains all your files and the history of every change you've made. You might have one repo for your skills, another for a prototype, another for shared templates.

**Commit:** A saved snapshot of your files at a point in time. Every time you make a change and want to save it, you create a commit with a short message describing what changed. Think of it like "Save As" but it keeps every previous version too.

**Branch:** A parallel version of your files where you can make changes without affecting the main version. Useful when you're experimenting or working on something that isn't ready yet. The main branch (called `main`) is the "official" version.

**Push:** Sending your local changes to GitHub so they're saved online and visible to others.

That's it. There are more concepts, but these four are enough to get real work done.

### Why Connect Claude Code to GitHub?

- **Deploy prototypes** so others can access and use them
- **Share skills** with your team — push a SKILL.md to a shared repo and anyone can use it
- **Version your work** so you can always go back to a previous version
- **Collaborate** — others can see what you've built, suggest improvements, or build on top of it

### What You Can Deploy

Anything you've built in this course is deployable:
- Skills (SKILL.md files)
- Prototypes and tools
- Templates and workflows
- CLAUDE.md configurations
- Documentation and guides

### How to Connect Claude Code to GitHub

Claude Code can interact with GitHub directly. If you have the GitHub CLI (`gh`) installed and authenticated, Claude can create repos, push files, and manage branches on your behalf. If you haven't set this up yet, Claude can walk you through the process in the Practice section.

## Practice

Let's get something onto GitHub.

**Step 1: Check your GitHub connection.** Ask Claude to check if GitHub is connected. If it isn't, ask Claude to help you set it up. This typically involves installing the GitHub CLI and authenticating.

**Step 2: Create a repo (or use an existing one).** If you don't have a repo for your course work yet, ask Claude to create one. Something like:

> "Create a GitHub repo called 'claude-code-toolkit' with a description of 'Skills, prototypes, and tools built with Claude Code.'"

If you already have a repo you'd like to use, that works too.

**Step 3: Push a file.** Pick something you've built during this course — a skill, a prototype, a template, anything. Ask Claude to push it to the repo. Walk through the basic flow together:

1. Create the repo (if it doesn't exist)
2. Add the file
3. Write a commit message describing what you're adding
4. Push to GitHub

Claude handles the Git commands. You focus on what to push and what to call it.

**Success criteria:** Successfully pushed at least one file to a GitHub repo with Claude's help. The file should be visible on GitHub.

## Challenge

Deploy something useful. Pick the best artifact you've created during this course — a skill, a prototype, a tool — and push it to GitHub in a way that others could actually find and use it.

**Step 1: Choose your artifact.** What's the most useful thing you've built? Something a teammate could benefit from?

**Step 2: Push it to GitHub.** If it's not already in a repo, create one or add it to an existing one.

**Step 3: Write a README.md.** Ask Claude to help you create a README for the repo that explains:
- What the artifact is
- What problem it solves
- How to use it (step by step)
- Any prerequisites or setup needed

A good README turns a file on GitHub into something someone else can actually use without asking you questions.

**Success criteria:** Created a GitHub repo with a deployed artifact and a README.md that explains what it is and how to use it.
