# Onboarding (about 35 minutes)

Design goals: clear, real, and no surprises.
- **Clear:** the exec hears what each skill is for, answers a few direct questions (recorder, task tool, people notes), and sees each part of a real output explained.
- **Fast where it can be:** for everything else, read before you ask. Infer from the calendar, email, and task tool, then show the exec what you found and let them correct it.
- **Real:** every step uses the exec's own meetings, inbox, and people.
- **No surprises:** finish with exactly what they'll get, when, and where.

Rules: one question at a time; offer the likely answer as a default they can accept with "yes"; save the Preference Sheet after each part so they can stop and say "continue my setup" later.

## Part 1: Welcome and what each skill is for (3 minutes)

Explain what each skill is for, one line each. List only the skills this exec installed (check which `mm-*` skills are available), in this order:

> Here's what each skill does for you:
> - **Setup** (this one): connects your tools and saves your preferences.
> - **Meeting prebrief:** a skimmable brief for each call, ready the morning of.
> - **Meeting debrief:** after each call, your action items, follow-ups, what you learned about the person, and a follow-up email draft.
> - **Email loop scan:** what you're waiting on (like "did they sign the contract we sent?") and personal moments worth a touch.
> - **Missed-task scan:** anything you promised in email or Slack and never wrote down.
> - **Loop manager:** checks which open loops closed and drafts nudges for the rest.
> - **eDraft:** say "Edraft:" and a few sentences, and a send-ready email appears in your drafts.
> - **Calendar upkeep:** tomorrow's calendar checked every afternoon, confirmations drafted.
> - **End-of-day update:** a short summary with only the decisions that need you.
> - **Calendar review:** every Friday, next week checked and fixed, plus trips and big events 2-3 weeks out.
>
> You'll hear from it **twice a day**: once in the morning and once at the end of the day. Setup takes about 35 minutes, and by the end you'll know exactly what you get tomorrow, where, and what to do with it.

## Part 2: Connect and confirm (10 minutes)

1. **Ask two questions first**, one at a time. If you can already see their calendar or tasks, offer what you see as the default.
   - **Recorder:** "What do you record your meetings in? **Granola, Fathom, Quill, or other (please enter).**" If you see recorder links or bots on the calendar, add: "I see [Fathom] links on your calendar. Is that right?" If they don't record, say dictation is covered in Part 3.
   - **Task tool:** "Where do you want your action items to go? **Asana, Notion, ClickUp, Trello, Microsoft To Do, or other (please enter).**"
2. **Connect, in one go.** Check which connectors are already on. For the missing ones among calendar, email, the task tool they named, the recorder they named, and chat, give the steps from `tool-guides.md` all at once ("Turn these on, then say done"). Guide them through connecting the recorder step by step. Test each with real data and show one line per tool ("Calendar: I can see your 6 meetings tomorrow").
3. **Read, then propose.** Look at the last 4 weeks of calendar and the task tool and propose the Preference Sheet as one short list:
   - Working hours, earliest start, latest end (from the actual first and last meetings)
   - Days they take external meetings (from patterns)
   - Typical buffers and longest back-to-back stretch
   - Lunch and protected blocks (recurring holds)
   - Invite naming and colors they already use
   - Project and naming they already use in their task tool (e.g. existing `Call with` tasks)
   Then ask: **"Here's what I see. What should change?"** Fix only what they correct.
4. **Ask only what you can't infer**, one at a time, each with a suggested default:
   - "What's the most meeting time you want in a day, and how long can you go before you need a break?"
   - "How much Whitespace do you want protected each week?" (Mindmaven minimum: 4-6 hours.)
   - Travel (only if the calendar shows travel): home airport, nonstop, red-eyes, buffer after landing, ground transport.
   - "Any calls you never record?" (sets the no-record rule)

## Part 3: Choose how it works (7 minutes)

1. **Your delegate.** Explain all three modes using the table in `ea-playbook.md` (one line each, plus the Maria/Jordan example), **then** ask: "Do you have an EA, chief of staff, or colleague who helps with follow-through, and which mode fits?" Anyone who helps can be the delegate. Recommend Mode 1 to start.
2. **Where things land.** Offer, with the default first:
   - **People notes:** "For notes on the people you meet: **do you already have a CRM, or do you want me to build a People database in Notion?**" CRM: ask which one and connect it (`tool-guides.md`, people destinations). Notion: build it now from `notion-people-database.md`, **in their Private section** (never a shared teamspace), and share the link.
   - **Call tasks:** "Want a `Call with [First Last] - YYYY-MM-DD` task for every call, internal and external, and a `Follow up with [First Last]` task after?" (Recommended.)
   - **Prebriefs:** "Where do you want your prebriefs each morning?"
     - **In each call task** (recommended): the brief sits inside that call's `Call with` task.
     - **One morning email** to you with all of today's briefs in time order.
     - **Both.**
   - **Follow-up emails:** "After external calls, should I draft the follow-up email for you to send? Always, ask each time, or never?"
   - **Confirmations:** "Should I draft confirmation emails for tomorrow's external meetings each afternoon?" (Recommended if they or their delegate already send them.)
   - **Your email voice:** "I'll read 20 of your recent sent emails so drafts sound like you. OK?" Save the voice note.
   - **Loops:** "When I find proof a loop closed (like the signed contract arriving), should I close it for you with the proof attached, or list it for you to close?"
   - **Your two daily touchpoints:** "Everything that needs you comes together twice a day: a **Morning** review ready by 9:30am and an **End of day** review ready by 4:45pm. Do you want them as a task in your task tool (recommended) or as an email?" (conventions section 8). Don't offer Slack: the suite reads Slack but never delivers there.
