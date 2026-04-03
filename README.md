# Memory Bank

Memory Bank is a simple file-based memory system for projects that need context to survive across sessions, handoffs, and long pauses.

---

## What It Is

Memory Bank stores the important project context in a `memory-bank/` folder at the project root.

It gives every new session the same starting point:
- what the project is
- what it is for
- what was decided
- what is in progress
- what should happen next

---

## What It Is For

Use it when work needs to stay clear over time.

It helps with:
- keeping project goals in one place
- preserving current state between sessions
- recording durable decisions and why they were made
- making handoffs easier for the next agent or contributor

---

## How It Works

The workflow is intentionally small:

1. Look for `memory-bank/` at the project root.
2. If it does not exist, create it from `templates/memory-bank/`.
3. If it exists, read `projectbrief.md` and `activecontext.md` first.
4. Read `decisionlog.md` when a choice needs context.
5. Read `progress.md` when you need the recent timeline.
6. Update the right file as work happens.

That keeps the flow steady:
- `projectbrief.md` holds the stable project foundation
- `activecontext.md` holds the current state
- `decisionlog.md` holds durable decisions
- `progress.md` holds progress and next steps

---

## What Is Inside

This repo ships one installable template:

```text
templates/
  AGENTS.md
  memory-bank/
    projectbrief.md
    activecontext.md
    decisionlog.md
    progress.md
```

File roles:
- `AGENTS.md` - tells the agent when to create the folder, what to read first, and what to update
- `projectbrief.md` - project purpose, structure, constraints, conventions
- `activecontext.md` - shared notes and per-workstream current state
- `decisionlog.md` - durable decisions with rationale
- `progress.md` - completed work, active work, known issues

---

## How To Use It

Copy the template files into the target project root:

```bash
git clone https://github.com/mo-abulyusr/memory-bank.git /tmp/memory-bank \
  && rsync -a /tmp/memory-bank/templates/ ./ \
  && rm -rf /tmp/memory-bank
```

That gives the project a root `AGENTS.md` file and a `memory-bank/` folder.

Then open `memory-bank/projectbrief.md`, fill in the project facts, and keep the other files current as work changes.

Recommended reading order at the start of work:
1. `projectbrief.md`
2. `activecontext.md`
3. `decisionlog.md` when decisions matter
4. `progress.md` when status matters

---

## Notes

- Keep paths relative.
- Keep entries short.
- Use the `Shared` section for cross-cutting blockers.
- Update only your own section in `activecontext.md`.
- Store no secrets.
