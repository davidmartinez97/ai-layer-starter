---
name: meeting-notes
description: Turn raw meeting notes or a transcript into a short decision record, with decisions, action items with owners and due dates, open questions and parking-lot items. Works for any meeting type.
status: main
owner: [name]
last_verified: [date]
validated: [date, after three real runs read by the owner and one try by a colleague outside the team]
---

# Meeting notes: raw input to a decision record

Good meeting notes are a decision record, not a transcript. This skill takes whatever was captured (shorthand, a transcript, a voice-memo dump) and returns the half page people actually read.

## Trigger phrases

- "Clean up these notes" · "write up the meeting" · "structure these notes"
- "Summarize this transcript" · "what did we decide?" · "pull out the action items"
- The user pastes raw notes or a transcript without saying anything

## Step 0: privacy gate and context

If the notes contain personal data about customers, candidates, employees or anyone outside the company, anonymize first: replace names with role tokens such as [customer] or [candidate]; drop emails and phone numbers. Do this before anything else and do not ask permission to follow the data-protection rules in `company.md`.

Then confirm quickly: the meeting type (sync, client call, review, planning, interview debrief), the date and attendees if not in the notes, and, for very long notes, whether a full summary or only decisions and actions is wanted.

## Step 1: extract

Identify decisions (things settled or agreed), action items (a task with a named owner; mark [OWNER TBD] if genuinely unclear), open questions (raised, not resolved), key context (two to five load-bearing points) and parking-lot items (deferred on purpose).

## Step 2: write, using this template

```
# Meeting notes: [title or topic]
Date: [date]  Type: [type]  Attendees: [names or roles]

## Decisions
- [one sentence per decision; who decided if relevant]

## Action items
| # | Action | Owner | Due |
|---|---|---|---|
| 1 | [what needs to happen] | [name or OWNER TBD] | [date or "next sync"] |

## Open questions
- [question] (who answers, by when, if known)

## Key context
- [two to five points: the why behind decisions, constraints, background]

## Parking lot
- [deferred items and what would bring them back]
```

Quality bar: every action has an owner, even if [OWNER TBD]. Every decision is a sentence, not a noun. Open questions end with a question mark. A 20-minute sync fits in ten lines; do not pad.

## Step 3: offer to save

Offer once: "Want me to save this to [the wiki]? Tell me where it belongs." Save only after confirmation, in the place the person names.

## Notes for the assistant

- Extract, do not transcribe.
- Infer owners from context ("Anna said she would follow up" makes Anna the owner); flag real ambiguity instead of guessing.
- Match length to the meeting's weight.
- The privacy gate is not optional.
