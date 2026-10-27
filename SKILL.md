---
name: verify-against-source
description: Trace every claim in a draft back to a source before it is called done. Use before handing over any deliverable, meeting note, status update or message, and whenever someone asks to verify, check or confirm.
---

# verify-against-source

Principle: evidence over claims. Nothing is "done", "verified", "confirmed" or "delivered" until this pass has run and its table has been shown. A claim with no source is a guess that looks like a fact.

The failure this skill exists to catch: a meeting note that lists an attendee who was never in the meeting.

## When it runs

- Before any deliverable, meeting note, register entry, status line or message is handed over as finished.
- Whenever the user asks to verify, check or confirm something.
- When someone else reports that something is done, built, fixed or sent and that report is about to be recorded as true. Record it as Reported, not Verified, unless you have seen the evidence.

## Procedure

1. **Inventory the claims.** Walk the draft and list every named person, role or title, number (money, counts, dates, times, percentages), quote or attributed statement, decision, deadline, "done" or status claim, and causal statement ("because", "so that").
2. **Locate the sources.** Allowed sources, strongest first:
   1. A raw capture: transcript, chat export or email, verbatim and timestamped.
   2. A file the user supplied.
   3. A register entry that itself cites a capture.
   4. The user's own words in the current conversation.

   If you keep a people list or a speaker key (a file that maps the names a transcript uses to real people), resolve names against it. No person may appear in the draft who is not in that list, unless the user introduced them.
3. **Build the trace table.**

   | # | Claim | Source (file, line or timestamp) | Status |
   |---|---|---|---|

   Status is one of:
   - **Verified**: seen in the source.
   - **Inferred**: follows from sources; say which ones.
   - **Reported**: someone said it; no evidence seen.
   - **Unverifiable**: no source found.
   - **Contradicted**: a source says otherwise; quote it.
4. **Fix the draft.**
   - Unverifiable or Contradicted claims that carry weight: remove them, or keep them marked `[unverified]` and tell the user.
   - Inferred claims: keep them only if the inference is stated.
   - Reported claims: word them as reported ("Sam reports the fix is live"), never as fact.
   - Never repair a gap by inventing a plausible detail.
5. **Recompute arithmetic by running it**, not by eye: totals, counts, date differences, time-zone conversions.
6. **Report**, in this order: counts per status; every Contradicted and Unverifiable item and what was done about it; what changed in the draft. A report that says "all good" with no table is not a report.

## Rules

- The pass should be a fresh read, not the author re-reading their own work. When a separate agent is available, give it the draft and the sources only, not the reasoning that produced the draft.
- Scale the table to the item. Three lines for a chat reply is still a table. Small items carry names and dates too.
- Keep sources inside their boundary. If you work for more than one client or team, never pull one side's internal material to verify a document meant for the other.
- If a source cannot be reached (offline, folder not mounted), say so and mark everything that depended on it Unverifiable. Do not downgrade to "looks consistent".

## Output

The trace table, the fix list, then the corrected draft. Keep commentary to the counts and the exceptions.
