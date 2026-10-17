---
name: weekly-recheck
description: Use when the scheduled weekly routine fires, or when the user asks "what changed" or "anything new". Reruns the page check and reports only what is new since the last run.
---

# Weekly re-check

This skill is driven by a routine that is off by default. The routine is turned on only after the user says yes in getting started, and runs at the day and hour saved in prefs, in the user's timezone. Default when the user gives no preference: Monday, 9:00.

## Steps

1. Rerun the Page check skill on the saved page list. Add any new page that now appears in the navigation under pricing, plans, security, or integrations.
2. Compare the result with the newest saved findings list.
3. Sort every finding into one of four groups:
   - **New:** not in the last list.
   - **Still open:** in the last list and still present.
   - **Fixed:** in the last list and no longer present. Confirm by rereading both pages.
   - **Back again:** marked fixed earlier and present again.
4. Save the new dated list.

## Report

Report only if there is something new, fixed, or back again. If nothing changed, send nothing. No "all clear" messages.

Lead with one line ("2 new, 1 fixed since last Monday"). Then:

- **New** findings in full, in the page check format.
- **Back again** findings in full, with the date they were marked fixed.
- **Fixed:** one line each.
- **Still open:** a count only.

Report each finding as new exactly once. A finding that stays open is never repeated in later weeks.

Findings the user marked "fine" are never reported again.

## Bot check

The weekly routine does not question the user's other bots. That runs only when the user asks.
