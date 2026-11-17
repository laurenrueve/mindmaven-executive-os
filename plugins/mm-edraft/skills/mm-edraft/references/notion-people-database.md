# Notion People database (for users without a CRM)

Create a database called **People** inside a page called `Relationships`.

**Private by default.** People pages hold personal details (spouses, kids, health, challenges), and most Notion workspaces are shared with a team. Always create the `Relationships` page in the user's **Private** section, never in a teamspace or a shared page, unless the user explicitly asks to share it. Then tell them in one line: "Your People database is in your Private section, so only you can see it. If your EA needs it, share the Relationships page with just them (Share > invite)." After creating it, fetch the page and confirm it isn't inside a teamspace; if it is, say so and move it to Private only with the user's OK.

## Properties

| Property | Type | Notes |
|---|---|---|
| Name | Title | Full name |
| Company | Text | |
| Title | Text | |
| Email | Email | |
| Cell | Phone | Backup contact for prebriefs |
| LinkedIn | URL | |
| We Met | Text | How and when the exec first met them, and who introduced them |
| Relationship | Select | Client, Prospect, Investor, Partner, Team, Friend, Other |
| Last met | Date | Updated after each debrief |
| Next touch | Date | Date of the earliest upcoming loop leverage |
| Location | Text | Where they live now (and hometown, if known) |
| Family | Text | Spouse/partner and kids' names and ages, dated |
| Professional Challenges | Text | APPA. Short dated bullets, newest first |
| Personal Interests & Passions | Text | APPA |
| About/Facts | Text | APPA: everything else worth remembering |
| NRM group | Select | Optional: which relationship group (for future Mindshare skill) |
| Last touch | Date | Last meaningful outreach (any direction) |
| Upcoming moments | Text | Open loop leverages with dates |
| Source meetings | URL or Text | Links to the recordings |

## Each person's running page

Every row in the database opens as a page. That page is the running record of the relationship: everything learned about this person, across every meeting, in one place. The properties are the quick-glance summary for views and filters. The page is the full story.

When creating a new person, build the page with this template:

```
[Callout] Quick glance
  Who: [Title] at [Company]  |  We met: [how, when, who introduced]
  Family: [Spouse/partner, kids with ages, dated]
  Location: ...  |  Cell: ...  |  LinkedIn: ...
  Personal Interests & Passions: [top 2-3]
  Professional Challenges: [current biggest]

## Upcoming moments
  [ ] [M/D] [Moment] -> [touch]  (task + LL question links)

## Open commitments
  [ ] Given: [task]  ->  LL | Did [Exec]...?
  [ ] Received: LL | Did [Name]...?

## Running notes
  ### [YYYY-MM-DD] | [Meeting title]  ([link to recording])
    Discussed: 2-4 bullets on what the conversation was about
    Action items: given and received, with links to their tasks and LL questions
    Professional Challenges: ...
    Personal Interests & Passions: ...
    About/Facts: ...
    (every line has its receipt: timestamp, dictation line, or email link)

## No longer true
  - [date] [old fact] -> replaced by [new fact] ([receipt])
```

**After every debrief, update the page:**
1. Add a new entry at the **top** of `Running notes` (newest first) using the format above. Never edit or delete older entries.
2. Refresh the **Quick glance** callout so it reflects the latest. This is the one section that gets rewritten. If a fact changed (new job, new city), the old value still lives in the older running note, so nothing is lost.
3. Add new loop leverages to `Upcoming moments` (with a link to the matching `LL |` task in the task tool, since the task is what reminds the user) and new commitments to `Open commitments`. Check off any that this meeting shows are done (the trip happened, the deck was sent). Don't remove checked items.
4. Update the `Last met` and `Next touch` properties.

**Notes outside meetings:** the user can also say "add a note to Maria's page: she just got promoted" or "Maria's daughter got into Michigan". Add it as a dated entry in `Running notes` (title it `[YYYY-MM-DD] | Note`), and update Quick glance, Upcoming moments and properties the same way.

**Before a call:** if the user asks "what do I know about Maria?" or "prep me for my call with Maria", read her page and give a short brief: Quick glance, open commitments, upcoming moments, and the last 2-3 running notes.

## Views to create

1. **All people** (table, sorted by Last met, newest first).
2. **Upcoming touches** (table, filtered to Next touch is within the next 7 days, sorted ascending). This is the "who should I reach out to this week" view. Use 7 days: a rolling 14-day window couldn't be built with Notion's relative date filters in testing.

After creating it, add the attendee from the first real debrief so the user sees a filled-in example.

## Which skills touch the page

| Skill | What it adds |
|---|---|
| `mm-meeting-debrief` | A `Running notes` entry per meeting, Quick glance refresh, moments, commitments |
| `mm-email-loop-scan` | A `[date] \| From email: [subject]` entry with the new facts, new Upcoming moments |
| `mm-meeting-prebrief` | Reads only. Never writes. |
| `mm-calendar-review` | Reads only (to recognize who attendees are). |

Entries from email use the same format but only the APPA lines that apply and any moments.
