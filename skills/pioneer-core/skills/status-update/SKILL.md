---
name: status-update
description: >
  Draft a concise project status update for stakeholders or leadership.
  Use when someone asks to "write a status update", "send a project update",
  "draft an update for [person/team]", or needs to communicate project health
  (on track, at risk, blocked). Also trigger for sprint updates, milestone
  check-ins, or any time someone needs to communicate progress on a project.
---

# Status Update

Write a clear, professional project status update that gives stakeholders
the right information without burying them in detail.

## What to gather

Ask the user for:
- Project name
- Current status: **On Track**, **At Risk**, or **Blocked**
- Key accomplishments since the last update
- What's coming up next
- Any blockers or risks (if At Risk or Blocked)
- Who this is going to (informs tone and detail level)

If they give you notes or bullet points to work from, use those directly.

## Output format

```
**[Project Name] — Status Update**
*[Date]*

**Status:** 🟢 On Track  /  🟡 At Risk  /  🔴 Blocked

**Summary**
One or two sentences on overall project health and the most important
thing to know right now.

**Since Last Update**
- [Accomplishment or milestone reached]
- [Accomplishment]

**Next Up**
- [What's happening in the next week/sprint/phase]
- [Key upcoming milestone]

**Blockers / Risks**
- [Blocker and who owns resolving it — omit this section if status is On Track and there are none]

**Asks (if any)**
- [Specific request from stakeholders, e.g. a decision needed, a resource request]
```

## Tips

- The status emoji (🟢/🟡/🔴) should be honest — stakeholders rely on it
  to know whether to dig in; avoid defaulting to green when things are rocky
- "At Risk" means you're still on track but something could derail you
- "Blocked" means work has stopped and outside action is needed
- Keep "Since Last Update" to 3-5 bullets max; this isn't a changelog
- Only include "Asks" if there's a genuine request — don't pad it
- Adjust formality based on the recipient; a Slack message to your team
  can be much looser than an email to an exec
