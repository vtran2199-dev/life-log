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

Do not assume the existing target-date file is complete or authoritative merely because it exists. It may be an early, partial, or poor reconstruction and must be checked against the day's actual conversation history.

Do not treat something as a target-date event merely because it appears in recent context.

## Reconstruct the day from cross-chat context

Cross-chat/recent-conversation retrieval is a REQUIRED part of the daily closeout, not optional context.

Use whatever cross-chat or personal-context retrieval capability is available at run time. If a dedicated retrieval tool is available, call it before drafting rather than relying only on the current conversation, the nearest few chats, memory, or the existing daily file.

Perform reconstruction in at least two passes:

### Pass 1 — broad day retrieval

Retrieve a broad recap of activity on `target_date` in `America/Chicago` across conversations, projects, and relevant connected context.

Look for the day's meaningful storylines, including where applicable:

- work completed, shipped, debugged, or materially advanced
- job search, applications, interviews, offers, or career decisions
- software/project architecture and implementation work
- important metrics, throughput, scale changes, and milestones
- decisions, reversals, discoveries, and mental-model changes
- blockers, failures, tool problems, and debugging that shaped the day
- personal interests, entertainment, games, purchases, errands, or life events that were memorable
- funny, absurd, surprising, frustrating, or emotionally salient moments
- notable direct statements by Victor about what happened "today"
- open loops created by the day

Do not limit retrieval to the current project or to the most recent few conversations if other same-day chats are available.

### Pass 2 — gap check

Before drafting, perform a second retrieval/check specifically for major things that the first pass may have missed.

Compare the candidate storylines against:

- the existing target-date file, if any
- the previous day's file
- same-day recent-conversation context
- any strong direct statements about totals, accomplishments, failures, or memorable events

Ask internally: "If Victor rereads this years later, what major part of today would he immediately notice is missing?"

If a major same-day storyline appears in conversation history but is absent from the draft plan, investigate it before writing.

The goal is not maximum length. The goal is high recall for meaningful events without inventing chronology.

## Temporal classification

For each candidate event, distinguish among:

- happened on the target date
- discussed on the target date but happened earlier
- plan or intention for a future date
- uncertain timing

Only the first category belongs as a normal event in the daily log.

Older facts may be used briefly as context when they explain why a target-date event mattered.

Direct user statements such as "today I did X" made on the target date are strong chronology evidence unless contradicted by more precise timestamps or other reliable context.

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

Do not allow technical work to crowd out the rest of the day. If meaningful personal, entertainment, gaming, social, or other non-work moments occurred, preserve them too.

## Draft completeness check

Before writing to GitHub, review the planned entry and verify:

- it reflects the actual target calendar day rather than mostly carrying forward the prior day's work
- the day's largest accomplishments or milestones are present
- major failures/blockers are present when they materially shaped the day
- important numerical totals or scale changes are included when supported
- meaningful personal or memorable moments are represented when they occurred
- the entry has enough context to be understandable years later
- it reads as Victor's day, not merely as a project changelog

If the result looks suspiciously thin compared with the amount of same-day conversation activity, do another retrieval pass before writing.

## Write the entry

Create or reconcile:

`daily/YYYY/MM/YYYY-MM-DD.md`

The normal scheduled run is an end-of-day same-date closeout. Its job is to make the target-date file reflect the best reconstruction of that calendar day through the automation run time.

If the target-date file does not exist, create it.

If the target-date file already exists, do not treat that as a conflict. Read it, then replace or revise it as needed so it becomes the complete target-date entry through the current run time. The existing file may have been created by an earlier manual run or partial same-day run and must not block the scheduled closeout.

Do not modify any file for a date earlier than `target_date` during a normal daily run.

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

- During a normal automated run, create or reconcile only the target day's file.
- Do not rewrite previous daily logs to incorporate hindsight.
- An existing target-date file is expected and may be updated to produce the complete same-day closeout.
- Higher-level reconciliation belongs in weekly/monthly/yearly summaries.

## Final response

Keep the automation chat lightweight.

After the repository write succeeds, respond with only a concise confirmation containing the target date and repository path written.
