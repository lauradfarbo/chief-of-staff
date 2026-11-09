---
name: briefing
description: Produces the user's daily Chief of Staff briefing from their connected email, calendar, chat, tasks, CRM and meeting notes, in operator mode (what is slipping, what needs a decision, prep, numbers), growth mode (opportunities, quiet follow-ups, who to talk to), or both. Use when the user says "briefing", "where are we", "what's open", "what do I need to know today", "prep me for today", when a scheduled run fires, or when the day's briefing is requested by the tasks or onboard skills.
---

# Briefing

Produce a briefing the user can read in two minutes. It is built from real data, carries open items forward, and never sends anything.

## Before you start

1. **Find the profile.** Look for the `chief-of-staff` folder or project docs (project knowledge, connected ~~files, working folder, memory). Read `about-me.md`, `preferences.md`, `decisions.md` and `metrics.md`. If `about-me.md` or `preferences.md` is missing, stop and run the onboard skill.
2. **Read the mode** from `preferences.md`: `operator`, `growth` or `both`. If both, run the operator core first, then add the growth sections from `references/growth-mode.md` under a clear heading.
3. **Read the last two briefing notes** (`briefing-YYYY-MM-DD.md`) in the profile folder. List every item still open and how many days it has been open. If fewer than two exist, use what exists.
4. **Read the delivery place** (canvas, doc or message). Treat every ticked item as closed and record it as closed with today's date. Keep anything the user typed under "Notes (yours)" word for word.
5. **Keep carried-over item text identical** to how it first appeared, so the user's ticks still match. Change only the days-open count.

## Window

Look back to the time of the last briefing, not a fixed 24 hours. On a Monday that covers the weekend. If there is no previous briefing, look back 3 days.

## Gather

Use only what is connected. For each source, collect what the mode needs (see the mode references).

- ~~email: messages from always-surface people, threads waiting on the user, asks and deadlines, and documents that need routing to someone else.
- ~~chat: direct messages, mentions and threads waiting on the user.
- ~~calendar: the day or week, with attendees and what each meeting needs.
- Commitments: anything the user told someone they would deliver, from email, chat or ~~meeting notes, with its date.
- ~~task tracker: use the tasks skill. Items due in the window and relevant to the user.
- ~~crm and metrics: pull numbers named in `metrics.md` from their source. Never use a remembered or estimated number.
- ~~meeting notes: the user's own actions and decisions. Do not attribute remarks to other people.

**If a source is not connected or fails, say so in one line in that section and continue.** Do not skip silently.

## Core sections (every mode)

Every briefing, in every mode, includes these three sections first. The modes add to them; they never replace them.

1. **Needs a reply.** Email and chat together, one list. Messages since the last briefing that need an answer, come from an always-surface person, or mention an ask, an opportunity or a deadline. Per item: who, where (email or channel), one-line summary, action needed, link.
2. **Today's calendar.** Today's events (the week on a start-of-week briefing). Per meeting: attendees, likely agenda inferred from the title and context, and what the meeting needs from the user. Detailed prep for chosen meetings belongs to operator mode.
3. **Loose ends.** Search ~~email and ~~chat for the past 7 days, beyond the current window. Flag: promises the user made and has not kept, introductions they said they would make, follow-ups that went quiet, and external threads waiting on them. Name the person and the thread. Do not repeat anything already shown in Needs a reply or carried over in Drift.

If a source is missing, say so in the relevant section. If a section is empty, say so in one line.

## Output rules (all modes)

- One line per item: what, owner, date, link. Every item has an owner, a date and a link.
- Plain words. No emoji. No tables unless the user asked for them.
- Cap each list at the number in `preferences.md` (default 5). When there is more, show the top items, state the true count ("8 more"), and save the full list in the day's note. Never drop items silently.
- Rank by outcome impact first (the user's three outcomes in `about-me.md`), then due date.
- Overdue items say "overdue Nd".
- If nothing qualifies in a section, write one line saying so ("Nothing drifted."). Do not pad.
- Prefix "Looks done, confirm:" on an item the evidence says is finished. Keep it open until the user ticks it.
- Draft messages and long prep go into a separate doc, linked from the briefing. Do not put drafts in the briefing itself.
- Use the voice skill's rules for tone. No em dashes, no superlatives, no filler.

## Modes

Read the mode file before writing:
- `references/operator-mode.md` for operator and both.
- `references/growth-mode.md` for growth and both.

## After you finish

1. **Save the note.** Write `briefing-YYYY-MM-DD.md` to the profile folder. First line: the delivery link. Then list every open item with exact text, the date first opened and days open; items closed today; pending decisions; proposed tasks; and the numbers pulled with their source.
2. **Update the delivery place in place.** Create a new one only if none exists.
3. **Notify once.** One message to the user themselves, three lines at most:
   ```
   [Day] briefing is ready. 3 open, 1 decision, 2 handled.
   [link]
   ```
4. **If the delivery place fails**, write the briefing as a doc in the profile folder, send the link, and say once that the preferred place failed.
5. **Learn.** If the user ticked, ignored or rewrote items, log the pattern in `patterns.md` (see the skill-spotter skill). Ask at most one question per briefing, taken from the top of the Open list in `decisions.md`.

## Rules

- **Never send anything to anyone.** The only writes are the delivery place, the profile folder and a message to the user themselves.
- Numbers come from their source, never from memory.
- Never create a task from the briefing alone. Propose tasks as numbered questions (see the tasks skill); a proposal the user has not answered carries to the next briefing once, then drops.
- Read time stays under two minutes. If it would run longer, cut and count; do not shrink the text.
- Meeting notes and transcripts are for the user's own actions. Do not repeat what other people said about their colleagues, and do not store transcripts.
