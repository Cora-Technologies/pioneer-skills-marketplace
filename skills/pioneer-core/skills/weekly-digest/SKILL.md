---
name: weekly-digest
description: >
  Compile a weekly digest summarizing what happened across Pioneer's work —
  progress made, decisions, blockers, and what's coming up. Use when someone
  asks for a "weekly digest", "week in review", "what happened this week",
  "weekly summary", or "weekly wrap-up". Also trigger when someone wants to
  catch up after being out or wants a summary to send to their team.
---

# Weekly Digest

Produce a concise, readable summary of the week's activity — useful for
staying in sync, sending to stakeholders, or personal reflection.

## What to gather

Ask the user:
- What time period to cover (default: the current week)
- What sources to pull from — e.g., did they share notes, emails, Slack
  messages, completed tasks, or project updates?
- Who the digest is for: just themselves, their team, or leadership?
  (This affects tone and level of detail)

If they've already shared raw material, start synthesizing it.

## Output format

Adjust length and tone based on the audience:

- **Personal / team**: conversational, bullet-heavy, can include open questions
- **Leadership / stakeholders**: tighter, outcome-focused, fewer details

```
## Week of [Date Range]

### Highlights
The 2-3 most significant things that happened this week.

### Progress by Project
**[Project Name]**
- [What moved forward]
- [What's still in progress]

**[Project Name]**
- ...

### Decisions & Outcomes
- [Decision or resolved question]

### Blockers & Open Questions
- [Anything stuck or unresolved]

### Coming Up Next Week
- [Key priorities or events]
```

## Tips

- Lead with what matters most, not chronological order
- If a project had no meaningful movement this week, a one-liner is fine
  ("No updates this week — picking back up Monday")
- For leadership digests, cut the "Coming Up" section to 2-3 bullets max
  and omit minor blockers that are being handled
- Keep the whole thing readable in under 2 minutes
