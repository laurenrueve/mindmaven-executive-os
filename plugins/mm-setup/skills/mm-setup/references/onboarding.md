# Onboarding (about 30 minutes)

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
> You'll hear from it **twice a day**: once in the morning and once at the end of the day. Setup takes about 30 minutes.

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
5. **Changes without asking:** confirm `Writes allowed` with defaults: create tasks yes, update people pages yes, create email drafts yes, calendar changes that notify others always ask. Scan mode: review first for 2 weeks (explain the `Suggested` section: "Delete what's wrong; the rest moves into your list.").

Save the Preference Sheet (`conventions.md` section 1) to Claude memory if it's on; otherwise project instructions; otherwise ask them to paste it into Settings > Profile. Show it.

## Part 4: Turn it on (5 minutes)

1. **Create the schedules** in `conventions.md` section 7, each calling its skill by name. Show the list with times. If one-time runs aren't available, say the per-call debrief falls back to the 5:45pm catch-all. If scheduling isn't available at all, say so plainly and give the two phrases to use instead ("good morning, run my Executive OS" and "debrief today's calls").
2. **Offer the history backfill:** "Want me to go back through your last 2 weeks of meetings and email (or 30 / 90 days) to build people pages and find open loops and commitments you haven't captured? I'll put them in `Suggested` for you to review." If yes, run it now and report counts.
3. **One live run, together, then walk through each part.** Run the most useful thing right now with real data: today's prebrief for their next external call, or a debrief of their last call. Open where it landed, then go through it section by section: what each section is, where it came from, and what they do with it ("This is your action items section. Each one is now a task in Asana, here. This one is a loop leverage question your delegate will check on Thursday..."). Ask "Any questions on this part?" before moving to the next section.
4. **Tell them exactly what to expect** with this card, filled in with their real times, tools, and names:

```
WHAT HAPPENS NOW
You hear from it twice a day. Everything else just lands where it belongs.

MORNING (ready by 9:30am) -> "Review | Morning" [task in Asana / email]
  - Anything to fix before today's calls
  - Morning scan: promises you didn't capture, open commitments, personal moments
  - Loops that need you
  - Fridays: next week's calendar review. Reply to each numbered item Y or N.

END OF DAY (ready by 4:45pm) -> "Review | End of day" [task in Asana / email / from Jordan]
  - End-of-day update: what got done, yes/no decisions, tomorrow at a glance
  - Tomorrow's calendar fixes and confirmation drafts
  - Anything from today's debriefs that needs you

LANDS ON ITS OWN (nothing to review)
  - Prebriefs -> [inside each "Call with" task / one morning email / both]
  - After each call: action items, follow-ups, notes on the person -> [Asana] + [People];
    follow-up email -> [Gmail Drafts]
  - Say "Edraft:" + a few sentences any time -> a send-ready email in [Gmail Drafts]

Your delegate [Jordan]
  Gets their own Morning and End of day reviews: scheduling, nudges, "LL | Did...?" checks
First 2 weeks
  New items land in "Suggested" so you can delete mistakes. Then they go straight in.
Change anything: say "update my setup".
```

5. Close: "The next thing you'll get is [first scheduled run, day and time]. Nothing else to do."

## Delegate onboarding ("onboard my EA")

Run with the delegate present, or in the delegate's own Claude for Mode 2.
1. The split, in one line: "AI captures and drafts. You execute and chase. [Exec] decides and speaks in their own voice." Then the talking points in `ea-playbook.md`.
2. Walk the "Who does what" table for the skills that are on.
3. Show where their work lands (their tasks, the `LL | Did...?` list) and the daily rhythm.
4. Mode 2 only: install the same skills, connect the delegate's Claude to the exec's delegated calendar and email, save the same Preference Sheet with `Operator: [name]`, and test by listing the exec's meetings tomorrow. Move the scan, prebrief, and Friday review schedules to the delegate's Claude.
5. First shared workflow: the Friday calendar review. The delegate fixes logistics; the exec answers the numbered decisions.

## Adding one skill later ("set up [skill]")

Explain in one line what the skill is for (the Part 1 line). Check only the tools and Preference Sheet fields that skill needs, create its schedule, do one live run and walk through each part of it (Part 4 step 3), and show where it appears on the "What happens now" card.
