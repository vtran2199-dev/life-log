# Daily Log Prompt

Create the Life Log entry for the previous calendar day in `America/Chicago`.

## Determine the target date

At run time:

- Resolve the current local date and time in `America/Chicago`.
- Set `target_date` to the previous local calendar date.
- The target window is exactly `00:00:00` through `23:59:59` Central on `target_date`.

## Read repository instructions

Read `AGENTS.md` before doing anything else and follow it as authoritative repository guidance.

## Establish continuity

Before writing the target day:

1. Read the previous daily file if it exists.
2. Read any existing target-date file if it already exists.
3. Use those files to avoid duplicate carryover and to understand active storylines.

Do not treat something as a target-date event merely because it appears in recent context.

## Reconstruct the day

Use available cross-chat/recent conversation context and any directly relevant connected context to identify meaningful events that actually occurred on `target_date`.

For each candidate event, distinguish among:

- happened on the target date
- discussed on the target date but happened earlier
- plan or intention for a future date
- uncertain timing

Only the first category belongs as a normal event in the daily log.

Older facts may be used briefly as context when they explain why a target-date event mattered.

If timing is uncertain, omit the event or mark it explicitly as uncertain. Never fabricate chronology to make the narrative smoother.

## Write the entry

Create:

`daily/YYYY/MM/YYYY-MM-DD.md`

Use a lively but accurate narrative style. The log should be enjoyable to reread years later, not a sterile activity report.

Prioritize meaningful developments over exhaustive detail.

Use whichever sections fit the day, such as:

- The Day in One Sentence
- What Happened
- Wins
- Friction / Lows
- Things Shipped
- Things Learned
- Decisions
- Funny / Memorable Moments
- Open Loops
- Quotes of the Day

Do not force empty sections.

Preserve memorable language when it materially captures the day, but do not overload the file with transcript excerpts.

## Historical behavior

- Create only the target day's file during a normal automated run.
- Do not rewrite previous daily logs to incorporate hindsight.
- If a target-date file already exists, do not blindly replace it. Compare it with the reconstructed day and update only if the existing entry is incomplete or clearly wrong.
- Higher-level reconciliation belongs in weekly/monthly/yearly summaries.

## Final response

Keep the automation chat lightweight.

After the repository write succeeds, respond with only a concise confirmation containing the target date and repository path created or updated.
