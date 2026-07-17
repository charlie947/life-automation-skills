# Life Automation Skills

A pack of 12 doing-skills plus the `company-setup` keystone, 13 [Agent Skills](https://agentskills.io) to install in all, that hand the repetitive admin of a working week to Claude: inbox, calendar, meetings, follow-ups, planning, and the money jobs, so a busy professional spends their day on the work only they can do.

They share one brain. A keystone skill, `company-setup`, interviews you once and writes a `company-profile.md` (your priorities, VIPs, working hours, tone, tools) that every other skill reads at step 0. So they work to your context, not to generic defaults.

Each skill is a plain `SKILL.md`. Install what you want, leave the rest.

## Install

With the [`skills` CLI](https://github.com/vercel-labs/skills):

```bash
npx skills add charlie947/life-automation-skills          # the whole pack
npx skills add charlie947/life-automation-skills/inbox-executive-assistant   # one skill
```

Or drop any `skills/<name>/` folder into your agent's skills directory.

## The pack

Run `company-setup` first. Then the twelve doing-skills, flagship first. Skills 1–4 are the least-served by existing public skills (few good equivalents also surface meetings). 5–12 round out the working week.

| # | Skill | What it owns | Connectors |
|---|-------|--------------|------------|
| ★ | **company-setup** (keystone) | Interview once, write the shared `company-profile.md` every skill reads | none |
| 1 | **inbox-executive-assistant** | Triage Gmail → prioritised brief + reply drafts + today's meetings | Gmail, Calendar |
| 2 | meeting-scheduler | Find slots, book, reschedule, send holds | Calendar |
| 3 | meeting-notes | Capture + summarise a meeting, route action items | Granola/Fireflies, Notion |
| 4 | follow-up-chaser | Find threads awaiting a reply, draft the nudge | Gmail, Calendar |
| 5 | weekly-review | Turn the week's calendar + inbox into a plan | Calendar, Gmail, Notion |
| 6 | task-capture | Pull tasks out of email/chat, route them to your list | Gmail/Slack, Notion/Airtable |
| 7 | research-brief | Multi-source brief on a topic, cited, filed | Web, Drive/Notion |
| 8 | standup-writer | Draft your status/standup from what you actually did | Slack, Calendar, Notion |
| 9 | doc-drafter | First-draft a doc or contract from a brief | PandaDoc, Drive |
| 10 | expense-wrangler | Pull receipts from email, log them | Gmail, Airtable/Sheets |
| 11 | crm-hygiene | Dedupe, enrich, and tidy contact records | Airtable/Notion |
| 12 | invoice-chaser | Spot overdue receivables, draft the chase | Xero, Gmail |

## Safety by default

This pack is on-demand, human-in-the-loop assistance: it drafts and proposes, you approve and send. It is not background or autonomous automation, and nothing runs without you.

These skills act on your real accounts, so every one ships **least-privilege, draft-only, confirm-before-act**:

- **Nothing sends or deletes on its own.** Replies land in Drafts. You hit send. Destructive actions are proposed, then done only on your yes.
- **Inbound content is treated as untrusted.** Emails and documents can carry hidden instructions (prompt injection). These skills follow *you*, never the content they're reading, and never auto-open links or images inside a message.
- **Each skill asks for the minimum connectors it needs**, nothing more.

## What this is not

No personal data, no private pipelines, no one's "secret sauce". These are clean, generic skills built from how these jobs are done well. Bring your own accounts.

## Licence

MIT. See [LICENSE](LICENSE).
