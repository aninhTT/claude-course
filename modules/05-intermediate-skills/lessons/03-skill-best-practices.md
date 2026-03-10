---
module: 5
lesson: 3
title: "Skill Best Practices & Patterns"
difficulty: intermediate
prerequisites: "5.02"
---

# Lesson 5.03: Skill Best Practices & Patterns

## Learn

You've been building skills all module. Now let's step back and look at what separates skills that get used every day from skills that get abandoned after a week.

### Naming Conventions

Names matter more than you think. A well-named skill is one you can find and remember.

**Do:**
- Use verb-noun format: `draft-update`, `scan-inbox`, `prep-meeting`
- Be specific: `summarize-weekly-metrics` over `summarize-stuff`
- Keep it short: aim for 2-3 words
- Use lowercase with hyphens consistently

**Don't:**
- Use vague names: `helper`, `do-things`, `my-skill`
- Use abbreviations only you understand: `wk-mtrc-smry`
- Mix naming styles: `draftUpdate` alongside `scan-inbox`

### Writing Clear Instructions

The instructions in your SKILL.md are the most important part. Claude follows them literally, so clarity is everything.

**Be specific, not vague:**
- Vague: "Look at recent messages"
- Specific: "Search the #team-updates Slack channel for messages from the past 7 days"

**One action per step:**
- Overloaded: "Search Slack, check email, scan Jira, and look at the calendar"
- Clear: Four separate numbered steps, one per source

**Define "done":**
- Unclear: "Write a summary"
- Clear: "Write a summary with 3 sections: Highlights (top 3 items), Details (grouped by person), and Action Items (bulleted list)"

**Specify the format:**
- Ambiguous: "Present the results"
- Explicit: "Format as a Slack message using bullet points, with bold headers for each section"

### The "Start Simple, Iterate" Principle

This is the single most important pattern for skill building:

1. **Version 1:** The bare minimum that works. 3-4 steps, basic output.
2. **Test it.** Does it produce something useful?
3. **Version 2:** Add error handling and edge cases you discovered.
4. **Test again.** Try it in different situations.
5. **Version 3:** Polish the output format, add inputs for flexibility.

Most people try to build the perfect skill on the first attempt. This leads to over-engineered skills that are hard to debug and hard to improve. Start simple. Get it working. Then make it better.

### Versioning Your Skills

When you improve a skill, keep the old version around — at least temporarily.

**Simple approach:** Add a version comment at the top of your SKILL.md:
```markdown
<!-- v3 - 2025-03-08 - Added error handling for missing Slack channels -->
```

**More structured approach:** Keep a changelog section:
```markdown
## Changelog
- v3 (2025-03-08): Added error handling for missing Slack channels
- v2 (2025-03-01): Added Jira integration
- v1 (2025-02-20): Initial version with Slack-only summary
```

This helps when something breaks — you can see what changed and roll back if needed.

### Sharing Skills with Teammates

One of the best things about skills is that they're just markdown files. Sharing them is as easy as sharing a file.

**To make a skill shareable:**

1. **Remove personal assumptions.** Replace "my #team-updates channel" with a configurable input or clear instruction.
2. **Add context.** Someone who didn't build the skill needs to understand what it does and why.
3. **Include setup instructions.** What does the user need to have configured? What tools or access are required?
4. **Test with fresh eyes.** Can someone who's never seen this skill understand and use it?

**Sharing methods:**
- Drop the skill folder in a shared directory or GitHub repo
- Include a README.md alongside the SKILL.md
- Share the skill catalog document you built in Lesson 5.01

### Learn From What Breaks

Here's a best practice most people miss: **when Claude runs into issues with your skill, ask it what it learned.**

After a skill hits a snag — wrong output format, couldn't find the data, missed an edge case — don't just fix the problem and move on. Ask Claude:

> "What went wrong? What did you learn about this issue? How should we update the skill to handle this in the future?"

Claude will often give you a specific, actionable insight: "The Slack channel was archived so the search returned nothing — the skill should check for archived channels and fall back to the general channel." That's not just a fix for today — it's an improvement you can **codify directly into the skill's instructions.**

This creates a virtuous cycle:
1. **Run the skill** → something unexpected happens
2. **Ask Claude what it learned** → get a clear diagnosis
3. **Update the skill instructions** → bake that learning in permanently
4. **Next run is better** → repeat

Over time, your skills get smarter because they accumulate real-world lessons. The skills that get used every day aren't the ones that were perfect on day one — they're the ones that learned from every failure.

### Common Pitfalls

**Over-engineering:** Your skill doesn't need to handle every edge case on day one. Build for the 80% case first.

**Not testing enough:** "I wrote it, it probably works" is the motto of every broken skill. Test after every change.

**Unclear output specs:** "Write something useful" is not a useful instruction. Define what the output should look like.

**Overloading a single skill:** Your skills can absolutely be complex and multi-step — that's one of their strengths. The pitfall is trying to do too many *different* things in one skill. A 12-step skill that generates a weekly digest? Great. A skill that generates a digest AND updates a spreadsheet AND sends three different Slack messages to different channels? That's three skills pretending to be one. Keep each skill focused on one clear purpose, even if that purpose requires many steps. Clear instructions and good context are what make complex skills work — not cramming everything into a single file.

**Ignoring failure modes:** Happy path skills break in the real world. Add error handling before you automate.

**Copying without understanding:** Borrowing patterns from other skills is great. Copying a whole skill and changing three words is a recipe for confusion.

---

## Practice

Time to audit and improve your existing skills.

**Step 1:** Open your skill catalog from Lesson 5.01 (or list your skills if you didn't create one).

**Step 2:** Pick your **weakest** skill — the one that feels roughest, least reliable, or hardest to use.

**Step 3:** Apply at least 3 best practices from this lesson to improve it. For each improvement:
- Note what you changed
- Note which best practice it addresses
- Test the skill after the change

**Ideas for improvements:**
- Rename it to follow verb-noun convention
- Rewrite vague instructions to be specific
- Add a version comment or changelog
- Split overloaded steps into single-action steps
- Add or improve error handling
- Define the output format explicitly
- Add inputs for flexibility

**Step 4:** Save your improvement notes at `workspace/skill-audit.md` so you can reference them later.

**Success Criteria:**
- Identified the weakest skill with clear reasoning
- Applied at least 3 specific best practices from this lesson
- Documented each improvement and the practice it addresses
- Tested the improved skill

---

## Challenge

Package one of your best skills so that a colleague could pick it up and use it without any guidance from you.

**Step 1:** Choose your most polished, most useful skill.

**Step 2:** Create a `README.md` alongside its `SKILL.md` that includes:
- What the skill does (one paragraph)
- Prerequisites (what tools, access, or setup is needed)
- How to use it (slash command and natural language triggers)
- What output to expect
- Known limitations or edge cases
- Example usage

**Step 3:** Review the SKILL.md itself through the lens of someone who has zero context about your work:
- Are there references to "my" channels, "our" team, or other assumptions?
- Would the steps make sense to someone outside your team?
- Is the error handling sufficient for someone who can't troubleshoot?

**Step 4:** Organize the skill folder cleanly:
```
workspace/skills/your-skill-name/
  SKILL.md
  README.md
```

**Success Criteria:**
- README.md covers purpose, prerequisites, usage, output, limitations, and example
- SKILL.md is free of personal assumptions (or clearly marks them as configurable)
- The skill folder is organized and self-contained
- A colleague could use this skill based solely on the documentation

> **Hint system:** Use `/hint` if you're stuck. First hint is a nudge, second is more specific, third nearly gives it away.
