# AI layer starter

A folder, not a product. Ten files that give any AI assistant the three things it does not have about your company: what you know, how you do things, and who may touch what. Built from a layer that runs daily at a mid-size company; stripped of everything specific to it.

Works with any assistant that can read a text file: Claude (Projects, Cowork, Claude Code), ChatGPT (custom instructions or company knowledge), Copilot, or whatever comes next. The skill file format is the open Agent Skills standard, read by Claude, OpenAI's Codex and others.

## The files

| File | What it is | Your first move |
|---|---|---|
| [company.md](company.md) | The one page every chat should read first | Fill in the ten lines. Point to documents, never copy them. |
| [knowledge/index.md](knowledge/index.md) | The map: what you need, which document, who owns it | Add one row per document that matters. Owner and date on every row. |
| [task-audit.md](task-audit.md) | The table that decides which task becomes a skill first | Fill it in an hour |
| [skills/README.md](skills/README.md) | How to write a skill, and the two tiers | Read before writing your first skill |
| [skills/meeting-notes/SKILL.md](skills/meeting-notes/SKILL.md) | A complete, working skill to copy | Run it on your next meeting's notes |
| [connections.md](connections.md) | The posture table: what each connected tool may read and write | Fill in one row for one tool, read-only |
| [gate.md](gate.md) | The check before anything is saved or shared, and who approves what | Name the person. Start there. |
| [CLAUDE.md](CLAUDE.md) | The router, for assistants that read a folder (Claude Code, Cowork) | Leave as is |
| [CHANGELOG.md](CHANGELOG.md) | What changed and when | Add a line every time you change a file |

## The five moves, in order

1. **Write the one page.** `company.md`, ten lines. Paste it at the start of every chat until you have somewhere better to keep it (a Project's instructions, a desktop assistant's folder).
2. **The task audit.** Fill `task-audit.md` in an hour. Pick the one task that is daily, repeatable and already written down.
3. **Make it a skill.** Copy `skills/meeting-notes/SKILL.md`, replace the steps with yours, put your name and today's date at the top.
4. **Connect one system, read-only.** One hour with IT. Write the row in `connections.md`.
5. **Add the gate.** `gate.md`: one named person who reads every output before it is shared, and the checklist for anything saved.

First checkpoint: the first chat that already knows your company. A layer a week, not a platform a year.

## Rules that came from the failures

- Keep the system of record where it is. The layer holds pointers, not copies. Copies drift within days.
- Fetch a document by its exact link, never by search. Search returns old decks next to current pages.
- Skills fire on plain language only after they are validated: three real runs, the owner has read the outputs, one colleague outside the team tried it. Until then, call them by name.
- Agents start with no write access. Propose first. Verify always.
- A named owner and a last-verified date on every file. When the date runs out, the owner is asked "still accurate?".
- A check for secrets and personal data runs before anything is saved, never after.

## Licence and provenance

MIT licence, see [LICENSE](LICENSE). Take it, change it, share yours. Prepared for the talk "Building the AI Layer Your Company Actually Runs On", Berlin AI Meetup, 2026-11-11. Maintained by David Martinez.

## A shared language

Seven words this folder uses, each defined once.

| Term | What it is | Use it when |
|---|---|---|
| Skill | Reusable instructions for one outcome, in one file | You repeat a task with changing inputs |
| Agent | An assistant with a defined purpose, tools and limits | You need ongoing answers or tool-based help |
| Routine | A skill or prompt that runs on a schedule or a trigger | A defined job should run at a set time or event |
| Project | Shared context for related work | Several tasks need the same background |
| Connector | A plug that lets the assistant read, and sometimes write, a tool, through MCP | The assistant needs live data, not a pasted copy |
| Gate | A human check before anything is saved, sent or deployed | The output leaves the chat |
| Artefact | The output: a page, a report, a deck, a tool | You need a deliverable to review or share |
