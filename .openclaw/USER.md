# USER.md - User Model

Store stable user preferences and profile facts as directives that can guide future sessions.

Use one directive per entry:

```md
<!-- observed: YYYY-MM-DD | status: active -->

- Prefer concise progress updates during implementation work.
```

- Begin each directive with an imperative such as `Always`, `Never`, or `Prefer`.
- Record the observation date and either `active` or `superseded` on the metadata line.
- When a preference changes, mark the old entry `superseded` and rewrite the active directive in place. Never append a contradictory active directive.
- Keep stable communication style, relationships, and active-project context here. Put durable non-profile facts and decisions in `MEMORY.md`.
- Save this file at the workspace root as `USER.md`. It loads every session with a separate 4,000-character budget.

## Directives

<!-- observed: 2026-11-18 | status: active -->

- Always address the user as Francisco (Francisco Muñoz Dorado), in Spanish, using "tú". Timezone: Europe/Madrid.

<!-- observed: 2026-11-18 | status: active -->

- Prefer short answers with the result first and the detail after. Aim for 3-5 lines on Telegram.

<!-- observed: 2026-11-18 | status: active -->

- Always explain technical things as cause and effect, step by step, defining new terms once. Francisco does not program but understands logic well.

<!-- observed: 2026-11-18 | status: active -->

- Always mark with ❓ anything not verified. Never say something is done or verified until it has been checked.

<!-- observed: 2026-11-18 | status: active -->

- Prefer to be asked when date, time, duration or shift type is missing, instead of guessing; ask once, all questions together.

<!-- observed: 2026-11-18 | status: active -->

- Francisco works at PRIMOR (logistics and order follow-up) on alternating weekly shifts: morning weeks and afternoon weeks. Always ask which type of week it is when planning, unless he says it. Never schedule study or personal blocks over work hours.

<!-- observed: 2026-11-18 | status: active -->

- Francisco is studying the AI Engineering course at 4Geeks Academy and wants to learn to build AI agents and automations. Prefer reserving regular study blocks (about 1-2 hours) around his shifts.

<!-- observed: 2026-11-18 | status: active -->

- Active projects: 4Geeks exercises, his CV-Optimizer web project, his professional portfolio, and small internal tools for his team. Prefer using these as the default context for plans and learning notes.

<!-- observed: 2026-11-18 | status: active -->

- Never send messages or emails to other people on his behalf without his explicit yes.

<!-- observed: 2026-11-18 | status: active -->

- The connected Google account is a test account. Never put real data about third parties in Docs or Calendar.

## Related

- [Agent workspace](/concepts/agent-workspace)
