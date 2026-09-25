# Weekly Log Prompt

Create the weekly Life Log summary for the most recently completed ISO week in `America/Chicago`.

Read `AGENTS.md` first and follow it as authoritative guidance.

## Source material

Read all available daily files belonging to the target ISO week from `daily/YYYY/MM/`.

Use daily files as the primary evidence. Do not rely on cross-chat memory when the canonical daily logs already cover the period, except to clarify a clear omission or ambiguity.

## Synthesis goals

Create:

`weekly/YYYY/YYYY-Www.md`

Do not concatenate the daily entries. Reconcile the week into a coherent retrospective that captures:

- the main story of the week
- major wins
- setbacks and friction
- career movement
- projects shipped or materially advanced
- important learning and discoveries
- decisions and changes of mind
- funny, surprising, or memorable moments
- unresolved threads entering the next week

Track how understanding changed during the week when useful. Preserve chronology without repeating every detail.

## Historical integrity

Do not rewrite the daily files.

If later days corrected an earlier assumption, explain the evolution in the weekly summary rather than modifying the earlier snapshot.

## Style

Write for future rereading. Be concrete, narrative, and selective. Preserve personality without turning the summary into a transcript.

## Final response

After the repository write succeeds, respond only with a concise confirmation containing the ISO week and repository path created or updated.
