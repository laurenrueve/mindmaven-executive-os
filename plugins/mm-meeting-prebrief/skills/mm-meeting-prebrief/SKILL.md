---
name: mm-meeting-prebrief
description: Mindmaven prebriefs, delivered the morning of each call - a skimmable brief for every call that day (external in full, internal in three lines) with the basics (name, title and company, meeting type, icebreaker, how you met, link or location, backup cell), agenda plus a silent agenda of promises to follow up on, the APPA bio from the person's page, what's owed both ways, recent threads, and a suggested goal. Delivered inside each "Call with [First Last] - YYYY-MM-DD" task, as one morning email, or both, then checked hourly so calls added, moved or changed during the day get a brief or an update. Short bullets under clear headers, no paragraphs, empty sections dropped. Part of the Mindmaven Executive OS. Use for "prep me for my call with X", "prebrief today", "brief me on today's meetings", "what do I know about X", "where do my prebriefs go", or the scheduled morning run.
---

# Meeting Prebrief (Mindmaven Executive OS)

Read `references/conventions.md` first (house rules, Preference Sheet, APPA, people pages, delivery in section 8). This skill needs: Calendar, Email, Tasks, Call tasks, People notes, Prebriefs, Delivery; Chat is optional.

**The only thing this skill writes is the brief itself**, into the `Call with` task (or wherever `Prebriefs` says). It never edits the calendar (except its own optional `Prebrief:` link events), other tasks, or people pages; the hourly check below also keeps call tasks and debrief timing in step with calendar changes. Anything that needs fixing goes under "Fix before the call" for the exec or delegate. Every fact has a receipt (a link to the page entry, email, or task it came from).

## When it runs and where briefs go

