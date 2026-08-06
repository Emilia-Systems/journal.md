# journal.md

A single, dated log of everything done, across all repository, in the process of building a full open system from the ground up.

## Why a separate journal repo

Work on a project like this happens across many repos, often in parallel, over a long stretch of time. Without a single record:

- there's no easy way to see what happened on a given day across the whole project
- context and reasoning behind decisions gets lost once it scrolls out of a single repo's commit history
- anyone trying to follow along (including me) has to dig through commit logs in five different places

`journal.md` is the one place that answers "what happened, and where" for the whole project, day by day. It's meant to be read like a devlog: short, honest, and current, and not a polished writeup.

## Format

Entries live in a single file, [`journal.md`](journal.md), in **reverse-chronological order** (newest at the top, so the latest work is always visible without scrolling).

Each day gets a level-2 heading with the date (`YYYY-MM-DD`), followed by one bolded line per repo touched that day, describing what was done in it.

```
## 2026-08-07

**emilia** — some cursed program encountered
**jny** — also very much important work done

## 2026-08-06

**emilia** — started some very important work
**journal** — wrote initial README
```

A few conventions to keep it consistent:

- Repo names should match the actual repo name exactly, so they're easy to search for (`Ctrl+F "cpu-rtl"` should find every day that repo was touched).
- Keep each line to what was *done*, not general commentary, save deeper writeups (design notes, "why") for that repo's own README or docs.
- Optionally, link a commit or PR at the end of a line, e.g. `**jny** — fixed A20 line enable ([commit_n](../jny/commit/n))`.
