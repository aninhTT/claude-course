---
module: 4
lesson: 2
title: "Docs & Slides"
difficulty: beginner
prerequisites: "4.01"
---

# Lesson 4.02: Docs & Slides

## Learn

Docs and Slides are the two artifact types you'll probably use most. Between them, they cover most of what knowledge workers make: briefs, plans, recaps, proposals, and presentations.

But the format is the *last* decision, not the first. Always start from **what your audience needs**.

> Already comfortable with this topic? Skip ahead anytime with `skip` followed by the next lesson number.

### Start From Your Audience

Before you ask Claude for anything, answer three questions:

1. **Who is it for?** Your manager, your team, another department, leadership?
2. **What do they need to do with it?** Make a decision, approve something, get up to speed, take an action?
3. **How will they take it in?** Read it alone, skim it between meetings, or see it presented in a meeting?

The answers pick the format for you:
- If they'll **read it on their own**, make a **Doc**.
- If you'll **present it**, make **Slides**.
- If they only need **one decision or one update**, maybe it's neither. A short Slack message or email might do the job.

There's no fixed order. You don't need to write a doc before you make a deck, or the other way around. Make the one thing your audience needs.

### Own the Outcome

Thumbtack's [AI Expectations](https://thumbtack.haystack.so/resources/c8602dcc-0898-4f92-ae93-243ee7d696ba) include a pillar that applies directly to every doc and deck you make with Claude:

> **Own the outcomes.** AI doesn't replace your judgment and discernment. Own it and remain fully accountable for the quality, accuracy and impact of your work. In practice, that means sharing work (documents, artifacts and messages in email or Slack) only once it's ready to review and act on. Ready means it's written for its audience, as short as it can be, and the ask/recommendation is easy to understand (drafts are okay, as long as you flag what you need reviewed). You should be able to explain and stand behind it, and your choices about what to include should be clear. If it took less time to create than it will take to consume it, it's probably not ready. When someone else's work isn't ready, tell them kindly and be specific. Use AI to make your communication clearer or faster, not to stand in for you or for the relationships you need to build.

Keep this in mind every time you generate an artifact. Claude's first version is a **starting point, not the finished product**. Expect to cut it down, sometimes by half. Expect to change what's on it. Don't share what Claude gives you without making it yours.

Before you share a doc or deck, check that it's **ready**:
- **Written for its audience?** It answers *their* questions, not every question.
- **As short as it can be?** Cut background, repetition, and anything they don't need to act.
- **Easy-to-find ask or recommendation?** Someone skimming should see it in seconds.
- **Can you stand behind it?** You could explain every line, and you know why each part is there.
- **The time test:** If it took you less time to make than it will take them to read, it's probably not ready.

> 💡 **Cutting help:** The **Clean Draft** skill you copied in Module 3 is built for exactly this. Run it on your draft to put the recommendation first, cut what the reader doesn't need, and strip out AI filler.

### Docs: Living Documents

A **Doc** is a document you and your team read and edit together, with Claude built in. What makes it different from pasting Claude's answer into a Google Doc:

- **Everyone edits the same doc at the same time.** It's live, not a copy.
- **Comments work both ways.** You and your teammates can comment, and Claude can leave its own comments while it drafts — flagging an assumption or a spot that needs your input.
- **@Claude in a comment.** Highlight a passage, leave a comment like "@Claude make this more concise," and Claude edits that part and explains what it changed. No need to re-prompt the whole doc.
- **Tabs.** One doc can hold several tabs — say, a brief, an FAQ, and meeting notes.
- **Charts and diagrams** can pull from your connectors. They update when you ask, not automatically.
- **Version history.** You can see earlier versions and go back if an edit went wrong.
- **Export.** Download as Word, PDF, or Markdown, or send it to Google Docs.

To start one, just ask: "Write this up as a Doc."

### Slides: Decks Without the Formatting Fight

A **Slides** artifact is a presentation deck. You can:

- **Build from anything** — notes, a file, a Doc, or the conversation you just had
- **Edit slides directly** or ask Claude to change them ("Split slide 3 into two," "Add speaker notes")
- **Present right from Claude**, or export to **PowerPoint**, **PDF**, or editable **Google Slides**

The same "ready" bar applies to decks. A first draft often has too many slides and too many words on each one. Cut slides, cut words, and keep only what supports the point you're making in the room.

> 💡 **On-brand by default:** Decks can use your company's design system, so colors, fonts, and layouts match the brand automatically. You'll learn how in the next lesson.

### Writing Good Requests for Docs and Decks

The same "state your goal clearly" habit from Lesson 1.01 applies here. A strong request names:
- **The audience** — "for my manager," "for the whole team," "for a pro-facing launch"
- **What they need to do** — decide, approve, get up to speed, take action
- **The length** — "one page," "5 slides max"
- **The source** — "use only my notes below," "use the Slack thread from #project-x"

> "Turn these notes into a one-page Doc for my manager, who needs to make a go/no-go decision on the pilot. Lead with the recommendation, then the three reasons, then risks. Use only what's in my notes — flag anything you had to assume."

That last line matters. Asking Claude to **flag assumptions** turns a polished-looking draft into one you can actually trust.

## Practice

Make a real doc or deck that's ready for its audience.

**Step 1: Pick something real you need to make.** A project brief, a proposal, a recap, a plan, a presentation — something with an actual audience.

**Step 2: Answer the three audience questions.** Who is it for? What do they need to do with it? How will they take it in? Based on your answers, choose a Doc or Slides (or decide a short message would be better, and pick something else to practice on).

**Step 3: Ask Claude for it.** Name the audience, what they need to do, the length, and the source. Ask Claude to flag anything it assumed.

**Step 4: Cut it down.** Read it as your audience would. Then edit it yourself: remove at least one section, paragraph, or slide they don't need, and make the ask or recommendation impossible to miss. Use an **@Claude** comment for at least one change if you made a Doc, or ask Claude in the conversation if you made a deck.

**Step 5: Check that it's ready.** Go through the five "ready" checks under **Own the Outcome**, including the time test. Fix anything that fails.

**Step 6: Find the version history.** Look at an earlier version from before your edits. Knowing you can go back makes it easier to cut boldly.

**Success criteria:** Chose a Doc or Slides based on what the audience needs, made it from real content, cut it down with your own edits, checked it against the "ready" bar, and found the version history.

## Challenge

**Get a second opinion before it goes out.** Get real feedback from someone else.

1. Share it with one teammate so they can comment (or, if no one's free, ask Claude to role-play a skeptical reader from your audience and leave three comments).
2. Ask them one specific question: **"What would you cut?"**
3. Work through each comment — fix it yourself, or ask @Claude to handle it.
4. Export the final version to wherever your team actually works — Google Docs, Google Slides, or PowerPoint — or keep it as an artifact if that's where your audience will look.

> **Before you're done — Question It:** What did Claude assume? What's missing? What could break?

**Success criteria:** Got at least two comments from a teammate or a role-played reader, resolved them, and put the final version where your audience will actually use it.
