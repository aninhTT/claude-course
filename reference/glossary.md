# Glossary

### Agent
An AI that can take actions autonomously — reading files, calling tools, making decisions. Claude Code and Cowork are both agent-based.

### Approval Modes
Cowork's settings for how often it asks before acting: **Manual** (asks before actions), **Auto** (reads freely; other actions get a safety check), and **Skip** (acts without asking). Claude Code has its own modes: Manual, Accept edits, Plan, and Auto.

### Artifact
A finished piece of work — a doc, deck, design, dashboard, or short animation — that opens beside your conversation and lives at its own link. Starts private; you choose who can view, comment, or edit. (Module 4)

### Auto Memory
Notes Claude Code writes for itself about your corrections and preferences, saved per project and loaded in later sessions. On by default. See and edit them with `/memory`.

### Auto Mode
A Claude Code mode where Claude handles routine actions without asking while a safety check reviews each action in the background. The default for new sessions on many plans.

### CLAUDE.md
A special markdown file at the root of a folder that tells Claude how to behave when working in that folder. Think of it as Claude's instruction manual for your project.

### Claude Chat
The conversational interface at claude.ai. Best for thinking, brainstorming, and one-off questions. Similar to ChatGPT.

### Claude Code
The builder tool. Reads, writes, and runs files. Has plan mode. Best for creating tools, skills, templates, and prototypes.

### Claude in Chrome
A Chrome extension that lets Claude read pages, click, and fill in forms in your own browser. Use it for websites that don't have a connector. (Lesson 2.05)

### Claude Tag
Claude in Slack. Tag @Claude in a channel to hand it a task. Your organization has to turn it on; it's set up per channel. (Lesson 2.05)

### Connector
An integration that gives Claude access to an external tool (Slack, Gmail, Calendar, Jira, etc.). Also called an MCP integration. Connectors can also come bundled inside plugins.

### Context
Information Claude has access to in a given session — the folder contents, CLAUDE.md, connected tools, and conversation history.

### Context Window
The amount of information Claude can hold in "memory" during a single session. Large but not infinite. Context management helps keep it efficient.

### Cowork
The task executor. Give it clear instructions and it works autonomously. It doesn't have plan mode, but it usually makes a plan before acting and has three approval modes (Manual, Auto, Skip) that control how often it asks before taking actions. Best for well-defined tasks.

### Design System
Your brand packaged for Claude — colors, fonts, logos, and components — applied automatically to designs and decks. Thumbtack's is **Thumbprint**: just say "Use the Thumbprint design." (Lesson 4.03)

### Frontmatter
YAML metadata at the top of a markdown file, enclosed in `---`. Used in SKILL.md files and lesson files to define properties like name, description, and triggers.

### /goal
A Claude Code command (v2.1.139+) that sets a **completion condition** and keeps Claude working turn after turn — without you re-prompting — until that condition is met, then clears itself. After each turn a fast "checker" model decides whether the condition holds, judging only what Claude has surfaced in the conversation (it can't run tools or open files), so the finish line must be something the output can demonstrate. Best for large, repetitive work with a verifiable end state — audits, vendor evals, verified research; the per-turn reasons double as an audit trail.

### Granola
A meeting note-taking tool. When connected as a connector, Claude can search and reference your meeting notes.

### Hook
A custom shell command that executes in response to Claude Code events (before/after tool calls, etc.). A power user feature. (Lesson 8.07)

### MCP (Model Context Protocol)
The protocol that enables connectors/plugins. Allows Claude to interact with external tools and services.

### Memory (Project)
Files that help Claude remember context across sessions — LEARNINGS.md, context files, etc. Different from CLAUDE.md (which is instructions, not accumulated knowledge). See also Auto Memory.

### Plan Mode
A Claude Code feature that makes Claude think through an approach before building. Always use plan mode before building anything substantial. Cowork doesn't have plan mode, though it usually lays out a plan before it starts.

### Plugin
A bundle of extensions you can install in one go. A plugin can include **skills** (reusable workflows), **connectors** (integrations with tools like Slack, Gmail, Calendar), and **subagents** (specialized helpers) — and in Claude Code, power-user extras like hooks. Browse and manage them under **Customize** in the Claude app.

### Progress (progress.json)
The file that tracks your course progress — completed lessons, badges, stats, and current position.

### Rewind
Claude Code's undo. Press Esc twice (or type `/rewind`) to go back to an earlier point and restore the files, the conversation, or both.

### Scheduled Task
A task that runs automatically on a schedule. Cowork's scheduled tasks run in the cloud, so they run even when your computer is asleep (unless they need local files). (Lesson 6.02)

### Session
A single conversation with Claude Code or Cowork. Sessions persist — you can close and reopen them. You can run multiple sessions simultaneously.

### Skill
A reusable workflow defined in a SKILL.md file. Can be triggered via slash command, auto-loaded when relevant, or scheduled. Works in both Claude Code and Cowork.

### SKILL.md
The file that defines a skill. Contains YAML frontmatter (name, description, trigger) and step-by-step workflow instructions.

### Slash Command
A command starting with `/` that triggers a skill or action. Examples: `/daily`, `/course`, `/lesson`.

### Subagent
A helper Claude hands part of a task to. It works in its own fresh context and reports back a summary — useful for parallel research. (Lesson 8.04)

### Token
A unit of text that Claude processes. Roughly 3/4 of a word. The context window is measured in tokens.

### Workspace
In this course, the `workspace/` folder where you build artifacts during exercises. In general, any folder where you work with Claude Code.
