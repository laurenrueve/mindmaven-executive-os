---
name: mm-meeting-debrief
description: Turn any meeting (a recording or the exec's own voice dictation) into a Mindmaven debrief in APPA format - Action items given and received, Professional Challenges, Personal Interests & Passions, About/Facts - then create tasks and yes/no loop leverage tasks in the task tool, update each attendee's running people page, and draft the follow-up email. Runs on its own: a morning sweep reads the calendar, marks each call internal or external, creates "Call with" tasks, and schedules a debrief 10 minutes after each call ends; a 5:45pm catch-all covers anything missed, including dictations. Also produces the AM Ping of meetings with no debrief. Works with any recorder, pasted transcripts, or dictation, and any major task tool. Use for "debrief my call with X", "debrief today's meetings", "here's my debrief for...", "what did I promise X", "add a note to X's page", "run my AM ping", or "set up meeting debrief". Part of the Mindmaven Executive OS.
---

# Meeting Debrief (Mindmaven Executive OS)

Mindmaven's Meeting Debrief cuts the post-meeting "follow-through tax" from about 30 minutes to about 5. This skill does the EA's processing step: it turns a meeting into APPA notes, tasks, and loop leverage, so nothing promised in a meeting is ever dropped and nothing learned about a person is ever forgotten.

Read `references/conventions.md` first: house rules (section 0), Preference Sheet (1), task rules (2), loop leverage (3), APPA and people pages (4), EA (5), guardrails (6). Where this file and conventions differ, conventions win.

## What the user can ask

| Ask | What happens |
|---|---|
| "Debrief my call with Maria" / "debrief today's meetings" | Steps 1-6 from the recording |
| A voice dictation or typed notes ("Hey, this is a meeting debrief for my meeting today with Maria at Acme...") | Steps 1-6 from the dictation |
| "Draft the follow-up to Maria" | Step 5 only, for a meeting already debriefed |
| "Run my AM Ping" (also part of the daily scans report) | The AM Ping section below |
| Scheduled: debrief sweep, per-call debrief, catch-all | The Scheduled runs section below |
| "Add a note to Maria's page: ..." | A dated note on her page (`notion-people-database.md`, "Notes outside meetings") |
| "What do I know about Maria?" | `mm-meeting-prebrief` if installed; otherwise a short brief from her page |

## Scheduled runs

Default schedules are in `conventions.md` section 7. Scheduled runs never ask questions (house rule 3).

**Debrief sweep (weekdays, early morning):**
1. Read today's calendar. Skip focus blocks, holds, personal events, and events with no other attendees.
2. **Mark each call** internal (every attendee is on `Company domain(s)`) or external (anyone else), and note never-recorded calls (matching `Never-recorded calls`).
3. **Call tasks** (if `Call tasks: yes`): make sure there's one `Call with [First Last] - YYYY-MM-DD` task per call, internal and external, due at the call time. If one already exists, don't create a second. The prebrief skill fills it in.
4. **Schedule a one-time debrief 10 minutes after each call's scheduled end** (a buffer in case it runs long). Skip never-recorded calls.
5. If one-time runs can't be created, say so in the report; the catch-all will handle today's calls.

**Per-call debrief (end of call + 10 min):** run Steps 1-6 for that call. If the recording isn't ready, try once more 30 minutes later; after that, leave it for the catch-all. What it produces depends on the call type:

| Type | Produces |
|---|---|
| External | Everything in Steps 2-4, the follow-up email per `Post-meeting` (Step 5), and the `Follow up with [First Last]` task if turned on |
| Internal | Action items and LL questions only (no people-page notes unless something personal came up, no follow-up email) |
| Never recorded | Nothing now; the catch-all creates the dictation task |

**Catch-all (weekdays, end of day):**
1. List today's calls with no debrief yet (calls added or moved after the sweep, late recordings, failed runs) and debrief them.
2. Pick up dictations: chats or emails starting "Debrief:" from today (`tool-guides.md`, "Dictating without a recorder") and debrief them.
3. For each never-recorded call with no dictation, create `Debrief from your notes - [First Last]`, due today, with the three ways to dictate in the description.

The `Follow up with [First Last]` task (if turned on) is due the next business day. Its description links the follow-up email draft, the tasks created, and the person's page, and opens with one line: "Send the draft (or edit it), then complete this task."

## Step 0 - Preference Sheet

Find the `MINDMAVEN PREFERENCE SHEET`. This skill needs: Recorder and/or Dictation, Tasks, Loop leverages, People notes, EA, Writes allowed.
- None, or "set up meeting debrief" -> `mm-setup`'s Meeting debrief module if installed, else `references/onboarding.md`.
- A needed field is missing -> ask for just that field (interactive) or use safe defaults and list it under Needs you (scheduled).
- A tool isn't connected in this chat -> say which connector to turn on (`references/tool-guides.md`) and offer to work from a pasted transcript or dictation.

## Step 1 - Get the source

**From a recording:** search the recorder for the named person or meeting, or list today's recordings. If more than one plausibly matches, list them (date, title, attendees) and ask; in a scheduled run, skip it and list it under Needs you. Pull the **full transcript**; the recorder's summary drops the small personal details, so use it only as a cross-check.

**From a dictation:** Mindmaven execs dictate in this order: header ("this is a meeting debrief for my meeting today with [Name] at [Company]", names spelled out), Action items given and received, Professional Challenges, Personal Interests & Passions, About/Facts, then optional extra context ("remind me to check in in 60 days", "turn this into a follow-up email"). Follow their order, but capture anything said out of order too. If the dictation says "no debrief needed", record that and stop. If a recording of the same meeting exists, use it to fill gaps, and say what came from where.

Identify who is who: which speaker is the exec, and each attendee's name, company, and role if stated. Check the header and the last part of a dictation for priority ("urgent", "today").

## Step 2 - Extract in APPA

Follow `references/extraction-rules.md`. Summary:

- **Action items given** (the exec promised) -> a task for whoever does it + an LL question to confirm it happened. Logistics go to the EA; judgment and voice stay with the exec. Tag exec tasks under 5 minutes `< 5 min`. Scheduling requests -> `Schedule | [Name]`.
- **Action items received** (promised to the exec) -> an LL question: `LL | Did Maria send the signed MSA?`
- **Professional Challenges**, **Personal Interests & Passions**, **About/Facts** -> the attendee's people page, dated, each with its receipt (timestamp or dictation line).
- **Moments** (trips, moves, a kid starting college...) -> a touch task for the exec on the date from conventions section 3, plus its LL question.
- **We Met**: if this was the first meeting, record how and when they met.

Then a **second pass**: re-read top to bottom looking only for what the first pass missed: throwaway promises ("I'll send you that article"), a name or age mentioned once, any future date for anything personal, promises the other person made that read like small talk, and speaker mistakes.

## Step 3 - Review

Interactive runs: show this, then ask "Anything to change, remove, or reassign before I send these over?" Scheduled runs: create first, then report. Create everything `Writes allowed` permits right away (during the first 2 weeks, in the `Suggested` section per `Scan mode`), then put anything that needs the exec in the Debriefs section of the End of day review. Only what `Writes allowed` forbids becomes a suggestion in the report instead.

```
MEETING DEBRIEF | [Name] ([Company]) - [meeting title], [date]

ACTION ITEMS
Given (you promised)
  1. [Verb + task]  |  [owner]  |  due [date or none]  |  [< 5 min?]  |  "[quote]" ([timestamp])
     + LL | Did [Exec] [do it]?  |  due [date]  |  EA
Received (promised to you)
  2. LL | Did [Name] [send thing]?  |  due [date]  |  EA
Scheduling
  3. Schedule | [Name]  |  [what and when]

LOOP LEVERAGE: MOMENTS
  L1. [Touch task]  |  you  |  due [date]  ([why that date])
      Draft: "[one or two lines]"
      + LL | Did [Exec] [touch]?  |  due [date + 1 business day]  |  EA

PROFESSIONAL CHALLENGES
  - [Name]: [fact] ([receipt])
PERSONAL INTERESTS & PASSIONS
  - [Name]: [fact] ([receipt])
ABOUT/FACTS
  - [Name]: [fact] ([receipt])

FOLLOW-UP EMAIL: [offer to draft / requested in dictation / not needed]
NOTHING FOUND: [empty categories, so the user knows you looked]
NEEDS YOU: [anything uncertain]
```

## Step 4 - Write to their tools

Only where Writes allowed permits.
- **Tasks and LL tasks** -> per conventions sections 2 and 3: yes/no LL names, owners by EA mode, staggered due dates, receipts and `Source: meeting debrief` in each description. Check for duplicates first.
- **People pages** -> per `references/notion-people-database.md`: new Running notes entry at the top in APPA format, refresh Quick glance, add Upcoming moments (linked to their LL tasks) and Open commitments both ways, update Last met and Next touch, move anything no longer true to the No longer true list. In a CRM, one dated APPA timeline note.
- **Debrief record** -> if the exec's EA works from email, also draft (never send) an email to the exec, subject `Meeting Debrief | [Name]`, with the APPA headers and dashes rather than bullets. Only if the Preference Sheet asks for it.

## Step 5 - Follow-up email (eDraft)

If `mm-edraft` is installed, hand the follow-up to it (type: follow-up after a meeting) so drafts share one voice and the 48-hour unsent check. Otherwise follow the rules below.

When to draft: per `Post-meeting` in the Preference Sheet (default: always for external calls, never for internal), or whenever the dictation or the user asks. In "ask" mode, interactive runs offer it; scheduled runs list it under Needs you. Draft (never send) the follow-up email in Mindmaven's 7-part structure:
1. Subject line: clear and specific to this meeting
2. Greeting
3. Positive impact: something specific from the meeting
4. Common ground
5. Key takeaways and next steps (both sides' commitments)
6. Future-pacing: what happens next and when
7. Sign-off in the exec's own style (copy it from a recent sent email)

Use relative time references ("as we discussed Tuesday"), and for introductions the subject `Introduction [Name] <> [Name]`. Mark anything inaudible as `_____` and any guess as `??guess??`, and tell the user. Never send in the exec's name; the exec presses send. If the Preference Sheet says the EA is BCC'd on sends, leave a note to BCC them.

## Step 6 - Report

A few lines: counts per category, links to what was created, what was skipped and why, the draft's location, and anything under Needs you.

## AM Ping (8am, or "run my AM Ping")

Mindmaven's AM Ping holds the exec accountable for debriefs without nagging.
1. List yesterday's calendar events that are "debrief-able": external meetings, plus anything the Preference Sheet adds. Skip internal meetings, personal events, and focus blocks.
2. For each, check whether a debrief exists: a dictation was received, this skill debriefed it, or the exec said "no debrief needed".
3. Include the missing ones in the morning scan report (or send per Delivery when run alone), **names only**: "Missing debriefs from yesterday: Maria G., Tom R. Dictate one by saying 'Debrief:' in the Claude app, or reply 'no debrief needed'." Nothing missing: leave the line out.
4. If a recording exists for a missing one, offer: "I can debrief these from the recordings now."

In Mode 2, the EA's Claude runs the AM Ping and the EA follows up.

## Rules

Conventions sections 0 and 6. The people pages and LL tasks you create are what `mm-meeting-prebrief` and `mm-calendar-review` read later, so keep names, companies, and dates clean and consistent.
