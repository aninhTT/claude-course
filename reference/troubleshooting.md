# Troubleshooting

Common issues and how to fix them.

---

### Claude doesn't seem to know about the course

**Symptom:** Claude doesn't act like a tutor or recognize course commands.

**Fix:** Make sure you opened this exact folder in Claude Code. Claude reads the CLAUDE.md file from whatever folder you open. If you opened a different folder, the course context won't be loaded.

---

### My progress didn't save

**Symptom:** Coming back to the course and Claude doesn't remember where you were.

**Fix:** Check that `progress.json` exists in the course root. If it's missing or empty, your progress may not have been saved. Start a lesson and complete at least the Learn section — Claude will create/update progress.json.

---

### A connector isn't working

**Symptom:** Claude says it can't access Slack/Gmail/Calendar/etc.

**Fix:**
1. Check your connector settings — is it still connected?
2. Try reconnecting the connector
3. Test with a simple query: "What's on my calendar today?"
4. Some connectors may need periodic re-authentication

---

### Claude gave me an unexpected response

**Symptom:** Claude's response doesn't match what you expected.

**Fix:**
1. Be more specific in your request — add context about what you want
2. If Claude went in the wrong direction, say so: "That's not what I meant. I want..."
3. Try rephrasing your request
4. If it's a course issue, try `/lesson` to reload the current lesson

---

### I can't find a command

**Symptom:** Slash commands aren't working.

**Fix:** Make sure you're in the course folder. Commands are defined in `.claude/commands/` and only work when Claude Code is running from this folder. Available commands:
- `/course` `/lesson` `/skip` `/progress` `/hint` `/check` `/exit`

---

### I want to start over

**Symptom:** Want to reset progress and start fresh.

**Fix:** Delete `progress.json` from the course root folder. Next time you open the course, Claude will treat you as a new learner.

---

### I'm stuck on an exercise

**Symptom:** Can't figure out what to do.

**Fix:**
1. Try `/hint` for progressive hints
2. Re-read the Practice or Challenge section by running `/lesson`
3. Ask Claude directly: "I'm stuck on this exercise. Can you help me understand what I need to do?"
4. Remember: exercises are personalized. There's no single "right answer"

---

### Multiple sessions are confusing

**Symptom:** Not sure which session is which or how to switch.

**Fix:**
- In the app: check the session sidebar — each session shows its context
- Keep the course session named or identifiable
- For Cowork tasks, open them in new sessions and come back to the course session when done

---

### Claude is running slowly

**Symptom:** Responses are taking a long time.

**Fix:**
1. Long responses or complex tasks take more time — this is normal
2. If Claude seems stuck, you can interrupt and try a simpler request
3. Large context windows (lots of files open) can slow things down — this is where .claudeignore helps (Module 7)

---

### Something else is wrong

If none of the above helps:
- Ask Claude: "I'm having an issue with [describe it]. Can you help me troubleshoot?"
- Check with your team's AI resources channel
- Reach out to the course creator

Remember: using AI to ask AI is one of the course principles. Claude is often the best debugger for Claude-related issues.
