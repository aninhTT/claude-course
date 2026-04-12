---
module: 1
lesson: 6
title: "Your First Build"
difficulty: beginner
prerequisites: "1.05"
---

# Lesson 1.06: Your First Build

## Learn

In the last lesson, you had a conversation with Claude Code and got useful output. Now let's take the next step — actually **building something** that only Claude Code can do.

> Already comfortable with this topic? Skip ahead anytime with `skip` followed by the next lesson number.

### The Magic of Claude Code: You Don't Need to Write Code

Here's the most important thing to understand: **Claude Code can build things that require code — and you don't have to write any of it.** Claude writes the code for you. You just describe what you want.

This means anyone can build:
- A **simple web app** (like a personal dashboard, a team directory, or a project tracker)
- An **interactive tool** (like a calculator, a quiz, or a decision-making flowchart)
- A **data visualization** (charts from a spreadsheet, a timeline, a kanban board)
- A **custom form** that collects and organizes information
- A **prototype** of an idea you've been thinking about

Sometimes if you're building something that feels more complex — an interactive tool, a data visualization, a custom app — Code is always the most flexible tool. It can create and run files directly, which gives you a level of creative power the other tools can't match.

### Building in the Workspace

For this lesson, we'll build inside the `workspace/` folder that's part of this course folder — the same folder you opened to start this course. If you go find that course folder on your computer (in Finder or File Explorer), you'll see `workspace/` right inside it. This is your sandbox — build freely here.

> 💡 **Remember:** Everything Claude creates lives in your folder. After Claude builds something, check the `workspace/` folder inside your course folder to see the files it created. You can always find what Claude made by looking in the folder you told it to build in.

### The Build Pattern

When building something with Claude Code, follow this pattern:

1. **Describe what you want** — Be clear about the purpose and who it's for
2. **Let Claude draft it** — Claude will create the file(s) and write any code needed
3. **Review and iterate** — Look at what Claude created, try it out, and refine
4. **Test it** — Make sure it works the way you want

You don't need to understand the code Claude writes. Focus on describing what you want and reviewing whether the result matches your vision.

### Start with Plan Mode

When you're about to build something, switch Claude Code into **plan mode** first. Look for the dropdown in the chat input area — change it from the default to **Plan**. In plan mode, Claude will think through the approach before writing any code. You review the plan, give feedback, and then Claude builds.

This is a best practice for any build: **plan first, build second.**

> ⏭️ **Feeling comfortable?** If you already get the concept, feel free to skip ahead to the Practice section or jump to the next module with `/skip 2.01`.

## Practice

Let's build something that only Code can do — a simple, functional app.

**Step 1:** Think about something that would be genuinely useful in your work. Here are some ideas to get you started:

- A **personal dashboard** that shows your priorities, upcoming meetings, and key metrics
- A **team standup tool** where you fill in fields and it formats a standup update
- A **meeting cost calculator** that estimates cost based on attendees and duration
- A **decision log app** where you can add decisions, tag them by project, and search
- A **quick reference tool** for something your team always looks up (policy numbers, contact info, process steps)

**Step 2:** Tell Claude what you want to build. Be specific about what it should do and who it's for. For example:

> "Build me a simple meeting cost calculator app in the workspace/ folder. It should let me enter the number of attendees, average salary level, and meeting duration, then calculate the estimated cost. Make it look clean and professional."

**Step 3:** Check what Claude created. Go find the `workspace/` folder inside your course folder and look for the files Claude made. If it's a web app (HTML file), Claude can help you open it. Try it out — does it work?

**Step 4:** Ask Claude to improve it. "Add a dark mode toggle," "Make the font bigger," "Add an export button" — iterate until you're happy.

> 💡 **It doesn't need to be perfect or 100% functional.** This exercise is just to give you a sense of what's possible in Code. We'll cover more best practices for building later on. Progress over perfection!

**Success criteria:** Built a functional tool or app in workspace/ that does something useful — not just a static document. Claude wrote the code; you directed what to build. Iterated at least once.

> ⏭️ **Challenges are always optional.** If you want to move on, skip ahead to Module 2 with `/skip 2.01`. Challenges are here for extra learning if you want it.

## Challenge

Build something more ambitious — a tool that combines information from your connected tools into something interactive.

For example:
- A **weekly dashboard** that pulls your calendar events, recent Slack highlights, and to-dos into one visual page
- A **meeting prep app** that auto-fills with info from your calendar and Granola notes for the next meeting
- A **project tracker** that you can update with status and share with your team

Ask Claude to help you figure out the right thing to build if you're not sure. Remember: you don't need to know how to code. Just describe what you want.

Once you've built it, take a moment: look at what Claude created and find one assumption it made that you didn't explicitly state.

> **Before you're done — Question It:** What did Claude assume? What's missing? What could break?

**Success criteria:** Built a more ambitious interactive tool that uses connected tool data. More complex than the Practice build.
