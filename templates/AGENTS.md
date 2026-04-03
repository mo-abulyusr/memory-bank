# Memory Bank Agent Guide

Use Memory Bank to keep project context in files that survive across sessions.

## Session Start

Before doing work:

1. Check for `memory-bank/` at the project root.
2. If it is missing, create it with these files:
   - `memory-bank/projectbrief.md`
   - `memory-bank/activecontext.md`
   - `memory-bank/decisionlog.md`
   - `memory-bank/progress.md`
3. Read `memory-bank/projectbrief.md` and `memory-bank/activecontext.md`.
4. Read `memory-bank/decisionlog.md` and `memory-bank/progress.md` when the task needs historical context, planning, or progress.

## During Work

- Update `activecontext.md` when focus, blockers, or next steps change.
- Update `decisionlog.md` when a durable decision is made.
- Update `progress.md` when meaningful work starts or finishes.
- Update `projectbrief.md` only when stable project context changes.

## File Roles

- `projectbrief.md` - stable project purpose, structure, constraints, conventions
- `activecontext.md` - current focus, blockers, and next steps
- `decisionlog.md` - durable decisions and rationale
- `progress.md` - completed work, in-progress work, known issues

## Writing Rules

- Keep entries short.
- Keep entries factual.
- Use plain language.
- Prefer file paths over long explanations.
- Store no secrets.
