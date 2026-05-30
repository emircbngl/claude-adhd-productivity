# adhd-productivity — an ADHD productivity plugin for Claude Code

> A **Claude Code plugin** (skill + hooks + slash commands) that makes Claude work like an **ADHD-optimized productivity coach and externalized executive function** — for both everyday tasks and coding.

**Topics:** `claude-code` · `claude-code-plugin` · `claude` · `adhd` · `productivity` · `focus` · `executive-function` · `body-doubling` · `pomodoro` · `neurodivergent`

It doesn't make Claude "scattered." It teaches Claude the *compensatory operating system* that actually makes ADHD brains productive: shrink everything to one tiny next action, externalize working memory to a file, manufacture motivation, body-double through the work, make progress visible, and never shame.

> One next physical action. Always.

## Why this exists

ADHD runs on an **interest-based nervous system**, not an importance-based one. Motivation comes from **INCUP** — Interest, Novelty, Challenge, Urgency, Passion (Dr. William Dodson) — not from "this is important." A task with none of those is *neurologically* hard to start, however trivial it looks. The friction is rarely "not knowing what to do"; it's activation energy, working-memory overload, time blindness, overwhelm, and rejection-sensitive shame.

This plugin turns those insights into how Claude behaves.

## Core behaviors

- **One next *physical* action** — every reply ends with a single concrete step ("open `notes.md`, write one bad sentence"), never a to-do list.
- **Externalized memory** — current task, steps, parked ideas, and progress live in a visible `FOCUS.md`, so nothing depends on memory (yours *or* Claude's).
- **2-minute steps** — anything bigger than ~5 minutes gets broken down before you start.
- **INCUP injection** — when a task feels flat, Claude adds urgency (a timer), challenge, novelty, or meaning.
- **Body doubling** — short timed sprints with gentle check-ins; presence, not supervision.
- **Visible progress** — ticked steps, counts, and streaks; every completion is celebrated.
- **Zero shame** — when you stall or spiral, Claude normalizes it, shrinks the task, and restarts gently. No "should", no guilt.
- **Capture, don't chase** — stray ideas go to a parking lot so the current thread survives.
- **Coding mode** — smallest runnable/committable step, scaffold the blank file, "make it run then make it right", green tests as dopamine hits.

## Install

```
/plugin marketplace add emircbngl/claude-adhd-productivity
/plugin install adhd-productivity
```

Then restart Claude Code. (To try it locally before publishing, run `/plugin marketplace add` with the absolute path to this folder instead of the GitHub slug.)

> Forking or rehosting? Update the `emircbngl/claude-adhd-productivity` slug in `.claude-plugin/marketplace.json` and `.claude-plugin/plugin.json` to your own.

## Commands

| Command | What it does |
|---|---|
| `/focus [task]` | Start a focus session: one task → 2-minute steps → timed body-doubling. |
| `/braindump` | Empty everything on your mind into the parking lot, then pick the one thing for now. |
| `/next` | Restate the single next physical action. |
| `/breakdown [task]` | Decompose a task into 2-minute steps. |
| `/done [what]` | Mark a step/task done — celebrate, bump the streak, surface the next action. |
| `/checkin` | Low-pressure body-double check-in. |
| `/park [idea]` | Capture a tangent without derailing. |
| `/unstick` | Stuck/overwhelmed/spiraling rescue: normalize → shrink → one tiny action. |

The plugin also activates automatically when you sound overwhelmed, stuck, or are staring down a vague/giant task — no command required.

## How `FOCUS.md` works

Claude keeps a short `FOCUS.md` at the root of your working directory holding your current task, the one next action, your 2-minute steps, a parking lot, your progress/streak, and a resumption point. It's a **cache, not a journal** — overwritten freely and cleared when a task is done.

In a code repo, add `FOCUS.md` to your `.gitignore` — it's personal working state, not project code.

## Hooks (always-on scaffolding)

- **SessionStart** — silently surfaces `FOCUS.md` so a new session opens with your current next action instead of a blank slate.
- **PostCompact** — re-reads `FOCUS.md` after context compaction, so a long session never loses your place.
- **Stop** — reminds Claude to flush the latest state back to `FOCUS.md` before ending.

## Project layout

```
adhd-productivity/
├── .claude-plugin/{plugin.json, marketplace.json}
├── skills/adhd-focus/SKILL.md          # the operating doctrine
│   └── references/                     # incup, task-decomposition, coding-mode,
│                                       # anti-shame-rsd, body-doubling, focus-state-format
├── hooks/hooks.json
└── commands/                           # the 8 slash commands above
```

## Credits & sources

The behavior model draws on widely-used ADHD productivity and coaching frameworks: ADDA (time blindness, body doubling), ADDitude (ADHD strengths — hyperfocus, divergent thinking), CHADD / the ADD Resource Center (dopamine, task initiation), Dr. William Dodson's INCUP framework, the Professional Association of ADHD Coaches' core competencies, and practitioner sources on externalizing working memory, the 2-minute rule, and Pomodoro for ADHD.

This is a behavioral coaching tool, not medical advice.

## Star history

<a href="https://star-history.com/#emircbngl/claude-adhd-productivity&Date">
  <img src="https://api.star-history.com/svg?repos=emircbngl/claude-adhd-productivity&type=Date" alt="Star history chart for emircbngl/claude-adhd-productivity" width="640">
</a>

## License

MIT — see [LICENSE](LICENSE).
