# Worked example: a meeting note

Everything here is invented. Kestrel Logistics and the people in it do not exist.

## The source: transcript excerpt

```
[10:02] Dana Reyes: Thanks for joining. Priya sends apologies, she's out today.
[10:03] Leo Park: The carrier invoices for March came to 412 rows. We matched 389.
[10:05] Dana Reyes: So 23 unmatched. Can you have those cleared by Friday the 14th?
[10:05] Leo Park: I think so, if finance sends the April rates.
[10:07] Sam Ortiz: The rate upload script is fixed, by the way. Pushed it last night.
[10:09] Dana Reyes: Good. Let's move the weekly sync to Thursdays.
```

## The draft note (before the pass)

> **Attendees:** Dana Reyes, Leo Park, Sam Ortiz, Priya Shah
>
> - March carrier invoices: 412 rows, 389 matched, 25 unmatched.
> - Leo will clear the unmatched rows by Friday the 14th.
> - The rate upload script is fixed.
> - Weekly sync moves to Thursdays.

## The trace table

| # | Claim | Source | Status |
|---|---|---|---|
| 1 | Dana Reyes attended | [10:02] | Verified |
| 2 | Leo Park attended | [10:03] | Verified |
| 3 | Sam Ortiz attended | [10:07] | Verified |
| 4 | Priya Shah attended | [10:02] "Priya sends apologies, she's out today" | Contradicted |
| 5 | 412 rows, 389 matched | [10:03] | Verified |
| 6 | 25 unmatched | [10:05] Dana says 23; 412 - 389 = 23 | Contradicted |
| 7 | Leo will clear them by Friday the 14th | [10:05] "I think so, if finance sends the April rates" | Inferred (conditional) |
| 8 | Rate upload script is fixed | [10:07] Sam's statement; no test or deploy seen | Reported |
| 9 | Weekly sync moves to Thursdays | [10:09] | Verified |

Counts: 5 Verified, 1 Inferred, 1 Reported, 2 Contradicted, 0 Unverifiable.

## Fixes

- Priya moved from attendees to apologies.
- Unmatched count corrected to 23 (recomputed: 412 - 389 = 23).
- Leo's deadline carries its condition.
- The script fix is worded as Sam's report.

## The corrected note

> **Attendees:** Dana Reyes, Leo Park, Sam Ortiz. **Apologies:** Priya Shah.
>
> - March carrier invoices: 412 rows, 389 matched, 23 unmatched.
> - Leo expects to clear the unmatched rows by Friday the 14th, provided finance sends the April rates.
> - Sam reports the rate upload script is fixed (pushed the night before).
> - Weekly sync moves to Thursdays.
