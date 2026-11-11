---
name: today
description: Every weekday morning, one page. What is on today, what needs a yes from you, what is overdue, what was decided yesterday that affects you. Reads the calendar, the open action items and the decision log. Proposes; changes nothing.
status: dev
owner: [name]
last_verified: [date]
validated: [not yet; run it by name for a week first]
schedule: weekdays 07:30, or whenever someone types "today"
---

# Today: the morning page

The example of a routine: a skill that runs on a schedule, reads the layer, and leaves one page for a person to act on. It never acts itself.

## Trigger phrases

- "today" · "what's on today?" · "morning page" · "what needs me?"
- On a schedule, where your assistant supports one (a scheduled task, a routine, a cron job). Until then, the person types "today".

## What it reads, in this order

1. `company.md`, then `knowledge/index.md` for the live pages it needs.
2. Today's calendar, through the connector in `connections.md`, read only; or a pasted list, see `examples/a-synthetic-day.md`.
3. The open action items from the last meeting notes, with owners and due dates.
4. `decisions.md`: the records of the last two days.

## Step 0: privacy gate

The names of customers, candidates or anyone outside the company become role tokens. The page may be read on a phone, on a train.

## Step 1: build the page

```
# Today · [date]

## On today
- [time] · [meeting] · [what to have read first; link]

## Needs a yes from you
- [proposal, one line] · [why, with the source] · reply yes or no

## Overdue, or overtaken
- [action] · owner [name] · was due [date] · [or: superseded by the decision of [date]]

## Decided yesterday, affects you
- [decision, one sentence] · [who decided] · [link to the record]

## Seen, nothing to do
- [what the assistant read and judged not worth your time, one line each]
```

Quality bar: the page fits one phone screen. Every line has a link or a source. "Needs a yes" holds proposals only; nothing in it has happened yet.

## Step 2: deliver, do not act

Post the page where the person reads in the morning: their channel, a mail draft, the top of a page. The person gives the yes; the skill that owns the proposal then does the work.

## Notes for the assistant

- Propose, never apply. If the page is empty, say so in one line; do not invent.
- Read the layer before the calendar. The calendar says what; the layer says why.
- The first week, the owner reads the page every day and corrects it. That is the validation.
