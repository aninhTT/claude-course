---
module: 7
lesson: 3
title: "Claude Code in the Terminal"
difficulty: advanced
prerequisites: "7.02"
---

# Lesson 7.03: Claude Code in the Terminal

## Learn

Everything you've done in this course works in both the Claude Code app and the terminal. This lesson is about expanding your toolkit — understanding when and why the terminal version of Claude Code is useful, and getting comfortable with it.

### Why Some Power Users Prefer the Terminal

The terminal gives you:

- **More control.** You can specify exactly which directory Claude works in, pass flags to customize behavior, and script interactions.
- **Scripting and automation.** You can chain Claude Code into shell scripts, cron jobs, or other automation tools. Want Claude to run a skill every morning at 8am? The terminal makes that possible.
- **Speed for certain workflows.** If you're already in the terminal (navigating files, running commands, checking logs), switching to a separate app breaks your flow. Claude in the terminal keeps you in one place.
- **Integration with other tools.** The terminal lets you pipe output from one tool into Claude, or pipe Claude's output into another tool. This composability is powerful.

### How to Open Claude Code in the Terminal

If Claude Code is installed, you can launch it from any terminal by running:

```
claude
```

That's it. You'll get an interactive session just like the app, but in your terminal window. Claude has the same capabilities — it can read files, run commands, use connectors, and execute skills.

### Key Differences from the App

The capabilities are identical. The differences are in the interface:

- **Text-based interaction** rather than a graphical interface
- **No visual file browser** — you navigate with terminal commands
- **Session management** works the same way, but you start and resume sessions from the command line
- **Output is text** — no rich formatting, but the information is the same

### Terminal Tips

- **Navigate to your project folder first.** Run `cd /path/to/your/project` before launching `claude`. Claude will use that directory as its working context.
- **Use flags for customization.** `claude --help` shows available options.
- **You can pass a prompt directly.** `claude "summarize the files in this directory"` runs a one-shot command without entering an interactive session.
- **Pipe input and output.** `cat report.txt | claude "summarize this"` pipes a file's contents directly to Claude.

### When the Terminal Is Better vs When the App Is Better

**Terminal is better when:**
- You're already working in the terminal
- You want to script or automate Claude Code interactions
- You need to chain Claude with other command-line tools
- You're working on a remote server or headless environment
- You want quick one-shot commands without opening an app

**The app is better when:**
- You prefer a visual interface
- You want easy access to conversation history and session management
- You're doing long, interactive sessions with lots of back-and-forth
- You're new to Claude Code and learning the basics

Neither is "right" — they're different tools for different moments. Most power users switch between them depending on the task.

## Practice

Let's get comfortable with Claude Code in the terminal.

**Step 1: Open a terminal.** If you're not sure how, ask Claude in the app to help you open one.

**Step 2: Navigate to your course workspace.** Use `cd` to get to your project folder.

**Step 3: Launch Claude Code.** Run `claude` and start an interactive session.

**Step 4: Try a few interactions:**
- Ask Claude a question ("What files are in this directory?")
- Ask Claude to create a simple file ("Create a file called terminal-test.txt with a brief note that I completed the terminal lesson")
- Try running one of your skills from the terminal — trigger it the same way you would in the app

**Step 5: Try a one-shot command.** Exit the interactive session and run a single command, like:
```
claude "list the skills I've created in the workspace folder and summarize what each one does"
```

**Success criteria:** Successfully used Claude Code in the terminal for at least 3 interactions. You should have launched an interactive session, run at least one command, and tried a one-shot prompt.

## Challenge

Create a terminal workflow that would be harder — or impossible — to do in the app.

Some ideas:

- **A shell script that runs a skill on a schedule.** Write a script that launches Claude Code with specific context and triggers a skill. You could use `cron` or just have the script ready to run manually.
- **A pipeline that chains Claude with other tools.** For example, a command that pulls data from an API, pipes it to Claude for analysis, and saves the result to a file.
- **A project launcher.** A script that navigates to a project folder, sets up the right context, and starts a Claude Code session with a specific initial prompt.
- **A batch processor.** A script that runs Claude Code on multiple files or inputs in sequence.

Ask Claude to help you design and build the workflow. The goal is to create something that leverages the terminal's unique strengths — scripting, piping, automation — in a way the app can't easily replicate.

**Success criteria:** Created a terminal-specific workflow or script that leverages capabilities unique to the terminal (scripting, piping, automation, or chaining with other tools). Saved the script or workflow in `workspace/`.
