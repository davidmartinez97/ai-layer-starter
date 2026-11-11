# Skills: how to write one

A skill is one text file that teaches the AI one job. It follows the open Agent Skills format: a folder named after the skill, with a `SKILL.md` inside. Copy [meeting-notes/SKILL.md](meeting-notes/SKILL.md) to start.

## The four parts every skill has

1. **A header** with `name`, `description` (one sentence: when to use it and what it produces) and `status` (`dev` or `main`, see below). Add `owner` and `last_verified`.
2. **Trigger phrases:** the words people actually say. "Clean up these notes." "What did we decide?"
3. **Steps:** numbered, specific, in the order the work happens. The first step is the privacy gate if the input can contain personal data.
4. **The output template:** the exact shape of what comes back. People read the output, not the skill.

## The two tiers

| Tier | When it fires | Until when |
|---|---|---|
| `dev` | Only when someone calls it by name | Until it is validated |
| `main` | On plain language matching the trigger phrases | After validation |

Validated means: three real runs, the owner has read the outputs, and one colleague outside the team has tried it. Write the date of validation into the header. Half-validated skills firing on their own is how a team loses trust in a week.

## Rules

- One skill, one job. A skill that does three things is three skills.
- Owner and last-verified date in the header. Re-verify every 90 days.
- No company facts inside a skill; the skill points to `company.md` and the index.
- A skill that writes anywhere (wiki, chat, tracker) asks for confirmation first, every time, unless the owner has explicitly allowed otherwise in `connections.md`.
