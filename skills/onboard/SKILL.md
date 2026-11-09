---
name: onboard
description: Runs the first-run interview that sets up a personal Chief of Staff and creates the profile files every other chief-of-staff skill depends on. Use when the plugin is first installed, when the user says "set me up", "interview me", "onboard me", "recalibrate", "update my profile" or "my situation changed", or when any chief-of-staff skill finds no profile.
---

# Onboard

Interview the user once, build their profile, then prove it works with a real first result. Target length: about 10 minutes. Keep it conversational. The user is a busy person doing a favor to their future self.

## Find the profile first

Look for a folder or project docs named `chief-of-staff` holding `about-me.md` and `preferences.md`. Check, in order: project knowledge, a connected ~~files location, the current working folder, memory. If found, switch to **Recalibration** (below). If not found, run the full interview.

## Principles

- **Read before asking.** Inspect what is connected and draft answers from it. Ask only what cannot be found. Present drafts as "Here is what I found. What is wrong?"
- **Two questions at most per message.** Short, plain words. Offer 2 to 4 choices when a question has a natural set of answers.
- **Never get hung up on specific tools.** The user's stack is whatever they have. Map tools to categories (see CONNECTORS.md) and move on.
- **Skipping is fine.** If the user says skip or "not sure", write `unknown` and continue. Any skill can ask again at the moment it needs the answer.
- **Stay in scope.** Store work context only. Never store passwords, government IDs, financial account numbers or health details. Store third parties only as name, role and why they matter to the user's work.
- **Tell them the files are theirs.** Everything lands in plain files they can open and edit.

## Steps

### 1. Open (one message)

Say what will happen: about 10 minutes, you will look at what is connected first, ask only what you cannot find, and save everything as plain files they can edit. Say the interview can be paused and resumed.

### 2. Discover tools

For each category in CONNECTORS.md (~~email, ~~calendar, ~~chat, ~~task tracker, ~~crm, ~~meeting notes, ~~docs, ~~files), check whether a connected tool covers it. Report in one short list: connected, not connected. For missing categories, say work continues without them and the briefing will name the gap. Offer to search for a connector only if the user wants one.

### 3. Check for a career file

Before drafting anything, look for a **Career Asset File** (the output of the `career-foundation` skill from the career-skills family, usually kept in a Claude Project called something like "Career Builder"). Check project knowledge, uploads and the profile folder for a file titled "Career Asset File" or with sections named Snapshot, Timeline, Wins & Projects, Skills & Tools Inventory, Voice & Brand Notes and Open Threads.

**If found**, treat it as the richest source and read it first. Map it, then confirm with the user instead of asking:
- Snapshot (current focus, target audience) fills `about-me.md`: role, "what I want to be known for" and targets.
- Timeline gives the current role and company.
- Wins & Projects are proof points for growth mode (pitches, intros, points of view). Reference them by title; do not copy raw detail into the profile.
- Voice & Brand Notes seed the Voice section of `preferences.md` and the banned-phrases list.
- Open Threads that mention follow-ups or unconfirmed items go to the Open list in `decisions.md`.
- Skip every interview question the file already answers. Use the career file's wording; do not paraphrase it into something new.
- Never edit the career file. It belongs to the career-foundation skill.

**If not found**, say once, in a sentence: "For the richest setup, build your career file first with the career-skills family (a Career Builder project), then run this setup in the same project. Want to do that first, or continue without it?" Respect the answer. If they continue, run the interview as written and do not raise it again. The career file is recommended, not required.

### 4. Read-first draft

With the user's permission for each source, draft what you can:
- **Role and company:** from email signature, calendar title patterns, profile pages.
- **Rhythm:** recurring meetings from ~~calendar. Group them (team, 1:1, external, review).
- **Key people:** the most frequent contacts and any who the user replies to fastest.
- **Voice:** ask first, then read about 10 recent sent messages. Note length, greeting and sign-off habits, formality, and phrases they repeat.

Show the draft and ask for corrections. Do not save anything yet.

### 5. Interview rounds

Use `references/interview-guide.md` for the question bank. Run the rounds in order and skip any question already answered by the draft.

- **Round 1, role and outcomes:** what they own, top 3 outcomes for this quarter, who must always surface, what they are saying no to.
- **Round 2, how they work:** meetings that need prep, numbers they check and where they come from, how much to do alone versus ask first, what they hate.
- **Round 3, setup:** tool per category, where the briefing should land, when it runs, size limits, and the mode question below.
- **Voice and rules:** confirm the voice notes, seed the banned-patterns list (see voice skill), and ask for any additions.

### 6. The mode question

Ask this exactly, as a single choice question. Do not abbreviate it.

> Which of these is your bigger need right now?
> **A. Keeping things on track.** Your briefing focuses on what is slipping, what needs your decision, and what is coming up, including prep for meetings and the numbers you watch.
> **B. Finding what to pursue.** Your briefing focuses on opportunities, follow-ups that have gone quiet, and who to talk to next.
> You can switch at any time, or run both.

Save the answer as `mode: operator` (A), `mode: growth` (B) or `mode: both`.

### 7. Playback

Summarize the profile in about half a page: role, three outcomes, rhythm, tools, mode, voice notes, rules. Ask "What is wrong or missing?" Apply corrections. Then save.

### 8. Save

Create the five files from `references/templates/` in the profile folder: `about-me.md`, `preferences.md`, `decisions.md`, `metrics.md`, `patterns.md`. Ask once where to save them if the location is not obvious (a ~~files folder, project docs or the working folder). Record the location in `preferences.md`.

### 9. First win (same session)

Do two real things before ending: run the briefing once, and either draft one message in their voice or list their open tasks. Ask one question: "Anything in that you would have wanted differently?" Log the answer in `patterns.md`.

### 10. Scheduling

If a scheduling capability is available, offer to run the briefing on the days and time they chose. If not, tell them to say "briefing" whenever they want it.

## Recalibration

Run when the user asks, or when the profile is older than about three months and the user starts a session. Open each file, show the three or four lines most likely to have changed (outcomes, key people, mode, tools), and ask "What changed?" Update only what changed. Keep it under five minutes.

## Gaps later

If another skill hits an `unknown` field it needs, it asks that one question, uses the answer and saves it. Do not re-run the interview for that.