3. **If you don't record calls:** set up dictation now (`tool-guides.md`, "Dictating without a recorder") and have them try it once.
4. **Existing automations: look first, then ask.** Before asking, search for what's already running, so nothing doubles up:
   - **Claude scheduled tasks** in their account (list them if the scheduling tool is available).
   - **Duplicate task patterns** in the task tool over the last 2 weeks: recurring names that match what the suite will create (`Call with`, `Follow up with`, `Prep for`, `Review |`, `LL |`, daily scan or loop tasks), especially ones created automatically at the same time each day.
   - **Recorder or email automations:** recorder summaries emailed after each call, auto-generated follow-up drafts, recurring "prep" calendar holds.
   - **Other installed skills** that cover the same job (another debrief, prebrief, or loop skill).
   Then show one short table: what you found | what it does | which Executive OS skill overlaps | **your suggestion: Keep theirs / Use ours / Run both** (with one line why). Ask "OK to go with these?" and also ask "Anything else that runs on its own that I couldn't see, like something on your computer or a tool your assistant set up?"
   - **Turning things off:** turn off only what they approve, and only things Claude can reach (its own scheduled tasks, skills). Anything Claude can't reach (an automation running on their computer, like Windows Task Scheduler or a Mac app, a Zapier or Make zap, a recorder setting) gets a `Turn off [name]` task with the exact steps, and the overlapping Executive OS skill stays off until they confirm it's done, so they never get two of the same thing.
5. **Changes without asking:** confirm `Writes allowed` with defaults: create tasks yes, update people pages yes, create email drafts yes, calendar changes only you see (colors, your own blocks) made automatically and listed as "Already fixed" so you can undo, and calendar changes that notify others always ask. Scan mode: review first for 2 weeks (explain the `Suggested` section: "Delete what's wrong; the rest moves into your list.").

Save the Preference Sheet (`conventions.md` section 1) to Claude memory if it's on; otherwise project instructions; otherwise ask them to paste it into Settings > Profile. **Also save the backup** (the `Executive OS | Preference Sheet` task, "Keeping preferences safe") and tell them in one line: "I saved a backup of your settings as a task called Executive OS | Preference Sheet. Don't delete it: if you ever reinstall or update, I'll restore your settings from it." Show the sheet.

## Part 4: Turn it on and show exactly what happens (10 minutes)

1. **Create the schedules** in `conventions.md` section 7, each calling its skill by name. Show the list with times. If one-time runs aren't available, say the per-call debrief falls back to the 5:45pm catch-all. If scheduling isn't available at all, say so plainly and give the two phrases to use instead ("good morning, run my Executive OS" and "debrief today's calls").
2. **Offer the history backfill:** "Want me to go back through your last 2 weeks of meetings and email (or 30 / 90 days) to build people pages and find open loops and commitments you haven't captured? I'll put them in `Suggested` for you to review." If yes, run it now and report counts.
3. **Preview every workflow, one at a time, with their real data.** This is the most important part of setup: by the end, the exec should be able to say "tomorrow at 9 I get a task that looks like this, I do these two things, and this happens." Go through **every installed workflow** in the order they'll meet them in a day: prebrief, debrief, Morning review, eDraft, End of day review, Friday calendar review. Skip only ones not installed. For each one, show this card, filled in from **their real calendar, inbox, and people for tomorrow** (never made-up names; if there's no real example, say "for example, if you had a call with someone tomorrow" and use a real past one):

   ```
   [WORKFLOW NAME]
   WHEN:       [tomorrow, Tue Nov 17, 7:42am]
   WHERE:      [inside the Asana task "Call with Maria Garcia - 2026-11-17"]
   IT LOOKS LIKE THIS:
     [a short real preview, 5-10 lines, in the exact format they'll get:
      the real task name, the real sections, real items from their data]
   YOU DO:     [1-3 concrete actions with time, e.g. "Open it before your 11am call. 60-second read."]
   THEN:       [what happens next because of what they did, e.g. "Delete a line and it's never suggested again. Leave it and it becomes a task tomorrow."]
   IF YOU DO NOTHING: [e.g. "Nothing is sent and nothing shared changes."]
   ```

   After each card ask **"Make sense, or want to change anything about this one?"** and wait. Change only what they ask (save both copies), then go to the next card. Never show two cards at once.

   Then **run one for real, right now**: the most useful one (today's or tomorrow's prebrief for their next external call, or a debrief of their last call). Open where it landed and point at each section in turn: "This section is X, it came from Y, and you do Z with it." Ask "Any questions on this part?" before the next section.

