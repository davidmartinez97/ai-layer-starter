# The gate

> A check before anything is saved or shared: a program looks for secrets and personal data, then a named person says yes. The gate can start as one person and a checklist. Owner: [name]. Last verified: [date].

## Who approves what

| Scope | What it is | Who says yes |
|---|---|---|
| Personal | A skill or page only its author uses | The author, after the checklist |
| Team | Used by one team | The team lead |
| Company | Used by everyone | [the AI owner or a two-person group], after the checklist and a trial in one team |

## The checklist before anything is saved or shared

1. **Secrets.** No passwords, API keys, tokens or connection strings anywhere in the text. If one is found, it is removed before saving and rotated, because a secret in history cannot be unwritten.
2. **Personal data.** No customer, patient, candidate or employee names, emails or phone numbers in anything the whole company can see. Anonymize with role tokens.
3. **Claims.** Every number has a source. Nothing is invented.
4. **External.** Nothing leaves the company (an email, a post, a message to a customer) without a person pressing send.
5. **Docs.** The changelog has a line. The index still points to the right place. The owner and date are updated.

## The lifecycle of a skill or page

draft, then in review, then approved, then published, then deprecated. Every published item has an owner and a last-verified date. When the date is older than 90 days, the owner is asked "still accurate?" and the item is marked as unverified until they answer.

## When the gate fires

On any of: "commit this", "save this", "publish this", "share this", "ship it", "send it". In a tool that supports it, the gate runs automatically before the save; otherwise the person runs the checklist by hand. Either way it runs before, never after.
