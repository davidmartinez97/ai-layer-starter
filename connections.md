# Connections: the posture table

> A connector is the plug between the AI and one of your tools. Every plug gets one row: what it may read, what it may write, and the constraint. The table is the policy. Where a plug has no write capability, that is the enforcement; where it has one, the rule lives in the skill that uses it and a person checks the output before it is shared. Owner: [name]. Last verified: [date].

| Tool | Read | Write | Constraint |
|---|---|---|---|
| [Wiki, e.g. Notion or Confluence] | yes | yes, documents only | Never customer or personal data into a page the whole company can see |
| [Chat, e.g. Slack or Teams] | yes | yes, own channels | Never private data in a public channel |
| [Project tracker, e.g. Linear or Jira] | yes | no, propose only | The agent proposes in chat; a person applies in the tracker |
| [CRM] | yes | no | Read for context only |
| [Mail and calendar] | yes, own mailbox | draft only | Nothing is sent without the person pressing send |
| [Product database] | [yes or no] | [no, or yes with every change reviewed] | A schema change is reviewed by a person every time |

## How to fill the first row

1. Pick the one tool whose content answers most questions (usually the wiki).
2. Ask IT for read-only access for the assistant, with the same permissions the person has, not more.
3. Write the row. Leave write as "no" until a skill needs it, and then write the constraint before switching it on.

## Rules

- Start every plug read-only.
- An agent that reads text typed by other people (tickets, mail, forms) never gets write access to a system of record in the same loop. It proposes; a person applies.
- Re-verify this table whenever a tool is added, removed or re-scoped, and at least every 90 days.
