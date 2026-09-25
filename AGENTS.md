# AGENTS.md

This repository is Victor Tran's chronological personal life log.

Its purpose is to turn messy, disposable day-to-day activity into a durable historical record that can later be compressed into weekly, monthly, and yearly retrospectives.

## Canonical hierarchy

- Daily logs are the canonical historical snapshots for individual dates.
- Weekly summaries synthesize the corresponding daily logs.
- Monthly summaries synthesize weekly summaries.
- Yearly summaries synthesize monthly summaries.

Higher-level summaries may add hindsight, reconciliation, and corrected interpretation. They should not silently rewrite what an earlier daily entry actually said or knew at the time.

## Time standard

Use `America/Chicago` for calendar-day boundaries unless a prompt explicitly says otherwise.

A daily file covers exactly one local calendar date from 00:00:00 through 23:59:59 Central time.

## Paths

Create files at:

- `daily/YYYY/MM/YYYY-MM-DD.md`
- `weekly/YYYY/YYYY-Www.md`
- `monthly/YYYY/YYYY-MM.md`
- `yearly/YYYY.md`

Do not reorganize these paths casually. Treat the directory convention as stable infrastructure.

## Daily log rules

Daily entries should capture meaningful developments, not exhaustive transcripts.

Prefer:

- major work completed or shipped
- career developments
- projects materially advanced
- important decisions
- learning and discoveries
- friction, failures, blockers, and reversals
- memorable, funny, surprising, or emotionally salient moments
- useful direct quotes when available
- new open loops that matter going forward

Avoid filling the log with routine noise unless it became part of the story of the day.

## Temporal integrity

The date an event is discussed is not necessarily the date the event occurred.

When reconstructing a day from conversation history or other context:

1. Determine the target date explicitly.
2. Use timestamps, explicit dates, surrounding chronology, and direct user statements to decide whether an event actually occurred on that date.
3. Do not include an older event as a new event merely because it was discussed again.
4. Read the previous daily log when available to reduce duplicate carryover.
5. Older context may be used briefly to explain why a target-date event mattered.
6. If an event's date cannot be established confidently, omit it or mark it as uncertain rather than presenting it as fact.

## Historical integrity

Do not rewrite old daily files simply because later information changes the interpretation of an event.

Example: if Tuesday's log records an early hypothesis and Friday establishes a different cause, preserve Tuesday. The weekly summary may explain that the understanding changed during the week.

Correct factual errors in an old daily file only when there is a clear reason to do so and the edit preserves historical meaning.

## Style

The log should be enjoyable to reread.

Write clearly and concretely, but preserve personality. This is not a corporate status report.

A useful daily entry usually includes some combination of:

- `# <Month Day, Year>`
- `## The Day in One Sentence`
- `## What Happened`
- `## Wins`
- `## Friction / Lows`
- `## Things Shipped`
- `## Things Learned`
- `## Decisions`
- `## Funny / Memorable Moments`
- `## Open Loops`
- `## Quotes of the Day`

Do not force empty sections. The structure should fit the day.

## Weekly synthesis

Weekly summaries should read all available daily logs for the target week and reconcile repeated storylines.

They should identify:

- the week's main story
- major wins and setbacks
- meaningful career movement
- projects shipped or advanced
- important learning
- decisions and reversals
- memorable moments
- unresolved threads entering the next week

Do not merely concatenate seven daily files.

## Monthly and yearly synthesis

Monthly and yearly summaries should emphasize trajectory, change, recurring themes, turning points, and what became important in hindsight.

Compress aggressively while preserving the story.

## Source discipline

When creating a higher-level summary, prefer the lower-level canonical files as the source rather than relying on memory alone.

For example:

- weekly -> daily files
- monthly -> weekly files, with daily files only when detail is needed
- yearly -> monthly files, with lower levels only when detail is needed

## Automation behavior

Automated runs should be conservative. A missing event is preferable to confidently placing an event on the wrong date.

When an automated daily run creates a file, it should create only the target day's file and avoid modifying older logs unless explicitly instructed.

Prompts used by automations should live under `prompts/` so changes to logging behavior are versioned in Git.
