# verify-against-source

A Claude skill that traces every claim in a draft back to a source before the draft is called done.

I built it after a meeting note named an attendee who was never in the meeting. Since then nothing I hand over counts as finished until each name, number, date, decision and status claim has a source next to it.

## What it does

The skill walks the draft, lists every checkable claim and builds a trace table:

| # | Claim | Source | Status |
|---|---|---|---|
| 4 | Priya Shah attended | [10:02] "Priya sends apologies, she's out today" | Contradicted |
| 6 | 25 unmatched | 412 - 389 = 23 | Contradicted |
| 8 | Rate upload script is fixed | Sam's statement; no deploy seen | Reported |

Each claim gets one of five statuses: Verified, Inferred, Reported, Unverifiable or Contradicted. The draft is then fixed. Contradicted claims are corrected, Reported ones are worded as someone's report, and nothing is filled in by guessing.

See [examples/meeting-note.md](examples/meeting-note.md) for a full run on a made-up meeting.

## Install

Copy `SKILL.md` into a folder named `verify-against-source` in your skills directory (for Claude Code, `~/.claude/skills/`), or upload it as a skill in the Claude app. Claude loads it when you ask it to verify, check or confirm something, or before it hands over a finished piece.

## Where it helps most

- Meeting notes and minutes, where wrong attendees and wrong numbers are common
- Status reports that repeat someone else's "it's done"
- Anything built from transcripts or chat exports

## License

MIT