4. **The day plan.** End with this card, filled in with their real times, tool names, task names, and their first real meeting tomorrow. Offer to also save it as an `Executive OS | How your day works` task so they can find it later (same project as the backup; never completed).

```
YOUR DAY WITH THE EXECUTIVE OS
You check two tasks a day. Everything else lands where it belongs.

TOMORROW, [Tue Nov 17]
 [7:42am]  Your prebriefs are inside each call task.
           YOU: open "Call with [Maria Garcia] - [2026-11-17]" before your [11am]. 60-second read.
 [9:00am]  "Review | Morning [Tue Nov 17]" in [Asana].
           YOU: delete anything wrong (2 min). Answer any numbered question Y or N.
           THEN: what you keep becomes tasks; nudge drafts wait in [Gmail Drafts].
 After each call (10 min later)
           Action items and "LL | Did...?" questions appear in [Asana]; notes on the person in [People].
           A follow-up email draft waits in [Gmail Drafts].
           YOU: read the draft, edit, send. Nothing ever sends on its own.
 [4:00pm]  "Review | End of day [Tue Nov 17]" in [Asana].
           YOU: answer the Y/N decisions (2 min).
           THEN: I make the "yes" changes and confirm in the task.
 ANY TIME  Type or say "Edraft: [a few sentences]" -> a ready draft in [Gmail Drafts].

EVERY FRIDAY [8:23am]
           Next week's calendar review, inside Friday's Morning review.
           Changes only you see are already made (undo any). YOU: reply "1 Y, 2 N".

[YOUR DELEGATE, JORDAN]
           Gets their own Morning and End of day tasks: scheduling, nudges, loop checks.
FIRST 2 WEEKS (until [Nov 30])
           New items arrive as "Suggested": delete mistakes; the rest moves in the next day.
IF YOU DO NOTHING
           Nothing is sent, nothing anyone else sees changes.

Change anything: say "update my setup". See this again: say "how does my day work?"
```

5. Close: "The first thing you'll get is [first scheduled run, day and time]: [one line on what it is]. Nothing else to do today."

## Welcome back (a sheet or backup already exists)

Someone who reinstalled, updated, or said "set up my executive OS" again. Never start over and never save over their settings without a yes.

1. **Restore if needed.** If the sheet is only in the backup, put it back in memory first.
2. **Say what you found**, in one short block: "Welcome back. I found your settings from [Last saved date]: [3-5 key lines, e.g. tasks in Asana, prebriefs in your call tasks, EA Jordan in Mode 1, reviews by 9:30am and 4:45pm]."
3. **Ask one question:** "Keep these and just check everything's running, or change something?" Default: keep.
   - **Keep:** check the connectors still work (one line per tool), check every schedule in section 7 exists and is on (recreate any that are missing, with their saved times), check the skills listed in `Skills on` are installed, ask only fields that are new since their `Suite version` ("After an update", section 1), then show the day plan card. About 3 minutes.
   - **Change something:** go to "Update my setup" (show the sheet, change only what they name, show the changed lines, save both copies).
   - **Start over** (only if they say so explicitly): save the current sheet into the backup task as a comment titled "Previous settings [date]" first, so it can be brought back, then run Parts 1-4.

## Delegate onboarding ("onboard my EA")

Run with the delegate present, or in the delegate's own Claude for Mode 2.
1. The split, in one line: "AI captures and drafts. You execute and chase. [Exec] decides and speaks in their own voice." Then the talking points in `ea-playbook.md`.
2. Walk the "Who does what" table for the skills that are on.
3. Show where their work lands (their tasks, the `LL | Did...?` list) and the daily rhythm.
4. Mode 2 only: install the same skills, connect the delegate's Claude to the exec's delegated calendar and email, save the same Preference Sheet with `Operator: [name]`, and test by listing the exec's meetings tomorrow. Move the scan, prebrief, and Friday review schedules to the delegate's Claude.
5. First shared workflow: the Friday calendar review. The delegate fixes logistics; the exec answers the numbered decisions.

## Adding one skill later ("set up [skill]")

Explain in one line what the skill is for (the Part 1 line). Check only the tools and Preference Sheet fields that skill needs, create its schedule, do one live run and walk through each part of it (Part 4 step 3), and show its preview card (Part 4 step 3) and where it appears on the day plan.
