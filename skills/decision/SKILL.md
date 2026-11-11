---
name: decision
description: Turn one line in chat ("we decided X", "decision: X") into a decision record with every field, check it against the rules, and file it in decisions.md after the person who decided says yes. Names who must be told.
status: dev
owner: [name]
last_verified: [date]
validated: [not yet; call it by name until three real runs]
---

# Decision: one chat line to one record

A decision said in a chat or a call is gone by Friday unless it is written. This skill takes one line and returns the record, with the fields `decisions.md` requires, and files it only after the person who decided says yes.

## Trigger phrases

- "decision: …" · "we decided …" · "we agreed …" · "log this decision"
- While it is `dev`, call it by name: "run decision on: …"

## Step 0: privacy gate and context

Replace the names of customers, candidates or anyone outside the company with role tokens such as [customer A]. Read `company.md` and the rules it links to. Read the last ten records in `decisions.md`.

## Step 1: draft the record

Fill every field from the line and the context. What cannot be inferred is asked once, in one message: the question it answered, the alternatives rejected, the source.

## Step 2: check it against the rules

- Does it follow a rule, change one, or break one? Name the rule and its owner.
- If it breaks a rule: impact **critical**. The record is not filed until the rule's owner approves; say so and name them.
- Is there an earlier decision on the same subject? Mark it superseded in the draft and link both ways.

## Step 3: propose, then file

Show the record. Ask once: "File this in `decisions.md` and tell [the affected people]?" File only on a yes. Then list who must be told, one line each, ready to paste.

## Output template

```
## [date] · [the decision in one sentence]
- Decision: …
- The question it answers: …
- Alternatives rejected, and why: …
- The rule it follows, or changes: … (owner: …) · impact: normal or critical
- Who decided: …
- Source: [link]
- Who is affected: … · told: [date]
- Status: active · supersedes: [link, if any]
```

## Notes for the assistant

- One line in, one record out. No essay.
- Never file without the yes. Never delete an earlier record; supersede it.
- If the line is not a decision (a wish, a question, a task), say so and offer an action item or the meeting-notes skill instead.
