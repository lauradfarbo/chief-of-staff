---
name: skill-spotter
description: Notices recurring work and repeated corrections in the user's requests and offers to build a reusable skill for them together. Use when the user says "I keep asking you to", "this is a recurring task", "can we make this a skill", "build a skill for this", when the same multi-step request has come up three times, or when the briefing reviews the patterns log.
---

# Skill spotter

Turn repeat work into reusable skills, with the user's agreement. Offer rarely. Build only on a yes.

## Find the profile

Read `patterns.md` and `preferences.md` from the `chief-of-staff` profile folder or project docs. If there is no profile, run the onboard skill first.

## Log patterns as you work

Add a row to `patterns.md` whenever any of these happen:
- **Repeat request:** the user asks for the same kind of multi-step job again. Match by purpose, not exact words ("prep the board update", "summarize the sales call", "clean the sign-up list").
- **Repeated correction:** the user changes the same thing in your output twice.
- **Ignored briefing items:** the user leaves the same type of item unticked for a week or more.
- **Recurring calendar item with the same prep** each time.

Keep rows short: request, times seen, last seen. Do not store content, only the shape of the job.

## When to offer

Offer when one of these is true:
- The same job has come up **three times**.
- The user said it is recurring ("every Monday", "each month").
- The user says "I keep having to...".

**Offer limits:**
- At most **one offer per week**.
- Never offer in the middle of a task. Offer after you deliver the result.
- If the user declines, record it in `patterns.md` and do not offer that job again for 60 days unless they raise it.
- Never offer for sensitive or one-off work.

**Offer wording**, as a question and specific:
"You have asked me to [job] three times now. Want to build a skill for it together? It would take about 10 minutes, and next time you could just say [short trigger phrase]."

## Co-build flow (only after a yes)

1. **Trigger.** Ask: what would you say to start this? What else might trigger it?
2. **Steps.** Walk through the last real instance. Ask: what did I do, in order? What did you change?
3. **Inputs.** What do I need each time, and where does it live? (Tools use category names.)
4. **Output.** What does the finished result look like, and where does it go?
5. **Rules.** What must I always do? What must I never do? What needs your yes?
6. **Draft.** Write a short skill: a clear description with trigger phrases, numbered steps, output shape, and a Rules section. Use the user's wording. Keep it under about 400 words unless the job needs more.
7. **Test.** Run it on a real past example. Show the result. Ask what is wrong. Fix it.
8. **Save.** Offer to save it to the user's skills (if the environment supports saving skills) or to the profile folder as `skills-drafted/[name].md`. Note it in `patterns.md`.

If the user has the skill-creator available, offer it for testing and refinement.

## Rules

- Never build a skill without the user's yes.
- Never put credentials, personal data about others or transcript text into a skill.
- Keep skills in plain language the user can read and edit.
