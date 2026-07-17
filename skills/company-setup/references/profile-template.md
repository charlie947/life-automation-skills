# Profile template

Fill this with the user, one section at a time. Keep answers short and concrete. Leave anything unknown as `[NEEDS: …]` rather than guessing. Write the finished file as `company-profile.md`.

## Machine-readable block (top of the file)

Keep this compact so other skills can parse it fast.

```
name: <full name>
role: <job title>
company: <one line on what the company does>
timezone: <IANA zone, e.g. Europe/London>
working_hours: <e.g. 09:00-18:00 Mon-Fri>
task_system: <Notion | Airtable | none>
calendar: <Google Calendar | none>
crm: <Airtable | Notion | none>
accounting: <Xero | none>
meeting_notes: <Granola | Fireflies | none>
```

## Priorities (right now)

The most important section. Every triage, plan, and chase reads it. Push for specifics.

- The two or three things that matter most this quarter, and why.
- Active projects the user is pushing.
- Any hard deadline, with a date.

Update this often. Say "my priorities changed" to refresh it.

## VIPs

People whose messages jump the queue and whose chases need care.

- One line each: name, relationship (client, boss, report, partner), email or handle.
- Mark anyone where tone carries real cost, so the pack confirms before drafting to them.

## Working style

- **Focus blocks:** times the scheduler must keep clear.
- **Draft tone:** how replies should sound (for example warm, brief, plain, no jargon).
- **Sign-off:** the exact closing line the user uses.
- **Reply length:** short by default, or fuller.

## Stack

Confirm which tool each job routes to, so skills do not guess.

- Task system for captured tasks and action items.
- Calendar for scheduling.
- CRM for contacts.
- Accounting tool for receivables.
- Meeting-notes tool for transcripts.

## Guardrails

Hard limits the whole pack obeys.

- What to never do without asking (for example send anything, book over a focus block, merge or delete a contact, log an expense).
- Escalation appetite: how firm a chase may get.
- Anything the user wants kept fully manual.

## How other skills use this

Each skill reads `company-profile.md` at step 0:

- **inbox-executive-assistant, follow-up-chaser:** VIPs and Priorities to rank what matters.
- **meeting-scheduler:** working hours, timezone, focus blocks.
- **weekly-review, task-capture, standup-writer:** Priorities and the task system.
- **invoice-chaser, expense-wrangler:** the accounting tool and Guardrails.
- **doc-drafter, research-brief:** Voice and where to file.

If the file is missing, a skill runs on sensible defaults and suggests running `company-setup`.
