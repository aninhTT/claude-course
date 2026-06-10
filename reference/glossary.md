# Glossary

### Agent
An AI that can take actions autonomously — reading files, calling tools, making decisions. Claude Code and Cowork are both agent-based.

### CLAUDE.md
A special markdown file at the root of a folder that tells Claude how to behave when working in that folder. Think of it as Claude's instruction manual for your project.

### Claude Chat
The conversational interface at claude.ai. Best for thinking, brainstorming, and one-off questions. Similar to ChatGPT.

### Claude Code
The builder tool. Reads, writes, and runs files. Has plan mode. Best for creating tools, skills, templates, and prototypes.

### Connector
An integration that gives Claude access to an external tool (Slack, Gmail, Calendar, Jira, etc.). Also called a plugin or MCP integration.

### Context
Information Claude has access to in a given session — the folder contents, CLAUDE.md, connected tools, and conversation history.

### Context Window
The amount of information Claude can hold in "memory" during a single session. Large but not infinite. Context management helps keep it efficient.

### Cowork
The task executor. Give it clear instructions and it works autonomously. Does NOT have plan mode. Best for well-defined tasks.

### Frontmatter
YAML metadata at the top of a markdown file, enclosed in `---`. Used in SKILL.md files and lesson files to define properties like name, description, and triggers.

### /goal
A Claude Code command (v2.1.139+) that sets a **completion condition** and keeps Claude working turn after turn — without you re-prompting — until that condition is met, then clears itself. After each turn a fast "checker" model decides whether the condition holds, judging only what Claude has surfaced in the conversation (it can't run tools or open files), so the finish line must be something the output can demonstrate. Best for large, repetitive work with a verifiable end state — audits, vendor evals, verified research; the per-turn reasons double as an audit trail.

### Granola
A meeting note-taking tool. When connected as a connector, Claude can search and reference your meeting notes.

### Hook
A custom shell command that executes in response to Claude Code events (before/after tool calls, etc.). A power user feature.

### MCP (Model Context Protocol)
The protocol that enables connectors/plugins. Allows Claude to interact with external tools and services.

### Memory (Project)
Files that help Claude remember context across sessions — LEARNINGS.md, context files, etc. Different from CLAUDE.md (which is instructions, not accumulated knowledge).

### Plan Mode
A Claude Code feature that makes Claude think through an approach before building. Always use plan mode before building anything substantial. Cowork does NOT have plan mode.

### Plugin
An umbrella term for anything that extends Claude's capabilities. Plugins include **skills** (reusable workflows), **commands** (slash-triggered actions), and **connectors** (integrations with external tools like Slack, Gmail, Calendar). Think of "plugin" as the category, with skills, commands, and connectors as the types within it.

### Progress (progress.json)
The file that tracks your course progress — completed lessons, badges, stats, and current position.

### Session
A single conversation with Claude Code or Cowork. Sessions persist — you can close and reopen them. You can run multiple sessions simultaneously.

### Skill
A reusable workflow defined in a SKILL.md file. Can be triggered via slash command, auto-loaded when relevant, or scheduled. Works in both Claude Code and Cowork.

### SKILL.md
The file that defines a skill. Contains YAML frontmatter (name, description, trigger) and step-by-step workflow instructions.

### Slash Command
A command starting with `/` that triggers a skill or action. Examples: `/daily`, `/course`, `/lesson`.

### Token
A unit of text that Claude processes. Roughly 3/4 of a word. The context window is measured in tokens.

### Workspace
In this course, the `workspace/` folder where you build artifacts during exercises. In general, any folder where you work with Claude Code.
