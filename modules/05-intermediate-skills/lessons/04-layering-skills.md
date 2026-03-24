---
module: 5
lesson: 4
title: "Layering Skills"
difficulty: intermediate
prerequisites: "5.03"
---

# Lesson 5.04: Layering Skills

## Learn

As you get more comfortable with skills, there's a temptation to build one big, powerful skill that handles everything. It makes sense — why run two skills when one could do it all?

But in practice, large general-purpose skills are hard to build well, hard to debug, and hard to improve over time. The better approach is **layering**: start with small, focused skills that each do one thing perfectly, then let them work together.

### The Problem with Big Skills

Imagine you want a skill called `brand-guidelines`. The goal: make sure everything Claude produces is perfectly aligned to your company brand. Sounds great. But think about what that actually requires:

- Brand voice for written copy
- Visual standards for presentations
- Tone rules for external-facing content vs. internal content
- Layout guidance for decks
- Rules for blog posts vs. social posts vs. emails

That's not one skill. That's five different problems with different contexts, different outputs, and different failure modes. Trying to cram them all into one SKILL.md means the instructions become vague, the Gotchas section becomes unmanageable, and the skill works okay for some things but poorly for others.

### The Layering Approach

Instead of one `brand-guidelines` skill, build smaller and more specific:

| Big Skill (don't start here) | Layered Skills (start here) |
|------------------------------|------------------------------|
| `brand-guidelines` | `brand-pptx` — on-brand deck structure and visuals |
| | `brand-blog` — voice and format for external blog posts |
| | `brand-email` — tone and structure for external emails |
| | `brand-social` — short-form copy with brand voice |

Each of these is small enough to:
- **Write well** — the instructions are focused and specific
- **Test properly** — you know exactly what "working" looks like
- **Update with Gotchas** — failures are traceable to a specific context
- **Share cleanly** — a colleague knows exactly what they're getting

Once your small skills are polished, they compose naturally. Ask Claude to "write an on-brand blog post" and it will auto-detect `brand-blog`. Ask it to "build a deck for the quarterly review" and `brand-pptx` loads. They work together without needing to know about each other.

### The Right Way to Start

When you have a big, ambitious skill idea:

1. **Name the full scope** — what would the "complete" version do?
2. **Break it into use cases** — what are the distinct contexts or output types?
3. **Pick the most common one** — that's your first skill
4. **Build it small and polish it** — proper structure, tested, Gotchas filled in
5. **Then build the next one** — same process

Don't try to build all of them at once. Perfect one part of the skill, then build from there.

### When One Skill Is Fine

Layering isn't always necessary. A single skill is the right choice when:
- The workflow is genuinely unified (same inputs, same output type, same context every time)
- The scope is clear and bounded
- You've already built and tested it and it works well

The signal that you need to layer: your skill's instructions keep getting longer and more conditional. "If the output is a deck, then... but if it's a blog post, then... but if it's internal, then..." — that's three skills masquerading as one.

---

## Practice

Take a skill idea that feels broad or ambitious — either something you've been thinking about building, or one of your existing skills that's gotten unwieldy.

**Step 1:** Name the full scope of what the skill would ideally do.

**Step 2:** Break it into 2–3 smaller, more specific skills. Write out the name and one-sentence description for each.

**Step 3:** Pick the most useful one and build it fully:
- Proper YAML frontmatter (name, description, command)
- Clear numbered workflow steps
- Error handling section
- Gotchas section (even if it's empty to start — you'll fill it in as you use it)

**Step 4:** Test it on a real task. Does it work well for its specific scope?

**Success Criteria:**
- Decomposed a broad skill idea into 2–3 focused sub-skills
- Built one of them fully with all sections including a Gotchas section
- Tested it and confirmed it works for its specific use case

---

## Challenge

Build the second skill in your set and confirm the two work together without conflict.

**Step 1:** Build the second sub-skill with the same care as the first — full structure, error handling, Gotchas.

**Step 2:** Run both skills on a real task that touches both their domains. For example, if you built `brand-pptx` and `brand-blog`, try:
- Asking Claude to create a deck → confirm `brand-pptx` loads
- Asking Claude to write a blog post → confirm `brand-blog` loads
- Notice: do they conflict anywhere? Do their instructions contradict each other?

**Step 3:** If there's any overlap or conflict, refine the skill descriptions and scope so they're clearly differentiated.

**Success Criteria:**
- Second skill built fully with proper structure
- Both skills auto-detect correctly for their respective contexts
- No conflicting instructions between the two

> **Hint system:** Use `/hint` if you're stuck. First hint is a nudge, second is more specific, third nearly gives it away.
