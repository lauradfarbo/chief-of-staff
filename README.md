# Chief of Staff

A personal Chief of Staff for busy leaders, built as a Claude plugin. It interviews you once, then runs a daily briefing, handles your tasks, writes in your voice and learns how you work. It does not assume any particular tools. It uses whatever you have connected.

## Get started

1. Install the plugin.
2. Connect the tools you use (email, calendar, chat, task tracker, CRM, meeting notes, docs, files). None are required.
3. Say **"set me up"**. Claude interviews you for about 10 minutes, reading what it can from your connected tools first and asking only what it cannot find. It then runs your first briefing in the same session.

Your profile is saved as five plain files you can open and edit.

## What is in it

| Skill | What it does |
|---|---|
| **onboard** | The first-run interview. Builds your profile, picks your briefing mode, and recalibrates every few months. |
| **briefing** | Your daily brief. *Operator mode* covers what is slipping, what needs your decision, meeting prep and your numbers. *Growth mode* covers inbox, loose ends, signals, an opportunity radar and one thing to do. Run either or both. |
| **tasks** | Shows what is due and creates tasks only after you confirm project, assignee and date. |
| **voice** | Drafts and edits in your voice and removes common signs of AI writing. |
| **skill-spotter** | Notices work you repeat and offers, at most once a week, to build a skill for it with you. |
| **leadership-observation** | Optional, off by default. One small note a week on your own communication habits, from recorded internal meetings. |

## How it learns

- It logs your corrections and repeat requests in `patterns.md`.
- A pattern becomes a preference only after it repeats, and it shows you the exact change first.
- It asks at most one question per briefing.
- It offers to recalibrate your profile every few months.

## Your profile files

| File | Holds |
|---|---|
| `about-me.md` | Your role, three outcomes, key people, rhythm, what you are saying no to |
| `preferences.md` | Mode, tools, autonomy, format, voice and banned patterns |
| `decisions.md` | Open questions, decisions and rules you have set |
| `metrics.md` | Numbers you watch, with their source |
| `patterns.md` | The learning log |

## Principles

- **Never sends anything.** It drafts and proposes. You send.
- **Confirms before it creates or assigns anything.**
- **Numbers come from their source,** never from memory.
- **Says so when a source is missing,** and when there is nothing to report.
- **Your data stays in your files.** It stores work context only: no passwords, government IDs, financial account numbers or health details.

## Optional: leadership notes

Say "start leadership notes" to turn on a weekly observation about your own speech in recorded internal meetings. It never uses 1:1s or external meetings, never names or quotes other people, and sends only to you. Check that recording and analyzing meetings is allowed where you work. Say "stop leadership notes" any time.

## Customize

Everything is plain text. Edit the skills to change behavior, or ask Claude to. Tool references use `~~category` placeholders (see `CONNECTORS.md`) so the plugin adapts to your stack.

## License

MIT. See `LICENSE`.
