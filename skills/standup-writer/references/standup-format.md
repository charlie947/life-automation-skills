# Standup format: how to shape the update

A status update is read in seconds by a busy person. Lead with outcomes, cut the process, and never write a line the sources cannot back. Pick one of the two structures below and keep to it.

## The two structures

### Done / Doing / Blockers (default)
The daily and weekly standard. Best for a team sync.
- **Done**: work that is finished, shipped, closed, or decided in the window. Past tense.
- **Doing**: work genuinely underway now, or the very next thing. Not a wishlist.
- **Blockers**: what needs a decision or another person before it can move. Name the owner.

### Progress / Plans / Problems
The same shape in reporting language. Best for a manager or a cross-functional update.
- **Progress**: what moved forward, with the outcome.
- **Plans**: what is next and by when.
- **Problems**: risks and blockers, with what you need to clear them.

Map task status straight across: Done → Done/Progress, In Progress → Doing/Plans, Blocked → Blockers/Problems.

## Outcome-led writing rules

1. **Verb first, outcome first.** "Shipped the export feature", not "I have been working on the export feature". State the result, then the detail only if it earns its place.
2. **One clause per line.** If a line needs an "and", it is probably two lines.
3. **A metric only if a source carries it.** Never invent a number to make a line sound bigger. "Closed the top 3 support tickets" beats a made-up "reduced tickets 40%".
4. **Past tense for Done, present for Doing.** Tense signals status. Keep it honest.
5. **Cut the process.** The reader wants the result, not the journey. No "spent time on", no "had a call about", unless the call produced a named outcome.
6. **Length the reader will actually read.** A daily standup is 3 to 6 lines total. A weekly update is one screen. If it is longer, you are padding.

## Activity is not achievement

This is the line that keeps the update honest. The sources record activity. The update reports achievement. They are not the same thing.

- A Slack message about a task is not the task being done.
- A meeting on the calendar is not an outcome from the meeting.
- An "In Progress" ticket is not shipped.
- Ten messages in a channel is not "drove the discussion" unless a decision came out of it.

If the source shows the activity but not the result, write the result as `[NEEDS: …]` and let the user fill it. Never guess.

## Good vs bad lines

| Weak (process, vague, or invented) | Strong (outcome, evidenced) |
|---|---|
| Worked on the onboarding flow | Shipped the new onboarding flow, live to all signups |
| Had a lot of meetings about pricing | Agreed the pricing tiers in the pricing sync. [NEEDS: are they signed off?] |
| Made great progress on the migration | Migrated the reporting dashboard, ~60% done, on track for Friday |
| Improved performance by ~30% *(no source)* | Cut the report load time. [NEEDS: the exact number] |
| Closed lots of tickets | Closed 4 of 6 billing tickets. [NEEDS: which 2 remain] |

## Before you hand it over

- Every Done line points to a real source (Slack, Calendar, or a task).
- No line claims a result the sources do not show. Unproven results are `[NEEDS: …]`.
- The gaps are visible, not smoothed over.
- The sources used, and any source not connected or with nothing found, are listed so the user can see what was and was not covered.
