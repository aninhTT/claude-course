---
module: 4
lesson: 1
title: "Artifacts 101"
difficulty: beginner
prerequisites: "3.05"
---

# Lesson 4.01: Artifacts 101

## Learn

So far, most of what you've made with Claude has landed as files in a folder or as text in a conversation. That works for you — but most work at Thumbtack ends up in front of *other people*: a doc your manager reviews, a deck for a team meeting, a one-pager for a launch.

That's what **artifacts** are for. An artifact is a finished piece of work — a doc, a deck, a design, a dashboard, an animation — that opens beside your conversation, lives at its own link, and can be shared, commented on, and edited.

> Already comfortable with this topic? Skip ahead anytime with `skip` followed by the next lesson number.

### The Five Types

| Type | What it's for | Example |
|------|---------------|---------|
| **Docs** | Documents people read and edit together | Project brief, memo, meeting recap |
| **Slides** | Presentation decks | Team update, kickoff deck |
| **Design** | Visual layouts on a canvas | One-pager, flyer, landing page mockup, Slack graphic |
| **Dashboards** *(beta)* | Charts and numbers from your data | Weekly metrics, project tracker |
| **Motion** *(beta)* | Short animations exported as video | Animated explainer, product walkthrough |

You don't need to memorize these. Describe what you need — "turn this into a deck," "make this a one-pager" — and Claude picks the right type.

> 💡 **Beta types:** Dashboards and Motion are newer and still in beta. If you don't see one, your admin may not have turned it on yet.

### Where Artifacts Live

- They **open beside your conversation**, so you can see and change them while you talk to Claude.
- In the Claude app, they're collected in the **Artifacts** tab in the sidebar — that's where you find them later.
- Each one has its **own link**, and it **starts private**. Nobody else sees it until you share it. (Sharing is covered in Lesson 4.05.)

You can make artifacts in a chat, in Cowork, or right here in Claude Code. Just ask. (In the Claude Code terminal there are also shortcuts like `/slides` and `/design`, but plain language works everywhere.)

### You Have Plenty of Ways to Share

Artifacts give you a lot of new ways to share your work. But they aren't the only way, and they don't replace the tools your team already uses. **Google Docs, Sheets, and Slides still work great**, and Claude can write straight into them with the Google connectors from Lesson 1.02. You can also export most artifacts to Google Docs or Google Slides.

| | Artifact | Google Doc, Sheet, or Slides | File in a folder |
|---|----------|------------------------------|------------------|
| **Best for** | Things people will read, watch, or use, especially when you want comments or live data | Work that belongs where your team already collaborates | Things Claude or a tool will use (skills, CLAUDE.md, data) |
| **Lives** | At its own private link | In Google Drive | On your computer |
| **Sharing** | Share the link with view, comment, or edit access | Normal Google sharing | Send the file around |

Rule of thumb: **put it where your audience already works.** If your team lives in a shared Google Drive folder, a Google Doc may be the better choice. If you want a live dashboard or a one-off visual, an artifact may be. And if Claude or a tool is the audience, keep it a file.

### Watch Out for Artifact Fatigue

Artifacts are fast to make, and that's exactly the risk. If everyone shares every doc, deck, and dashboard they generate, people stop opening them.

Before you share, use your judgment:
- **Does this need to be shared at all?** Some artifacts are just for your own thinking.
- **Who is it for, and what do they need?** Start from your audience, not from what Claude made.
- **Which one version is best?** If you made a doc *and* a deck *and* a one-pager, share the one that fits. You don't need to send all three.
- **Would something simpler work?** Sometimes a three-line Slack message beats a link.

### Iterating on an Artifact

The first version is rarely the final one. You can:
- **Ask Claude** — "Make the intro shorter," "Add a slide on risks"
- **Edit it yourself** — click in and change the text directly
- **Leave a comment** — and have Claude act on it (more on this in the next lesson)

Remember **Always Verify Output**: an artifact *looks* finished, which makes it easy to trust. Read it like a reviewer before you share it.

> **Heads up:** Artifacts made in chats before September 2026 are now called *legacy artifacts*. They still work and can still be shared, but new artifacts use the types above.

## Practice

Turn something you already have into an artifact. The goal is to feel the difference between "a file I made" and "a thing I can share," and to decide on purpose whether it should be shared.

**Step 1: Pick your source — anything you want.** Some ideas:
- Something you made earlier in this course (your Cowork summary, your skill's output, your Module 1 build)
- Notes from a real meeting
- A rough draft of an email, plan, or update you need to write anyway
- A list or spreadsheet you keep updating by hand

**Step 2: Think about the audience first.** Who's going to look at this, and how? If they'll read it → Doc. If you'll present it → Slides. If they'll glance at it → Design or Dashboard. Also notice where they'd expect to find it. If the answer is "in our team's Google Drive," that's worth knowing.

**Step 3: Ask Claude to make it.** For example:

> "Turn my notes from this morning's project sync into a Doc my team can read — a short recap, the decisions we made, and action items with owners."

**Step 4: Find it.** Look at the artifact beside the conversation, then find it again in the **Artifacts** tab.

**Step 5: Improve it once.** Make one change by asking Claude and one change by editing it yourself.

**Step 6: Decide whether to share it.** Answer the four questions under "Watch Out for Artifact Fatigue." Is this worth sharing? If so, as an artifact, as a Google file, or as something shorter? It's fine to decide it was just for you.

**Success criteria:** Created at least one artifact from your own content, chose a type based on its audience, found it in the Artifacts tab, made at least one edit, and decided whether (and how) to share it.

## Challenge

**Same content, two shapes, one winner.** Take the content from your Practice and turn it into a *second* type — for example, a Doc and a 3-slide deck, or a Doc and a one-page Design.

Then compare:
- Which one would your actual audience prefer?
- What did Claude cut, change, or add when it switched formats?
- Is anything in either version wrong or made up?

Finally, pick **one** to keep. In real work, you'd share only the winner, not both.

> **Before you're done — Question It:** What did Claude assume? What's missing? What could break?

**Success criteria:** Created two artifact types from the same source, picked one, and can explain why it fits the audience better.
