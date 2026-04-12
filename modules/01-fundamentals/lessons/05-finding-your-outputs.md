---
module: 1
lesson: 5
title: "Finding Your Outputs"
difficulty: beginner
prerequisites: "1.04"
videos:
  - url: "https://www.loom.com/share/e23de5c1e5f84dfda7b98ca4346685b3"
    title: "Understanding Folders & Changing Your Output Location"
    duration: "~2.5 min"
    context: "Watch this to see how to check and change which folder Claude works in"
---

# Lesson 1.05: Finding Your Outputs

## Learn

Here's something important to understand early: **where your outputs end up depends on which tool you're using.**

> Already comfortable with this topic? Skip ahead anytime with `skip` followed by the next lesson number.

When you use **Chat** (claude.ai), everything stays in the conversation. Claude might generate a great summary, a table, or a draft — but it lives in that chat window. If you want it somewhere else, you have to copy and paste it yourself.

When you use **Claude Code or Cowork**, it's completely different. These tools **run locally** — meaning they work directly with your computer's file system. When Claude creates a file, it's a real file sitting in a real folder on your machine. You can open it in any app, email it, move it around — it's yours.

This is what "running locally" means: Claude Code and Cowork aren't just chatting with you. They're reading, creating, and organizing actual files on your computer, just like you would in Finder or File Explorer.

### You Need a Place for Your Outputs

Since Claude Code and Cowork create real files, you need a place to put them. Right now, you're working inside the course folder — but when you start using Claude for your own work, you'll want a dedicated spot.

We're going to set that up right now: a personal **"Claude Folder"** where your Claude-generated outputs will live.

### Changing Where Claude Builds

There are two ways to control where Claude puts things:

1. **Tell Claude where to build.** You can say "find my Claude Folder and create the file there" — Claude will locate it and work in that directory.
2. **Manually change the folder setting.** In Cowork, click the folder path at the top of the window to change it. In the Claude Code app, use the folder selector. This points Claude at a different directory before you start working.

Want to see this in action? Here's a quick demo that walks through checking and changing your folder: https://www.loom.com/share/e23de5c1e5f84dfda7b98ca4346685b3

Both approaches work — use whichever feels more natural. The key thing is **knowing where Claude is putting files** so you can find them.

## Practice

Let's put this into action. You're going to create your own output folder, have Claude build something in it, and then go find it on your computer.

**Step 1:** Create a new folder somewhere on your computer. Call it "Claude Folder" (or whatever you'd like). Put it somewhere easy to find — your Desktop, Documents folder, or wherever makes sense for you. Do this manually in Finder (Mac) or File Explorer (Windows).

**Step 2:** Now point Claude at that folder. You have two options:
- **Option A:** Tell Claude in this session: "Find my Claude Folder on my computer and build there." Claude will locate it.
- **Option B:** Manually change your folder setting in Code or Cowork to point to your new folder. (The video above shows how.)

**Step 3:** Ask Claude to create a spreadsheet with sample data in it. Don't overthink this — let Claude pick the topic and fill it with fake data. The point isn't the content, it's the experience of Claude creating a real file in your folder.

**Step 4:** Now the important part — **go find it.** Open Finder or File Explorer, navigate to your Claude Folder, and confirm the spreadsheet is there. Open it up and take a look.

**Step 5:** Come back here and tell Claude: "I found it!" That's it — that's the exercise.

**Success criteria:** Created a personal Claude Folder, had Claude build a spreadsheet with sample data in it, and physically located the file on your computer.

## Challenge

Here's a stretch goal: **tell Claude to move that spreadsheet from your Claude Folder to your Desktop.**

Don't move it yourself — ask Claude to do it. Then go check your Desktop and confirm it's there.

This might seem small, but think about what just happened: you told Claude to reorganize your actual files, and it did. Claude Code doesn't just create things — it can move, rename, and organize files across your computer. That's the power of running locally. It's not answering questions in a chat bubble — it's working with your real file system.

> **Before you're done — Question It:** What did Claude assume? What's missing? What could break?

**Success criteria:** The spreadsheet was moved to your Desktop by Claude (not manually), and you physically confirmed it's there.
