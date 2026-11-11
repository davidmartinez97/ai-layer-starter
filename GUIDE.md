# The guide: how to start, one layer at a time

> The method behind the folder. Five layers, in order, each one on the one before. The first move for each is small; the pace is yours. Owner: [name]. Last verified: [date].

## Before the first layer: make the assistant read the folder

Pick the assistant you already use. The files are plain text; nothing here needs an install.

| Assistant | What to do |
|---|---|
| Any chat (Claude, ChatGPT, Gemini, Copilot) | Paste `company.md` at the start of the chat. That is layer one working, today. |
| A Claude Project or a ChatGPT Project | Put `company.md` in the project's instructions. Add the other files as project files. |
| Claude Code or the Claude desktop app | Open the folder. `CLAUDE.md` is read at the start of every session. For the skills to fire on their own, copy `skills/` to `.claude/skills/` inside the folder. |
| Codex and other agents that read a folder | Copy `CLAUDE.md` to `AGENTS.md`. The skill files are the open Agent Skills format; put them where your agent looks for skills. |
| A copilot inside a tool (CRM, wiki, support desk) | Its instructions field gets the ten lines of `company.md`. |

The test: ask "what do we sell, and who owns the sales process?" If the answer comes from your page, with the owner's name, the assistant has read it.

## Layer 1: context. The one page and the map.

What it is: the facts every chat should know, and a map of where the real documents are. The assistant reads a short map first and fetches the rest by link when a question needs it. It does not read the whole wiki.

First move:

1. Fill `company.md`. Ten lines, facts that do not change this quarter, links instead of copies. One hour.
2. Fill `knowledge/index.md`: one row per document that matters, each with the exact link, an owner and a date. Mark each row fixed (changes by agreement, with a review) or live (edited in place, any day).
3. Load the folder, as above.

The rule: links, not copies. A copy drifts within days; a link is right at question time.

Done when: a new colleague's first chat answers a company question with the right source attached.

## Layer 2: data. One source, read only.

What it is: the numbers in one place anyone can ask, with the definition next to each field and an owner per table. The sources stay where they are.

First move:

1. Pick the one system whose content answers most questions. Usually the wiki or the tracker.
2. Ask IT for read-only access for the assistant, with the permissions the person has, not more. One hour with IT.
3. Write the row in `connections.md`. Write stays "no" until a skill needs it.
4. If you have a database or a warehouse: one table from one source, synced, with its definitions written next to it. Define, check, test, then let people read from it.

The rule: an agent starts with no write access. It proposes; a person applies.

Done when: someone asks the assistant about a ticket or a customer and gets the live status with a link, without a seat in that tool.

## Layer 3: intelligence. Decisions written.

What it is: what the company knows that is in no system: decisions, the reasons, what was tried. Captured where it is said, in meetings and chat, and written to one shared place with its source.

First move:

1. Run `skills/meeting-notes` on your next meeting. Every action has an owner; every decision is a sentence.
2. Write the first decision in `decisions.md`, with all its fields. `skills/decision` does it from one line in chat.
3. Open one channel where anyone can ask the layer a question and get an answer with the source linked. Read only.

The rule: agents read everything; people decide what is worth knowing. A decision is written with its source before the work continues. Nothing is deleted; it is superseded.

Done when: the decisions made this week are on the page by the evening, each with a source link, and someone found one there instead of asking.

## Layer 4: automate. One skill, one schedule.

What it is: the repeatable work, as skills with owners, some on a schedule. The rules live in the layer; the automation only reads them.

First move:

1. Fill `task-audit.md` in an hour. The first skill is the task that is daily, written down and repeatable.
2. Write it: copy `skills/meeting-notes/SKILL.md`, replace the steps, put your name and today's date at the top. Status `dev`: it runs when called by name until it is validated.
3. Put one skill on a schedule. `skills/today` is the example: every weekday morning, one page, proposals only.
4. Validate: three real runs, the owner reads the outputs, one colleague outside the team tries it. Then `main`.

The rule: the automation proposes; a person applies. It never had write access to the system of record.

Done when: one routine ran for a week without anyone touching it, and its owner read every output.

## Layer 5: build. With what you got back.

What it is: the tools, pages and agents you build on top, once the layers below feed them. Search first, reuse second, build last.

First move:

1. Before building anything, search the skills you have. A skill that exists is reused, not rebuilt.
2. The first build reads the layer: the one page, the index, the rules and, if you have one, the design system.
3. Every build has an owner, a last-verified date and a line in the changelog.

The rule: build on what the layers below already know. A tool that keeps its own copy of the company is one more copy to drift.

Done when: a person outside your team uses something you built without you in the room.

## The gate, from day one

`gate.md` is not a layer; it runs across all five. One named person reads every output before it is shared. The checklist runs before anything is saved, never after. Start there, on the first day, when it is one person and a checklist.

## Three measures

Not time saved; that comes later and needs a baseline. Three things you can count from the first month:

| Measure | The question | Where to look |
|---|---|---|
| Away from the desk | Can it run a weekend from your phone? | A question answered from the layer, source attached, with nobody at a desk |
| Tasks automated | Against your own audit: how many rows have a skill, and how many of those are `main`? | `task-audit.md` |
| Knowledge captured | How many decisions were written this week, each with a source? | `decisions.md` |

## Inside an organization: three things to add

The layer is not adopted by itself. Add:

1. **A place to ask.** One channel where anyone asks the layer a question in plain words. The answers show people what it knows.
2. **A weekly hour.** People bring one real task. One becomes a skill, with an owner.
3. **A nudge.** When a page or a skill passes its last-verified date, the owner is asked "still accurate?". `gate.md` has the rule; a calendar reminder is enough to start.

## How to keep the folder true

- Every file has an owner and a last-verified date. Re-verify every 90 days.
- Every change gets a line in `CHANGELOG.md`.
- When the folder and a linked document disagree, the document wins, and the folder is fixed.
- A fact in neither: the assistant asks. It does not invent.
