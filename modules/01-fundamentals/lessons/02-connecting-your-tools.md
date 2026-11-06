---
module: 1
lesson: 2
title: "Connecting Your Tools"
difficulty: beginner
prerequisites: "1.01"
---

# Lesson 1.02: Connecting Your Tools

## Learn

Claude Code and Cowork become much more powerful when they can access your actual tools — Slack, Gmail, Calendar, Granola, and more. These connections are called **connectors** (or MCP integrations). They let Claude read from and interact with the tools you use every day.

> Already comfortable with this topic? Skip ahead anytime with `skip` followed by the next lesson number.

### Core Connectors

These are the ones you'll use most:

**Granola** — Your meeting note-taker. When connected, Claude can search your meeting notes, pull action items, and reference what was discussed. If you use Granola for meetings, this is a must-have.

**Google Suite** — Calendar, Gmail, Drive, Docs, Sheets, and Slides. Claude can check your schedule, read emails, and read and create documents. Essential for any workflow that involves your calendar, inbox, or Google files.

**Slack** — Read messages, search channels, and even send messages. This is how Claude stays in the loop on what's happening across your team.

### Additional Connectors

**Jira** — If you use Jira for project tracking, Claude can read issues, create tasks, and update statuses.

**Confluence** — Access your team's documentation and knowledge base.

**Linear** — If your team tracks work in Linear, Claude can look up issues and projects.

**GitHub** — For code repos and deployment (we'll cover this in Module 8).

### Claude Inside Google Docs, Sheets & Slides

At Thumbtack, the **Google Docs, Sheets & Slides connectors** are turned on, so you can use them right away. They let Claude create and edit Google files from a conversation — "Put this summary in a new Google Doc" or "Add these numbers to my tracking sheet."

There's also the **Claude for Google Workspace add-on** (in beta), which puts Claude in a sidebar inside Docs, Sheets, and Slides, where it works on the file you have open.

### How Connectors Work

Connectors use a secure authentication flow — you approve access once, and Claude can use that connection going forward. Each connector has specific permissions (read, write, etc.) that you control.

Think of connectors as giving Claude eyes and hands for your tools. Without them, Claude is smart but blind to your work context. With them, it can actually help with your real tasks.

## Practice

Let's get your core tools connected. We'll do this step by step.

**Step 1:** Check which connectors you already have set up. In the Claude app, open **Customize** and go to **Connectors** — that's where connectors live, alongside your skills and plugins.

**Step 2:** Connect these core tools (if not already connected):
- Google Suite (Calendar, Gmail, Drive, Docs, Sheets, Slides)
- Slack
- Granola (if you use it)

**Step 3:** Verify each connection works by asking Claude a simple question:
- "What's on my calendar today?"
- "Show me my latest unread emails"
- "What Slack messages did I get this morning?"
- "Find the Google Doc I edited most recently and summarize it in two lines"

**Success criteria:** At least 2 core connectors connected and verified with a test query.

## Challenge

**Cross-Tool Query**

The goal: Use your connected tools together to answer a real work question in one ask.

Try this prompt right here in this session:

> "Look at my calendar for today and tell me which meetings I should prep for, and check if there are any relevant emails related to those meetings."

This requires Claude to pull from **two connectors at once** (Calendar + Gmail) and synthesize the results into something actually useful.

Give it a shot — ask that question (or your own version of it) and let's see what happens. I'll step back and let you drive.

> **Before you're done — Question It:** What did Claude assume? What's missing? What could break?

**Success criteria:** Claude successfully combines data from at least 2 connectors to answer a single real-work question.
