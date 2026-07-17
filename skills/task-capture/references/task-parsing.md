# Task parsing: what counts, and how to write it down

The whole value of this skill is that every line on the list is a real, doable job. A list padded with FYIs and invented deadlines is worse than no list. When in doubt, leave it off and flag it, never guess it on.

## What counts as a task

A task is a concrete action a named person is expected to take. It passes three checks:

1. **There is an action.** A verb you could do: send, review, book, confirm, reply, draft, pay, call, decide.
2. **Someone is on the hook.** A real person owns it (often the user, sometimes a named other).
3. **It is not already done.** If the thread shows it was completed, it is not a task.

Good signals that a task is real:
- A direct ask: "Can you send me the deck by Friday?"
- A commitment the user made: "I'll get you the numbers tomorrow."
- An assignment to someone named: "Sam, can you book the room?"
- A decision the user is being asked to make.

## What is NOT a task (leave it off, flag as FYI)

- **Awareness only.** CC'd for visibility, status updates, "just so you know".
- **Chatter and opinion.** Reactions, thanks, "sounds good", banter.
- **Already resolved.** The reply that answered the ask is in the thread.
- **Someone else's job with no involvement from the user.** Note it only if the user asked for a full extraction. Otherwise it is noise.
- **A vague wish with no owner and no action** ("we should really improve onboarding"). Not a task until someone owns a next step.

If a message says "URGENT: action required" but names no concrete action, treat the urgency as noise, not a task. Loud is not the same as real.

## How to set the owner

- Take the owner from the text. The person the ask is directed at, or the person who committed.
- Default to **the user** only when the text makes it their job (they were asked directly, or they said they would do it).
- If no owner is stated and it is not clearly the user's, set `[NEEDS: owner]`. Do not assign it to someone by guessing.

## How to set the due date

- Only from a real, stated deadline. "By Friday", "before the board meeting on the 21st", "end of day".
- Convert relative dates against the message date, and keep the format the destination expects (DD/MM/YYYY unless the list uses another).
- If a day is named with no date ("Thursday"), keep the word rather than inventing a calendar date, unless the year and week are unambiguous.
- No deadline stated means **no due date**. Leave it blank. Never manufacture one to look tidy. If a date clearly matters but was not given, use `[NEEDS: date]` and flag it.

## One-task-per-line format

Write each task so it stands alone, out of the thread:

- **Start with a verb.** "Send the signed MSA to legal" not "The MSA needs sending".
- **Name the object and the who.** Enough that the user knows what and for whom without reopening the source.
- **Keep it to one action.** If a message contains three asks, that is three lines, not one.
- **Split compound asks.** "Review and send" is two jobs if they can happen separately.
- **Attach the source.** Every task carries where it came from (Gmail subject, Slack channel) so the user can check it in one click.

Template per task:

```
<Verb> <object> <for whom / detail>   | owner: <name/You>   | due: <date or blank>   | source: <ref>
```

## Dedupe rules

- **Read the destination first.** Compare candidates against open tasks already on the list.
- A candidate is a duplicate when the action and owner match an existing task, even if the wording differs ("Send Q3 deck" vs "Get the Q3 deck to Priya").
- Drop duplicates inside the same batch too. One thread often repeats the same ask.
- **When unsure, keep both and flag it.** Silently merging two tasks that were actually different is the worse error. A visible near-duplicate the user can delete beats a real task quietly lost.

## The honest-list test

Before showing the list, check each line:
- Is the action really in the source, or did I infer it?
- Is the owner stated, or did I assume?
- Is the due date stated, or did I round a vague word into a date?

If any answer is "I inferred it", either fix it to a `[NEEDS: …]` flag or cut the line. A short true list beats a long confident one.