| Run | Covers | Goes to |
|---|---|---|
| Scheduled, weekdays morning of (default 7:40am, 10 minutes after the 7:30am debrief sweep that creates the `Call with` tasks) | Every call today, internal and external | Per `Prebriefs` in the Preference Sheet (conventions section 8): **task** (inside each `Call with [First Last] - YYYY-MM-DD` task: the description if it's empty, otherwise a comment), **email** (one `Prebriefs \| [Day, date]` email to the exec with all of today's briefs in time order), or **both**. Default: task. |
| **Hourly check**, weekdays, at the top of each hour from the first hour after the morning run until the last call of the day starts (Mindmaven's Pre-brief runs hourly; this keeps that) | Only what **changed** since the last run, for today's remaining calls | See "Hourly check" below. Silent when nothing changed. |
| "Prep me for my call with Maria" | The next event with Maria | Right here in chat (and into its `Call with` task if one exists) |
| "Where do my prebriefs go?" | n/a | Answer from the Preference Sheet in one line, with an example task link if one exists |

If `Call tasks: yes` and a call has no `Call with` task yet (the debrief sweep normally creates them), create it: `Call with [First Last] - YYYY-MM-DD`, due at the call time, in the Tasks project. Use the other person's first and last name; for a group, the main external person, or the meeting name if there isn't one.

## Hourly check (what changed since the last run)

Compare today's remaining calls with what the morning run and earlier checks saw (the `Call with` tasks and briefs are the record). Act only on changes; if nothing changed, do nothing and send nothing.

| Change | Do this |
|---|---|
| **New call** added since the last run | Create its `Call with [First Last] - YYYY-MM-DD` task (if `Call tasks: yes`), write the full brief into it (Steps 1-4), add the calendar link if chosen, and schedule its one-time debrief 10 minutes after it ends (if `mm-meeting-debrief` is installed; otherwise the catch-all picks it up). |
| **Moved** to a new time or day | Update the task's due time (and the date in its name if the day changed), move the `Prebrief:` link event, and reschedule the one-time debrief. Add `UPDATED [time]: moved from [old time]` at the top of the brief. |
| **Cancelled** or declined | Add `CANCELLED [time]` at the top of the brief and cancel the one-time debrief. Never delete the task; the exec or delegate completes it. |
| **Changed details** for a call in the next 24 hours: attendee added or removed, link or location changed, agenda or doc attached, a new email from an attendee | Add one `UPDATED [time]: [what changed]` line at the top of the brief, and fold the new information into the right section (a new attendee gets their own WHO lines). |

Rules: never rewrite a brief the exec or delegate has edited or commented on; add the update line instead. Problems that need the exec before the call (a new attendee with no context, a call moved into a protected block) go in the brief's FIX BEFORE THE CALL section, not a new message: the two daily touchpoints stay the only places the suite asks for attention.

## Step 1 - Pick the calls

- **Full brief:** every external call, including each session of a recurring one, interviews, kickoffs, webinars or speeches.
- **Short brief (3 lines):** internal calls.
- **No brief:** personal events, focus and Whitespace blocks, holds, events with no other attendees.
- **Meeting type** for each, from the invite and the person's page: e.g. Check-in, Kick-off, Interview, Webinar/Speech, Investor, Internal, Other. Internal = every attendee on `Company domain(s)`.
- Order in any combined report: first-time meetings, clients, investors, anything with an open commitment.

## Step 2 - Gather, per external attendee

1. **People page:** Quick glance, We Met, Title, Company, Location, LinkedIn, Cell, APPA sections, Upcoming moments, Open commitments, last 2-3 Running notes.
2. **New contact (no page):**
   - **Context from email, 1-2 lines:** how this meeting came about (who introduced them, what they asked for, what was already discussed), from the email thread that set it up. This line goes first in WHO.
   - **LinkedIn link only if you're confident it's the right person:** name **and** company (or title) match what's in the invite or email. If there's any doubt (common name, no company match), leave the link out. Never guess (house rule 2).
   - Light public research: role, company, one or two recent public items. Label it "public sources". Never research their personal life online.
3. **Tasks:** open tasks, `LL | Did...?` questions, and `Schedule |` tasks involving them, both directions. Apply house rule 5: don't list something as owed if any source shows it's done.
4. **Email** threads with them in the last 30 days; note anything unanswered on either side.
5. **Chat** (if connected): recent relevant messages.
6. **Calendar event:** agenda, attendees, link or location, attachments, who introduced them.
7. **Recorder** (if connected): summary of any earlier recorded meeting with them.

## Step 3 - Write the brief (skimmable, always)

Format rules, no exceptions:
- **Short bullets under clear headers. No paragraphs.** Each bullet fits on one line where possible (about 15 words max).
- **Drop any section that's empty.** No "None", no "N/A".
- At most 3 bullets per section, except Silent agenda and Owed (list everything).
- Bold only the one thing in each section they must not miss.
- The whole brief should read in under 60 seconds.

```
[Time] | [Meeting type] | [video link or address]
Backup: [cell]  ([who calls whom, for phone calls])

WHO
- [New contacts only: 1-2 lines on how this meeting came about, from email]
- [First Last], [Title] at [Company]  [LinkedIn link, only if confident it's them]
- Met: [how, when, who introduced] ([first meeting / met N times, last date])
- Icebreaker: [one line from interests or a recent moment]

SILENT AGENDA (for you only)
- [Promise to follow up on: "You owe the Q3 deck (due 11/14)"]
- [Moment to mention: "Ask how Lisbon was"]

AGENDA
- [From the invite]

THEM
- Working on: [Professional Challenges]
- Into: [Personal Interests & Passions]
- Family/about: [About/Facts]

LAST TIME ([date])
- [1-3 bullets, link to recording or overview]

OWED
- You owe: [task] (due [date])
- They owe: [LL question] (since [date])

RECENT THREADS
- [Subject, date, "unanswered by you" if so]

GOAL
- [One line]
- Ask: [question 1] / [question 2]

FIX BEFORE THE CALL
- [No video link / Tom not invited / no agenda]
```

**Internal calls (3 lines):**
```
[Time] | Internal | [link]
- Purpose: [from invite]
- Open between you: [tasks or LLs, or drop this line]
```

## Step 4 - Deliver

Write each brief to its destination. If `Prebriefs` includes the calendar link, also create (or update, never duplicate) the `Prebrief: [First Last]` event on the exec's own calendar right before the call, with no attendees and a link to the brief (conventions section 8). A scheduled run never asks questions: it delivers what it has and lists anything it couldn't brief, and any problem to fix before a call, in the **Before today's calls** section of the Morning touchpoint (conventions section 8).

Delegate Mode 2: the delegate's Claude writes the briefs; the delegate adds what only they know (a dietary note, a call the exec took) as a comment on the `Call with` task.

## Rules

Conventions sections 0 and 6. In meetings with several people, keep each person's details on their own lines, and never suggest raising one person's private details in front of others ("she mentioned a tough few months, be warm" is fine; specifics are not). Only suggest raising moments the person shared with the exec directly. If people pages are thin because the suite is new, say so once: "These get richer as your calls are debriefed."
