# Decisions

> The decision log: one place, one record per decision, every record with its source. Written by the person who made the decision, or proposed by a skill from a meeting or a chat line and confirmed by that person. Nothing is deleted; a decision that changes is marked superseded and the new record points to it. Owner: [name]. Last verified: [date].

## The record

Every decision has these fields. A record without a source or without the person who decided is a draft, not a decision.

- **Decision:** one sentence, in the words of the person who made it.
- **Date:** YYYY-MM-DD.
- **The question it answers:** what was open before.
- **Alternatives rejected, and why.**
- **The rule it follows, or changes:** the line in `company.md` or the linked page. If it breaks a rule, impact is critical, and the rule's owner approves before it is filed.
- **Who decided:** name and role.
- **Source:** the link to the meeting notes, the chat message or the document.
- **Who is affected:** the people or teams that must know; they are told the same day.
- **Status:** active, or superseded by [link].

## Example (synthetic)

## 2026-11-10 · Customer A gets 15 percent on renewal, as a named exception

- **Decision:** Customer A renews at 15 percent, until 2027-12-31, as a named exception; everyone else stays at the 10 percent limit.
- **Date:** 2026-11-10
- **The question it answers:** Can we go above the 10 percent limit to keep customer A?
- **Alternatives rejected, and why:** a two-year contract at 10 percent (decided 2026-11-04; the customer declined it); no change (usage still falling after ticket T-398; risk of losing the account).
- **The rule it follows, or changes:** "No discount above 10 percent without finance", on [the pricing page]. This record changes it: a named exception. Impact: critical. Finance, the page's owner, approved.
- **Who decided:** [the CEO], with [the finance lead].
- **Source:** [link to the meeting notes of 2026-11-10].
- **Who is affected:** the account owner, finance, the support lead. Told 2026-11-10 in their channels.
- **Status:** active. Supersedes: the two-year option of 2026-11-04, [link].

## Rules

- Written before the work continues, not at the end of the week.
- A decision said in a meeting or a chat is proposed by a skill (`skills/meeting-notes`, `skills/decision`) and confirmed by the person who made it. Nothing is filed alone.
- Every record says where it came from.
- Superseded, never deleted. The history is the point.
- The log is a live page: this file in a small company; a database in the wiki once it holds more than a screen of records. The index points to it either way.
