# Scheduling etiquette: buffers, hours, holds, timezones

The rules that keep a booked calendar humane and correct. Apply them before proposing or placing any event. When the user states their own preference, that always wins over these defaults.

## Working hours
- Default window: 09:00–17:30, Monday to Friday, in the user's calendar timezone. Never propose outside it unless asked.
- No slots before the user's start, after their end, or at the weekend, without an explicit request.
- Protect declared blocks: lunch, focus time, the school run, standing 1:1s. Treat anything marked busy or focus as immovable unless told otherwise.
- First-thing and last-thing slots are the least popular. Offer them only when the middle of the day is full, and say why.

## Buffers (no back-to-back)
- Keep a gap either side of a meeting. Default 10 minutes. Longer for anything needing prep or travel.
  - Internal call: 10 min.
  - External or client call: 15 min (context switch plus notes).
  - In-person: add realistic travel time both ways, never zero.
- Never stack three or more meetings with no gap. If the day is already wall-to-wall, flag it rather than adding a fourth.
- A "30-minute meeting" placed at :00 should aim to end by :25, keeping the buffer intact.

## Hold vs confirm
The single most useful distinction in scheduling. Get it wrong and you either double-book or annoy people.

- **Confirm** = a real, agreed meeting. Both sides have said yes. It goes on as a normal event, attendees invited, and Google sends the invite.
- **Hold** = a tentative placeholder the user can drop. Use it when a time is proposed but not yet agreed.
  - Title it clearly: prefix `HOLD:` (or `[TENTATIVE]`).
  - Mark it tentative and show-as-free, so it does not block the user out of a better slot.
  - Do not add the external party as an attendee on a hold unless the user wants them to see it. A hold is usually the user's own reminder while they wait for a yes.
  - When placing several holds for one meeting (offering options), make it obvious they are alternatives, not four separate meetings.
- **Promotion:** a hold becomes a meeting only on a fresh yes. When it does, update the existing hold (retitle, mark busy, add attendees) rather than creating a duplicate, then delete the losing holds.
- **Expiry:** if a hold is not confirmed by the time it starts, clear it rather than leave it cluttering the calendar. Flag stale holds back to the user.

## Timezones
- Every proposal states the timezone. Every event stores an explicit timezone. No exceptions.
- Read the user's default timezone from their calendar. Do not assume it from locale.
- Cross-timezone meetings: show the time in both zones and name both ("15:00 London / 10:00 New York"). Each party reads their own zone.
- Aim for the overlap of both parties' working hours. Avoid asking anyone to take a call before 08:00 or after 18:00 their local time unless they have offered.
- Watch daylight-saving edges. The UK and US do not switch on the same dates, so London to New York is not always five hours. Trust the stored timezone, never a fixed offset.
- All-day and multi-day events count as busy for the whole local day in the user's zone.

## Duration defaults
- If the user does not say: 30 minutes for a call, 60 for a workshop, 15 for a quick sync. Offer, do not impose.
- Prefer 25 and 50 minute meetings over 30 and 60 where the user likes a built-in gap (Google calls these "speedy meetings").

## Proposing well
- Offer 2–3 options, not one and not ten. One reads as a demand, ten is a burden.
- Spread options across the window (a morning and an afternoon, or two different days), so a single clash does not kill all of them.
- Lead with the option that best fits the user's known pattern, and give a one-line reason for each.
- Name the meeting for the reader: purpose, not "Meeting". "Q3 roadmap: Sam + Priya" beats "Sync".

## What this skill cannot do (be honest)
- **It sees only the user's own calendar.** It cannot read an external attendee's free/busy. It finds times that work for the *user*, then proposes them, and the other party still confirms. That is why holds and proposals exist, and why the skill never claims a slot "works for everyone".
- Inside the same Google Workspace organisation, colleagues' free/busy may be visible. Use it if it is, but never assume it for anyone outside the org.
- It does not send email or chat on its own. Google's own invite email goes out when an event with attendees is created. Anything beyond that (a "does this time work?" note) needs an inbox skill or the user.
- Calendly through Zapier can create and cancel a booking, but cannot reschedule one. To move a Calendly meeting, cancel and rebook.
