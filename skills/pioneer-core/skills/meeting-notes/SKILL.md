---
name: meeting-notes
description: >
  Capture and structure notes from a meeting into a clean, shareable summary.
  Use when someone says "write up my meeting notes", "summarize this meeting",
  "format my notes from [meeting name]", or pastes raw meeting notes and wants
  them cleaned up. Also trigger when someone shares a meeting transcript and
  asks what happened or what was decided.
---

# Meeting Notes

Turn raw notes, bullet points, or a transcript into a clean, structured meeting
summary that's easy to share and act on.

## What to gather

If the user hasn't provided notes yet, ask for:
- The raw notes, transcript, or bullet points from the meeting
- The meeting name and date (if not obvious)
- Any specific sections they want included or emphasized

If they've already pasted notes, start processing immediately — don't ask
for information that's already there.

## How to structure the output

Use this format:

```
## [Meeting Name] — [Date]

**Attendees:** [names if available, otherwise omit]

### Summary
2-3 sentences capturing the overall purpose and outcome of the meeting.

### Decisions Made
- [Decision 1]
- [Decision 2]

### Action Items
| Owner | Task | Due |
|-------|------|-----|
| [name] | [what they're doing] | [date or "TBD"] |

### Key Discussion Points
Brief bullets covering the main topics discussed. Focus on substance, not
play-by-play. Omit small talk and procedural filler.

### Next Meeting
[Date/time if mentioned, otherwise omit this section]
```

## Tips

- If action items don't have clear owners, flag them as "[Owner TBD]" rather
  than guessing
- If the notes are very sparse, work with what's there and note what's missing
  at the bottom (e.g., "Note: action item owners weren't captured in these notes")
- Keep the summary section genuinely brief — it should be scannable in 10 seconds
- When in doubt, include more detail in Key Discussion Points rather than less;
  the reader can skim but can't recover omitted context
