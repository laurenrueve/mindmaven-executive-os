---
name: mm-setup
description: Set up, onboard, and change settings for the Mindmaven Executive OS, a connected suite of scheduled skills (prebriefs, debriefs, morning scans, loop manager, eDrafts, daily calendar upkeep, end-of-day update, Friday calendar review) that work with the user's EA or delegate. Reads the calendar and inbox first to propose preferences, explains the delegate modes, sets where everything lands, creates the schedules, offers a history backfill, and ends with exactly what to expect and when. Use when the user says "set up my executive OS", "onboard me", "continue my setup", "set up [skill name]", "update my setup", "connect my calendar/recorder/task tool", "how does my EA fit in", "onboard my EA", "what can this do", or when another Mindmaven skill finds no setup.
---

# Mindmaven Executive OS: setup and onboarding

The front door to the suite. Four jobs:
1. **Explain the system** in under a minute.
2. **Build one Preference Sheet** every skill reads (`references/conventions.md`, section 1), mostly by reading the exec's calendar and tools and asking them to correct it.
3. **Turn it on:** create the schedules (`conventions.md` section 7), offer a history backfill, and run one thing live.
4. **Set expectations:** preview every workflow one at a time with their real data (what it looks like, what they do, what happens next), then end with the day plan card, so the exec knows exactly what they'll get tomorrow, where, and what to do with it.

Read `references/conventions.md` first. Then:

| The user says | Do this |
|---|---|
| "Set up my executive OS" (or any setup request) | **First, look for an existing sheet**: Claude memory, then the `Executive OS \| Preference Sheet` backup (`conventions.md` section 1, "Keeping preferences safe"). Found: `onboarding.md`, "Welcome back". Not found: `onboarding.md`, Parts 1-4 |
| "Continue my setup" | Pick up at the first Part not yet saved |
| "Set up [skill]" | `onboarding.md`, "Adding one skill later" |
| "Update my setup" / change one setting | **First, the update check:** compare `Suite version` in the sheet with this copy's version (top of `conventions.md`). If newer, read `whats-new.md` and say what's new in plain words, ask only the new settings, offer any new scheduled runs and create them on yes, then set `Suite version`. Also check every run in section 7 that their sheet says is on actually exists, and offer to recreate any that are missing. If they're already current, say so in one line ("You're on the latest version, [x.y.z]"). Then change only what they asked, update any affected schedule, save both copies, and show the changed lines. |
| "How does my EA fit in?" | The three-mode table in `references/ea-playbook.md`, with the example |
| "Onboard my EA" | `onboarding.md`, "Delegate onboarding" |
| "What can this do?" / "What happens when?" / "How does my day work?" | The day plan card (`onboarding.md` Part 4 step 4) with their real times, places, and tomorrow's real meetings. "Show me the [workflow]" -> that workflow's preview card (Part 4 step 3) |

Always one question at a time, with a suggested default. Use the exec's real meetings, emails, and people, never made-up examples. Always explain the delegate modes before asking which one they want.
