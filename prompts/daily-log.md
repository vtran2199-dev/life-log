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

Perform all of these retrieval passes for `target_date` in `America/Chicago`. The targeted passes supplement, and do not replace, the broad retrieval pass.

### Pass 1 — broad day retrieval

Retrieve a broad recap of activity across conversations, projects, and relevant connected context. Look for the day's meaningful storylines, including where applicable:

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

### Pass 2 — career activity

Run a separate, date-specific retrieval for target-date career activity. Check for:

- completed interviews and recruiter conversations
- interview preparation and scheduled interviews
- offers, rejections, feedback, and advancement
- applications and major job-search developments

Distinguish completed events from preparation, scheduling, possibilities, and future plans.

### Pass 3 — projects and coding

Run a separate, date-specific retrieval for target-date project and coding activity. Check for:

- code written or shipped
- GitHub commits and deployments
- bugs, debugging, blockers, and technical discoveries
- major accomplishments and project decisions

Distinguish work completed or published from work discussed or planned.

### Pass 4 — personal activity

Run a separate, date-specific retrieval for target-date personal activity. Check for:

- memorable experiences and milestones
- interesting conversations and discoveries
- frustrations, entertainment, humor, and unusual events

Keep relevant personal moments even when they are not work-related.

### Pass 5 — gap check

Before drafting, perform a final retrieval/check specifically for major things that may have been missed.

Compare candidate storylines against:

- the existing target-date file, if any
- the previous day's file
- same-day recent-conversation context
- the broad and targeted retrieval results
- any strong direct statements about totals, accomplishments, failures, or memorable events

Ask internally: "If Victor rereads this years later, what major part of today would he immediately notice is missing?" If a major same-day storyline appears in conversation history but is absent from the candidate events, investigate it before writing.

The goal is high recall for meaningful events without inventing chronology. If retrieval is incomplete or unavailable, acknowledge that limitation in the completion response rather than claiming comprehensive coverage.

## Build a temporary event inventory

Before drafting, construct a temporary list of meaningful events discovered across retrieval. Do not save this inventory as a repository file or create a database or tracking system.

For each event, record:

- what happened
- when it happened, using the best available date/time evidence
- whether it was completed, merely discussed, or planned for the future
- the evidence supporting it, such as a timestamp, direct statement, or repository activity

Use this inventory to guide the entry. Resolve uncertain timing or outcomes with focused retrieval when possible; do not turn plans or possibilities into completed events.

## Temporal classification

For each candidate event, distinguish among:

- happened on the target date
- discussed on the target date but happened earlier
- plan or intention for a future date
- uncertain timing

Only events that happened on the target date belong as normal events in the daily log. Older facts may be used briefly as context when they explain why a target-date event mattered.

Direct user statements such as "today I did X" made on the target date are strong chronology evidence unless contradicted by more precise timestamps or other reliable context.

If timing is uncertain, omit the event or mark it explicitly as uncertain. Never fabricate chronology to make the narrative smoother.

## Tell the story, not the transcript

The goal is not to summarize every conversation. Reconstruct the meaningful arc of the day and synthesize chats that are parts of one evolving storyline.

Use this explicit importance order:

1. Major real-world developments: interviews, offers, rejections, significant personal milestones, and major decisions.
2. Meaningful work: coding accomplishments, projects shipped, technical breakthroughs, failures, and blockers.
3. Learning, discoveries, frustrations, and interesting experiences.
4. Funny moments, entertainment, and memorable casual conversations.

This order guides emphasis; it does not eliminate lower-priority events. Preserve personality and humor. The purpose is to prevent an extended casual conversation from overshadowing a short but significant real-world event.

Also capture meaningful scale or throughput milestones and important open loops created by the day. Preserve memorable language when useful. Do not turn the entry into a corporate status report, and do not let technical work crowd out meaningful personal, entertainment, gaming, social, or other non-work moments.

## Draft completeness check

Before writing to GitHub, compare the draft against the temporary event inventory and verify:

- every confirmed completed interview is represented
- major offers, rejections, feedback, advancement, and other career outcomes are included
- important project accomplishments, decisions, and setbacks are covered
- significant personal milestones are preserved
- no earlier-day event is incorrectly presented as a target-date event
- no scheduled, possible, or future event is falsely described as completed
- the day's largest accomplishments or milestones and supported numerical totals or scale changes are present
- meaningful personal or memorable moments are represented when they occurred
- the entry has enough context to be understandable years later and reads as Victor's day, not merely as a project changelog

If a major event's outcome is unclear, perform focused retrieval for that event rather than guessing. If the result looks suspiciously thin compared with the same-day activity, do another retrieval pass before writing.

## Write the entry

Create or reconcile:

`daily/YYYY/MM/YYYY-MM-DD.md`

The normal scheduled run is an end-of-day same-date closeout. Its job is to make the target-date file reflect the best reconstruction of that calendar day through the automation run time.

If the target-date file does not exist, create it.

If the target-date file already exists, do not treat that as a conflict. Read it, then replace or revise it as needed so it becomes the complete target-date entry through the current run time. The existing file may have been created by an earlier manual run or partial same-day run and must not block the scheduled closeout.

Do not modify any file for a date earlier than `target_date` during a normal daily run.

Use a lively but accurate narrative style. The log should be enjoyable to reread years later. Use whichever sections fit the day, such as:

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

## Verify GitHub publication

After writing, verify all of the following before reporting success:

- the correct target-date file was updated
- the GitHub write succeeded
- the updated content is present in the remote repository, by fetching or otherwise confirming the remote file after the write

Do not claim success before confirming remote publication. If publication cannot be verified, state that plainly.

## Final response

Keep the automation chat lightweight. After verified publication, respond with only a concise confirmation containing the target date, repository path written, and publication verification status. If retrieval was incomplete or unavailable, briefly acknowledge that limitation.