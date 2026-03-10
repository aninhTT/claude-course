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

### Core Connectors

These are the ones you'll use most:

**Granola** — Your meeting note-taker. When connected, Claude can search your meeting notes, pull action items, and reference what was discussed. If you use Granola for meetings, this is a must-have.

**Google Suite** — Calendar, Gmail, Drive. Claude can check your schedule, read emails, and access documents. Essential for any workflow that involves your calendar or inbox.

**Slack** — Read messages, search channels, and even send messages. This is how Claude stays in the loop on what's happening across your team.

### Additional Connectors

**Jira** — If you use Jira for project tracking, Claude can read issues, create tasks, and update statuses.

**Confluence** — Access your team's documentation and knowledge base.

**GitHub** — For code repos and deployment (we'll cover this in Module 6).

### How Connectors Work

Connectors use a secure authentication flow — you approve access once, and Claude can use that connection going forward. Each connector has specific permissions (read, write, etc.) that you control.

Think of connectors as giving Claude eyes and hands for your tools. Without them, Claude is smart but blind to your work context. With them, it can actually help with your real tasks.

## Practice

Let's get your core tools connected. We'll do this step by step.

**Step 1:** Check which connectors you already have set up. In your Claude Code settings, look for the connectors or integrations section.

**Step 2:** Connect these core tools (if not already connected):
- Google Suite (Calendar, Gmail)
- Slack
- Granola (if you use it)

**Step 3:** Verify each connection works by asking Claude a simple question:
- "What's on my calendar today?"
- "Show me my latest unread emails"
- "What Slack messages did I get this morning?"

**Success criteria:** At least 2 core connectors connected and verified with a test query.
