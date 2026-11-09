---
name: tasks
description: Lists what is due or overdue and creates tasks in the user's task tracker, always confirming before it creates or assigns anything. Use when the user says "what's due", "what's due today", "what's on this week", "create a task", "assign this to", "add a to-do", "create 1 and 3" in reply to a briefing proposal, or when the briefing needs task items.
---

# Tasks

The user may have turned off notifications from their task tracker because it was too noisy. This skill is their view of it, so show what matters and nothing else. Assigning a task notifies the assignee, so creation always needs the user's yes.

## Find the profile

Read `preferences.md` from the `chief-of-staff` profile folder or project docs. It names the ~~task tracker and the projects to include. If no tracker is connected, say so, offer to keep a simple list in the profile folder, and stop.

## What is due

Triggered by "what's due", "what's due today", "what's on this week" or the briefing.

**Include:**
- Tasks assigned to the user that are due in the window or overdue.
- Tasks the user created for someone else that are overdue.
- Only tasks in the projects named in `preferences.md`. If none are named, use all the user's assigned tasks and ask once which projects to keep. Save the answer.

**Leave out:** subtasks (unless assigned to the user and due), comments, mentions, follows, new-task notices and project updates.

**Window:** the start of the week asks for tasks due this week. Other days ask for due today and overdue. Use the user's own rhythm if `preferences.md` says otherwise.

**Order and size.** Show up to the list cap (default 5; the user can change it in `preferences.md`). Choose the items to show in this order:
1. Overdue, oldest first.
2. Tasks the user promised to someone else.
3. Tasks that block someone else.
4. Everything else, by due date.

**Never hide the true count.** After the shown items, add one line with the real number remaining and its split by day, for example: "8 more due this week: Tue 2, Wed 3, Fri 3. Say 'show all' for the list." Save the full list in the day's briefing note. When more than the cap are overdue by over 14 days, collapse them into one line: "N overdue more than 14 days. Want the list?"

**Line format:** `Task. Project. Due date or "overdue Nd". Link.`

If nothing qualifies: "Nothing due today."

## Creating a task

Only when the user asks, or answers a briefing proposal ("create 1 and 3"). Never create a task on your own.

1. **Project.** Use the one the user or the proposal named. If none, suggest the likeliest from recent tasks and ask. If unsure, ask.
2. **Assignee.** Match the name against the tracker's users. If two or more match, or none, ask. Never guess. "Me" means the user.
3. **Due date.** Turn it into a date in the user's time zone and say the weekday, for example "Fri, Nov 13". If the day is ambiguous, ask. "Friday" said on a Friday is ambiguous.
4. **Confirm.** Restate in one line and wait for yes:
   `Create "Send vendor contract to Sam" in [Project], assign Sam, due Fri, Nov 13?`
   Skip the wait only when the user is answering a briefing proposal that already named all three, or has said to skip confirmations (see Rules).
5. **Check for a duplicate.** Search the project for an open task with the same title and assignee. If one exists, give its link and do not create another.
6. **Create.** The title starts with a verb and is plain. The description is one or two lines of context plus a link to the source (the message, thread or doc). Set project, assignee and due date. Add no followers, tags, subtasks or comments unless asked.
7. **Return the link:** `Created: "Send vendor contract to Sam". Sam, due Fri, Nov 13. [link]`
8. **Log it.** Put a line in Handled in the next briefing.

For "create 1 and 3", do each in turn and return both links.

If creation fails, say what happened. Search before retrying so you do not create a duplicate.

## Proposing tasks in the briefing

Do not propose a ticket for everything. Propose a task only when:
- someone other than the user has to act,
- the user promised a date to someone else, or
- a dependency would stall if it were dropped.

Never propose a task for the user's own routine to-dos. Source proposals from chat, email and meeting notes. Three proposals at most per briefing. Write each as a question:

`1. Create "X" in [Project], assign Y, due Fri, Nov 13? Link.`

## Editing and closing

Only when the user asks, in that message. If more than one task matches, ask which. Never delete a task. Never comment on a task.

## Rules

- Never create a task unprompted.
- Never comment, tag or add followers.
- Confirm project, assignee and due date before creating.
- If the user wants to skip the confirmation once all three are given, save that rule to `decisions.md` and `preferences.md` only after they say so.
- Log repeat task requests in `patterns.md` for the skill-spotter.
