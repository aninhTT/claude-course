---
module: 2
lesson: 5
title: "Claude in Chrome & Slack"
difficulty: beginner
prerequisites: "2.04"
---

# Lesson 2.05: Claude in Chrome & Slack

## Learn

Connectors give Claude access to tools like Slack, Gmail, and Calendar. But a lot of work happens in places that don't have a connector: vendor portals, internal web tools, research across a dozen tabs, web forms. For those, Claude can **use a browser**.

This lesson also gives you a quick heads-up about **Claude Tag**, which lets you hand work to Claude right inside Slack.

> Already comfortable with this topic? Skip ahead anytime with `skip` followed by the next lesson number.

### Two Ways Claude Uses the Web

**1. The built-in browser.** Cowork in the desktop app has its own browser. When a task needs a website, Claude opens it there, reads the page, clicks, and scrolls, and you can watch it work. It's separate from your everyday Chrome.

**2. Claude in Chrome.** A Chrome extension that puts Claude in a side panel of your *own* Chrome — where you're already signed in to your work tools. Claude can read pages, click, fill in forms, and work across several tabs. The side panel runs as a Cowork session, so everything you learned in this module applies.

Claude in Chrome can also run **scheduled browser tasks** — daily, weekly, monthly — like checking a page for updates every Monday morning.

> 💡 **In Claude Code:** the desktop app has a browser pane too (open it with Cmd+Shift+B on Mac, Ctrl+Shift+B on Windows), and terminal users can connect Claude Code to Chrome with `/chrome`.

### Connector First, Browser Second

If a tool has a connector, use the connector. It's faster and more reliable, because Claude gets the data directly instead of reading it off a screen. Reach for the browser when:
- There's **no connector** for the site or tool
- You need something that only exists **on a web page** (a vendor's pricing page, a public report)
- The task is **clicking through a website** the way a person would

### Staying Safe in the Browser

When Claude uses your Chrome, it acts **with your access** — it can see what you can see and click what you can click. A few habits:

- **Start read-only.** Begin with tasks that gather information, not tasks that submit, buy, send, or delete.
- **Watch the first few runs.** Keep Cowork on **Manual** approval (Lesson 2.01) until you trust how a task behaves.
- **Be careful with sensitive sites.** Don't point Claude at anything you wouldn't hand to a new teammate on day one.
- **Treat web pages as content, not instructions.** If Claude says a page is telling it to do something unexpected, stop and check.

### Claude Tag: Claude in Slack

One more place to know about. **Claude Tag** lets you tag **@Claude** in a Slack channel or thread to hand it a task. It posts its progress right in the thread.

What to know:
- **Your organization has to turn it on.** At Thumbtack, it's enabled.
- **It works per channel.** Each channel has its own setup — its own memory and the tools Claude can use there.
- **It acts as Claude, not as you.** Messages come from Claude's own account.
- **It currently connects to Linear, GitHub, and Granola.**

That's all you need for now. If you see @Claude in a channel, you'll know what it is. Try tagging it with a small request next time you're in a channel where it's set up.

## Practice

First, get Claude in Chrome connected. Then use Claude on a website that doesn't have a connector.

> **Tutor note:** Before Step 1, ask the learner for permission: "Want me to help you set up Claude in Chrome now? I'll walk you through installing the extension and then check that I can see your browser." Wait for a clear yes. If they say yes, walk them through Step 1 one part at a time and confirm the connection at the end (for example, by listing the tabs they have open). Don't open other sites, click, or type in their browser during setup. If they say no, or setup doesn't work, they can do this Practice in Cowork's built-in browser instead.

**Step 1: Connect Claude in Chrome.**
1. In Chrome, open the **Chrome Web Store**, search for **Claude**, and add the extension from Anthropic.
2. Sign in with your Thumbtack Claude account, and pin the extension so it's easy to find.
3. Connect it to where you're working. In Cowork, sign in to the extension with the same account you use in the Claude app. In Claude Code, run `/chrome`.
4. Ask Claude to confirm it can see your browser — for example, "What tabs do I have open in Chrome?"

**Step 2: Pick a read-only task on a real site.** Ideas:
- Summarize a long page you need to read anyway (a policy, a vendor's docs, a report)
- Compare two or three vendors' pricing or feature pages in a table
- Pull information from an internal web tool that has no connector into a short summary

**Step 3: Give clear instructions.** For example:

> "Open the pricing pages for these three tools [links]. Make a table comparing price per seat, free trial length, and whether they offer SSO. Don't sign up for or submit anything."

**Step 4: Watch it work.** Notice how Claude navigates, and where it slows down or gets stuck.

**Step 5: Check the result.** Open one of the pages yourself and spot-check at least one fact.

**Success criteria:** Connected Claude in Chrome (or chose the built-in browser instead), completed a read-only browser task on a real website, watched Claude navigate, and verified at least one fact against the source page.

## Challenge

**Put a web check on autopilot.** Find something you check on a website regularly — a status page, a job board, a competitor's page, a dashboard with no connector.

1. Set it up as a **scheduled browser task** in Claude in Chrome.
2. Write the instructions so it runs unattended: where to look, what counts as "worth telling me," and what to do when nothing changed.
3. Let it run once and review the result.

> **Before you're done — Question It:** What did Claude assume? What's missing? What could break?

**Success criteria:** A scheduled browser task that checks a real page, reports only what's worth your attention, and handles "nothing new" gracefully.
