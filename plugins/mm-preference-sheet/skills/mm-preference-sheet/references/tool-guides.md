# Tool guides

Connectors are turned on in Claude under **Settings > Connectors** (on the desktop app or claude.ai). Connector names and availability change over time: if a tool below isn't in the user's connector list, use the fallback and don't claim it exists.

General connection steps for any connector:
1. Open Claude > Settings > Connectors.
2. Find the tool (use "Browse connectors" if it isn't listed).
3. Click Connect, sign in to that tool, and approve access.
4. Come back to the chat and say "done". Then test it.

In any single chat, the user may also need to enable the connector from the tools menu in the message box.

## Recorders

| Tool | How to connect | Test | Fallback |
|---|---|---|---|
| Fathom | Fathom connector | List last 5 meetings | Copy transcript from the Fathom call page and paste |
| Granola | Granola connector | List recent notes | Copy the transcript from Granola and paste |
| Quill | Quill connects locally on the user's computer (Quill desktop app settings) | Search recent meetings | Export or copy transcript |
| Fireflies, Otter, tl;dv | Check connector directory | List recent meetings | Download transcript (.txt or .docx) and upload |
| Zoom / Teams / Meet recordings | Check connector directory | Find meeting | Download the transcript file from the platform and upload |
| No recorder | n/a | n/a | Paste rough notes. The skill still works, just with less detail |

Always pull the full transcript. Recorder summaries are useful as a cross-check, but they drop personal details.

## Dictating without a recorder

Mindmaven execs dictate a debrief within about 5 minutes of a call, in APPA order: "This is a debrief for my meeting today with [First Last] at [Company]. Action items... Professional challenges... Personal interests... About/facts... Anything else." Three ways that work with no recorder, easiest first:

1. **Claude mobile app:** open Claude on the phone, start a new chat, tap the **microphone**, and speak the debrief starting with "Debrief:". The debrief skill picks it up right there.
2. **Email:** send a voice-to-text note (phone keyboard mic) to yourself with the subject starting **"Debrief:"**. The 5:45pm catch-all picks up every "Debrief:" email from that day.
3. **Voice memo app:** record, copy the transcript, paste it into Claude with "Debrief:".

Setup has them try one once. For calls the exec never records, the catch-all creates `Debrief from your notes - [First Last]` with these steps in it.

## Task tools

| Tool | Notes |
|---|---|
| Asana | Pick a project (suggest `Meeting Follow-ups`). Assign EA tasks to the EA's Asana user. |
| Notion | Use an existing tasks database, or create one with Name, Owner, Due, Status, Source meeting. |
| ClickUp | Pick a List. Assign EA tasks to the EA. |
| Trello | Pick a board and list (suggest a `Meeting Follow-ups` list). Put the due date on the card. |
| Microsoft To Do | Pick a list. To Do has no assignees, so EA tasks go to a separate shared list. |
| Todoist | Pick a project. Use the due date field. |
| Other / not connectable | Produce a clean checklist the user can copy, or a CSV they can import. |

Loop leverage tasks (`LL | ...`) go in the same tool, always with a due date. In tools with sections or lists (Asana, ClickUp, Trello, To Do, Todoist), use the LL section/list from setup if there is one. In Notion, add a `Type` select (Task / Loop leverage) to the tasks database so they can be filtered.

## Email, calendar, and chat

| Tool | How to connect | Test | Notes |
|---|---|---|---|
| Gmail | Gmail connector | Search last 24h of inbox | Drafts only. Never send without an explicit yes. |
| Google Calendar | Google Calendar connector | List tomorrow's events | Edits that add attendees or change times notify others: approval required per change. |
| Outlook mail + calendar | Microsoft 365 connector (check directory) | Same | Same rules. |
| Slack | Slack connector | Search the user's own messages from yesterday | Read only: used to find commitments and check whether things are done. The suite never posts to Slack. |
| Microsoft Teams | Microsoft 365 connector, if it includes Teams | Same | If not available, the missed-task scan runs on email only and says so. |

### Google Calendar colors: use these exact names and IDs

Google has **two separate color lists**, and the API returns only numbers, never names. Use these tables; never guess.

**Event colors** (what you set on one event; the API's `colorId`). Only these 11 exist:

| colorId | Name in Google Calendar | Hex |
|---|---|---|
| 1 | Lavender | #7986CB |
| 2 | Sage | #33B679 |
| 3 | Grape | #8E24AA |
| 4 | Flamingo | #E67C73 |
| 5 | Banana | #F6BF26 |
| 6 | Tangerine | #F4511E |
| 7 | Peacock | #039BE5 |
| 8 | Graphite | #616161 |
| 9 | Blueberry | #3F51B5 |
| 10 | Basil | #0B8043 |
| 11 | Tomato | #D50000 |
| (none) | "Calendar color": the event uses its calendar's color | |

**Calendar colors** (one color for a whole calendar, set in that calendar's settings): Cocoa, Flamingo, Tomato, Tangerine, Pumpkin, Mango, Eucalyptus, Basil, Pistachio, Avocado, Citron, Banana, Sage, Peacock, Cobalt, Blueberry, Lavender, Wisteria, Graphite, Birch, Radicchio, Cherry Blossom, Grape, **Amethyst**.

How to apply the exec's color rules:
- When saving `Colors:` in the Preference Sheet, write each as the exact event name **and** ID, e.g. `Internal = Lavender (1)`.
- If the exec names a color that is **only** a calendar color (Amethyst, Cocoa, Pumpkin, Mango, Eucalyptus, Pistachio, Avocado, Citron, Cobalt, Wisteria, Birch, Radicchio, Cherry Blossom), it can't be set on one event. Check which of their calendars uses that color. If it's their main calendar's color, the rule means "leave the event on calendar color" (no `colorId`). Otherwise ask which of the 11 event colors to use instead, one question, offering the two nearest (e.g. Amethyst -> Lavender or Grape; Cobalt -> Peacock or Blueberry; Pumpkin -> Tangerine or Banana). Never pick one silently.
- When reading an event: `colorId` empty means calendar color; report it as "[calendar name]'s color ([that calendar's color name])".

Microsoft Outlook uses named categories instead of colors: read the category names the exec already uses and match them exactly.

For an EA in Mode 2 (see `ea-playbook.md`): the EA connects their own accounts in their own Claude, and the executive grants delegate access to calendar and mail in Google Workspace or Outlook. Chat DMs can't be delegated, so the executive runs the chat part of the missed-task scan.

## People notes destinations

| Tool | Where notes go |
|---|---|
| HubSpot | Contact record: add a Note on the timeline. Only update properties the user approves. |
| Salesforce, Attio, Affinity, Folk | Add a note to the person record. |
| Notion | The People database (see `notion-people-database.md`). |
| Google Sheet | One row per person with the same columns as the Notion database. |

Always search for the existing person first. Add, never overwrite.
