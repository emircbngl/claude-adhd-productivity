# FOCUS.md — the externalized working memory

`FOCUS.md` is the single source of truth for what the user is doing *right now*. It lives at the **root of the working directory**, visible on purpose: ADHD brains run on "out of sight, out of mind," so the state must be somewhere they (and you) will actually see it.

In a code repository, tell the user once to add `FOCUS.md` to `.gitignore` — it's personal working state, not project code.

## Core rules

- **It's a cache, not a journal.** Overwrite freely. Do not accumulate history or logs.
- **Update it the moment state changes** — a step finishes, an idea gets parked, the task changes, the session ends.
- **One active task at a time.** If they're juggling several, the others go in the parking lot, not the "Current task" slot.
- **When a task is fully done,** clear the task/steps and bump the Progress line. A near-empty FOCUS.md is a good thing.
- **The NOW line is sacred.** It always holds exactly one concrete, physical action.

## Schema

```markdown
# Focus
Updated: 2026-05-28 14:32

## ▶ NOW (the one next physical action)
- [ ] <a single concrete, physical action — start with a verb like open/type/write/click>

## Current task
<task name> — <why it matters / the INCUP hook> — est <N> min

## Steps (2-min chunks)
- [x] <done step>
- [ ] <next step>   ← you are here
- [ ] <later step>

## Parking lot (captured, not now)
- <stray idea, tangent, or task for later>

## Progress
Today: ✓✓✓ (3 done) · Streak: 4 days

## Resumption point
When you come back: start at "<step>". You were <one line of context>.
```

## Filled example

```markdown
# Focus
Updated: 2026-05-28 14:32

## ▶ NOW (the one next physical action)
- [ ] Open Gmail and click "Compose"

## Current task
Email the landlord about the leak — gets it off my mind + stops water damage — est 6 min

## Steps (2-min chunks)
- [x] Find the landlord's email address
- [ ] Open Gmail, click Compose   ← you are here
- [ ] Write 2 sentences: what's leaking + ask them to send someone
- [ ] Hit send

## Parking lot (captured, not now)
- Renew car insurance (due next month)
- Idea: ask landlord about the radiator too — maybe, later

## Progress
Today: ✓✓ (2 done) · Streak: 3 days

## Resumption point
When you come back: start at "Open Gmail". You already have the address copied.
```

## Empty template (use when creating it fresh)

```markdown
# Focus
Updated: <timestamp>

## ▶ NOW (the one next physical action)
- [ ] 

## Current task
 — why:  — est: 

## Steps (2-min chunks)
- [ ] 

## Parking lot (captured, not now)
- 

## Progress
Today:  · Streak: 

## Resumption point
When you come back: 
```

## Tips

- The **Resumption point** is what defeats time blindness and context loss. Always leave it filled before a break or at session end, so re-entry costs almost nothing.
- The **Parking lot** is how you honor a tangent without chasing it: "Good idea — parking it so we don't lose it," then back to NOW.
- Keep the whole file short enough to read in 10 seconds. If it's getting long, it's drifting into a journal — trim it.
