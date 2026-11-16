# How an EA works with the Executive OS

The core split, and the line to teach every client:

> **AI captures and drafts. The EA executes and chases. You decide and speak in your own voice.**

The AI never forgets a commitment or a detail, and it never gets tired of checking a calendar. The EA is the one who makes things actually happen: booking, rescheduling, sending materials, following up on logistics. The executive is protected for the things only they can do: judgment, relationships, and anything that should sound like them.

## The three modes

Setup records one of these. **Always explain all three before asking**, using the short version below, then let the exec pick. The "EA" can be any delegate: an EA, chief of staff, or a colleague who already helps with follow-through.

The one question that separates Mode 1 and Mode 2: **whose Claude does the work?**

| | Mode 0: Just me | Mode 1: My delegate gets tasks | Mode 2: My delegate runs it |
|---|---|---|---|
| **In one line** | The AI works for you; there's no delegate | The AI works for you, and hands logistics to your delegate | The AI works for your delegate, who runs it on your behalf |
| **Whose Claude runs the skills** | Yours | Yours | Your delegate's (with access to your calendar and email) |
| **What your delegate does** | n/a | Gets assigned tasks in your task tool (scheduling, sending materials, chasing `LL \| Did...?` questions) | Runs the morning scans, prebriefs, and Friday review; fixes what they can; sends you only decisions |
| **What you see** | Everything | Everything, minus the logistics | Only decisions and your own touches |
| **What it needs** | Nothing | Your delegate in your task tool | Delegate access to your calendar and email, and the suite installed in their Claude |
| **Best for** | No delegate yet, or trying it out | Starting out with a delegate (everyone starts here) | After 2-4 weeks in Mode 1, once you trust the output |

Example to say out loud: *"In Mode 1, Claude debriefs your call and puts 'Schedule follow-up with Maria' on Jordan's list. In Mode 2, Jordan's own Claude does the debrief and the Friday review, books what it can, and sends you one message with just the decisions."*

Details:
- **Mode 0:** recommend batching: one 15-minute block in the morning for scan results and prebriefs, one at the end of the day for anything debriefs flagged.
- **Mode 1:** needs nothing new from the delegate. The weekly calendar review goes to them as a fix list.
- **Mode 2:** the delegate's Claude uses delegated access (Google Workspace delegation or Outlook delegate access). The exec still runs anything that depends on their own private accounts: usually debriefs (if recordings are only in the exec's recorder account) and the Slack/Teams part of the missed-task scan, since a delegate can't read the exec's DMs.

In Mode 2, the EA's Claude uses the **same Preference Sheet** with `Me:` still set to the executive, plus `Operator: [EA name]`. Everything is written in the executive's task tool and people database so there is one source of truth.

## Loop leverage ownership

Mindmaven's rule: the EA owns the tickler file. Every `LL | Did [X]...?` question (gets, gives, and the check on each personal touch) is assigned to the EA, who scans 8-15 a day, checks the inbox to see if each loop closed, nudges the other party or reminds the exec, and completes the ones that are done. The AI creates the questions and can run the daily check; the EA makes the call. In Mode 0 the exec owns them.

## Who does what, per workflow

| Workflow | Runs it | AI does | EA does | Executive does |
|---|---|---|---|---|
| Meeting debrief | Exec (Mode 2: EA if they have recorder access) | Extracts tasks, LLs, people notes; drafts LL messages | Executes logistics tasks (scheduling, sending materials); owns and closes the `LL \| Did...?` questions; runs the AM Ping | Dictates or approves the debrief; owns judgment tasks and all personal touches |
| Prebrief | Mode 2: EA, night before. Else exec, morning of | Builds the brief from people pages, tasks, email | Adds anything only they know (a call they took, a dietary note for a lunch); confirms logistics | Reads it before the meeting (5 min) |
| Calendar review | Mode 2: EA, Friday. Mode 1: exec runs, EA gets fix list | Flags issues, proposes fixes | Fixes logistics (adds missing attendees after approval, adds links/locations, books travel time, reschedules) | Decides tradeoffs: what to decline, move, or protect |
| Email loop scan | Mode 2: EA (delegated inbox). Else exec | Finds personal moments, drafts LL tasks and messages | Reviews for accuracy, approves LL tasks onto the exec's list | Sends the touches in their own voice |
| Missed-task scan | Exec for Slack/Teams; EA can run the email part in Mode 2 | Finds uncaptured commitments | Takes logistics items; confirms which are already done | Approves own items; says no to things not worth doing |
| Loop manager | Scheduled; delivered to the EA (exec in Mode 0) | Checks every source for closed loops, drafts nudges, moves intros along | Sends the nudges, closes loops, asks the exec about stale ones | Does the gives and personal touches it's reminded of |
| Calendar upkeep | Scheduled; delivered to the EA (exec in Mode 0) | Checks tomorrow, fixes the exec's own events, drafts confirmations | Sends confirmations, fixes logistics, answers what they can | Answers the numbered decisions |
| eDrafts | Exec dictates any time | Turns the dictation into a draft in the exec's voice | Proofreads, attaches files, reminds the exec of drafts unsent after 48 hours | Edits if needed and presses send |
| EOD update | Scheduled; drafted for the EA (straight to the exec in Mode 0) | Gathers the day: confirmations, decisions, tomorrow, loops | Adds what only they know, sends it | Replies Y/N to the numbered decisions |

## What the EA should never do (by default)

- Send a personal touch (a moment message) as the executive. Those only work if they're genuinely from the person. The EA owns the `LL | Did...?` question that checks it happened, not the touch itself.
- Send email in the executive's name without written authorization ("I authorize [EA] to send..."). Default is drafts; the exec presses send.
- Accept or decline meetings that involve a judgment call (investors, key clients, board) without asking.
- See items the executive marks private. Setup can list private calendars, labels, or people the EA's Claude should skip.

## Rhythm with an EA (Mode 2 example)

| When | EA | Executive |
|---|---|---|
The exec hears from the suite twice a day (conventions section 8). The delegate has their own Morning and End of day touchpoints.

| When | EA | Executive |
|---|---|---|
| Weekday 7:30 | Prebriefs land in the call tasks | Reads them before each call |
| Morning (by 9:30) | Works their Morning touchpoint: the morning scan, the loops list (sends nudges, closes loops) | **Morning touchpoint:** clears own items (5 min); Fridays, answers the calendar review |
| After each call | Takes logistics tasks from debriefs | Dictates or approves the debrief (2-5 min) |
| Afternoon | Works tomorrow's upkeep list, sends confirmations | Nothing |
| End of day (4:30) | Finishes and sends the EOD, which holds every decision for the exec | **End of day touchpoint:** replies Y/N to the EOD decisions |
| Friday | Runs calendar review (next week + 2-3 week lookahead), fixes logistics, books travel holds, flags LLs needing prep (a gift, a card); the judgment list goes in the exec's Friday Morning touchpoint | Answers the judgment list (10 min) |

## Talking points for the EA

- "You're not being replaced by AI, you're being promoted. You stop being the memory and start being the operator."
- "Your job each day: run it, check it, fix what you can, and send your exec a short list of only what needs them."
- "If the AI got something wrong, fix it in the task or page directly. The next run builds on whatever's there."
