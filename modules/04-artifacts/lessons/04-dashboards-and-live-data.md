---
module: 4
lesson: 4
title: "Dashboards & Live Data"
difficulty: intermediate
prerequisites: "4.03"
---

# Lesson 4.04: Dashboards & Live Data

## Learn

Docs, slides, and designs are mostly words and visuals. **Dashboards** are about numbers: a page of charts, metrics, and tables built from your data. You ask in plain language — "show me ticket volume by week for the last quarter" — and Claude finds the data, builds the charts, and lays out the page.

> Already comfortable with this topic? Skip ahead anytime with `skip` followed by the next lesson number.

> 💡 **Beta:** Dashboards are in beta. If you don't see the option, your admin may not have turned it on yet.

### Where the Data Comes From

A dashboard can be built from:
- **A file you upload** — a spreadsheet or CSV
- **Your connectors** — the tools you connected in Module 1, like your calendar or Linear
- **A data warehouse** — such as BigQuery, if you have access to it

Behind the scenes, Claude writes the queries or calculations. You never have to.

### Every Number Shows Where It Came From

This is the most important thing about dashboards: **every chart and number shows its source** — the query or calculation behind it, and when it was last refreshed.

That matters because of one of our core agreements: **Always Verify Output.** A dashboard is the easiest place for a confident-looking mistake to hide. A chart can look perfect and still be counting the wrong thing — test accounts included, the wrong date range, cents instead of dollars.

Before you trust or share a dashboard:
1. **Pick the number that matters most** and open its source.
2. **Read the query or calculation in plain English** — ask Claude, "Explain how you calculated this number."
3. **Spot-check it** against something you already know is true.

### Live Data and Who Sees What

When a dashboard pulls from connectors, **each viewer uses their own connections**. If you share a dashboard built on your connectors, a teammate sees the data *they* have access to — not yours. That's good for privacy, but it means two people can see different numbers on the same dashboard. Keep it in mind when you share.

### Beyond Dashboards: Small Interactive Tools

Artifacts can also be small working tools — a calculator, a tracker, a checklist. Remember the app you built in Lesson 1.06? As an artifact, a tool like that can be shared with a link, and it can even **save data**, so a team tracker remembers what people entered. If a tool needs to think — say, summarizing what someone pastes in — it can use Claude too, running on each viewer's own account.

## Practice

Build a small dashboard and verify one number.

**Step 1: Pick your data.** Choose whatever you have access to:
- **Easiest:** upload a spreadsheet or CSV you already use
- **Connectors:** your calendar ("How many hours of meetings did I have each week this month, by type?") or a project tool like Linear
- **Warehouse:** a BigQuery table, if you already query it for your work

**Step 2: Ask for a dashboard.** Say what you want to *learn*, not just what to chart:

> "Build a dashboard from this spreadsheet that shows me where our team's requests come from and how long they take to close. Include a short note on how to read each chart."

**Step 3: Open the source of one number.** Pick the most important number and look at where it came from.

**Step 4: Verify it.** Ask Claude to explain the calculation in plain English, then spot-check it against the raw data.

**Success criteria:** Built a dashboard from real data, opened the source behind at least one number, and verified it against the original data.

## Challenge

**Make it trustworthy enough to share.** Turn your dashboard into something a teammate could rely on without asking you questions:

1. Add a one-line definition for every metric ("Time to close = days from request to resolved, weekdays only").
2. Verify **every** number, not just one. Fix anything that's off.
3. Add a "last checked" note and any known limits ("Excludes requests sent by email").
4. Bonus: ask a teammate to read it cold and tell you what they think it says.

> **Before you're done — Question It:** What did Claude assume? What's missing? What could break?

**Success criteria:** Every metric is defined and verified, and the dashboard states its limits clearly enough for someone else to use.
