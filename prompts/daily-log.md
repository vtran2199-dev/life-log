# Daily Log Prompt

Create the Life Log entry for the current calendar day in `America/Chicago`, covering that day only through the time the automation runs.

## Determine the target date

At run time:

- Resolve the current local date and time in `America/Chicago`.
- Set `target_date` to the current local calendar date.
- The target window begins at `00:00:00` Central on `target_date` and ends at the automation run time.
- Do not move events across midnight merely to make a work session read more smoothly.
- If a work session clearly began on the prior calendar date and continued after midnight, older events may be referenced briefly for continuity, but only target-date events should be presented as things that happened on `target_date`.

## Read repository instructions

Read `AGENTS.md` before writing and follow it as authoritative repository guidance.

## Establish continuity

Before writing the target day:

1. Read the previous daily file if it exists.
2. Read any existing target-date file if it already exists.
3. Use those files to avoid duplicate carryover and to understand active storylines.

Do not treat something as a target-date event merely because it appears in recent context.

## Reconstruct the day

Use available cross-chat/recent conversation context and any directly relevant connected context to identify meaningful events that actually occurred on `target_date`.

The prompt intentionally refers to cross-chat context generically rather than naming a specific internal retrieval tool. Use whatever context-retrieval capability is available at run time.

For each candidate event, distinguish among:

- happened on the target date
- discussed on the target date but happened earlier
- plan or intention for a future date
- uncertain timing

Only the first category belongs as a normal event in the daily log.

Older facts may be used briefly as context when they explain why a target-date event mattered.

If timing is uncertain, omit the event or mark it explicitly as uncertain. Never fabricate chronology to make the narrative smoother.

## Tell the story, not the transcript

The goal is not to summarize every conversation. Reconstruct the meaningful arc of the day.

Prioritize:

- major work completed or shipped
- career developments
- projects materially advanced
- important decisions and reversals
- discoveries or mental-model changes
- friction, failures, blockers, and debugging that materially shaped the day
- meaningful scale or throughput milestones
- funny, absurd, surprising, or emotionally salient moments
- important open loops created by the day

When several chats are parts of one evolving storyline, synthesize them into that storyline rather than giving each chat equal weight.

Preserve personality and memorable language when it helps future rereading. Do not turn the entry into a corporate status report.

## Write the entry

Create:

`daily/YYYY/MM/YYYY-MM-DD.md`

Use a lively but accurate narrative style. The log should be enjoyable to reread years later.

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

## Historical behavior

- During a normal automated run, create only the target day's file.
- Do not rewrite previous daily logs to incorporate hindsight.
- If the target-date file already exists, do not blindly overwrite it or create a duplicate. Inspect it and report the conflict unless the current run was explicitly instructed to revise that existing entry.
- Higher-level reconciliation belongs in weekly/monthly/yearly summaries.

## Final response

Keep the automation chat lightweight.

After the repository write succeeds, respond with only a concise confirmation containing the target date and repository path created.
