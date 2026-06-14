# prune

> A reusable **work-item harness** for projects that build fast and cut hard: write the change down
> before you build it, prune the *living* set aggressively, and keep the whole record append-only. The
> name is the crux — pruning here means **retire without erasing**.

For running real changes through a project — especially when a lot of the work is done with AI agents —
without losing the thread of what is open, what shipped, and why. Code or not: it is disciplined Markdown
plus a method.

This is the harness extracted from two live projects (a persistent-AI substrate and the city it forked
from), shipped here **empty by design**: the method and the templates, with the worked examples left in
the repos that actually used it.

## The idea

Write the change down *before* you build it. Review it against a rubric frozen *ahead* of the work. When
it ships or dies, move it to `history/` with a one-line evidence note — **append-only, nothing deleted**.
So the folder is always an honest snapshot of what is actually open, and the archive is a real record
rather than a graveyard of half-truths.

- **`majors/`** — large arcs (multi-file, new subsystems, behavior changes). Shape in [`majors/MAJOR_SCHEMA.md`](majors/MAJOR_SCHEMA.md).
- **`minors/`** — bounded changes. Shape in [`minors/MINOR_SCHEMA.md`](minors/MINOR_SCHEMA.md).
- **`history/`** — the append-only archive: shipped and retired items, each with its evidence. It is
  **gitignored** and mirrors the structure one level down (`history/majors/`, `history/minors/`). The full
  ledger is kept locally; only live work is published. (One convention across every project using this kit.)
- **`harness/`** — the method: operating model, work-item lifecycle, agent execution protocol, quality
  gates, git/release policy, a pruning playbook, and copy-paste `templates/`. Start at
  [`harness/00-ADOPTION_GUIDE.md`](harness/00-ADOPTION_GUIDE.md).

## Adopt it

1. Copy this tree (or just `harness/` + the two schemas) into your repo, e.g. under `improvements/`.
2. Read [`harness/00-ADOPTION_GUIDE.md`](harness/00-ADOPTION_GUIDE.md) and
   [`harness/01-OPERATING_MODEL.md`](harness/01-OPERATING_MODEL.md).
3. Draft your first item from [`harness/templates/`](harness/templates/) (`MAJOR_ITEM_TEMPLATE.md` /
   `MINOR_ITEM_TEMPLATE.md`).
4. Keep `majors/` and `minors/` to **live** work; archive to `history/` as you close things.

It works for non-code projects too — the unit is *a decision you can review and a result you can check*,
not a diff.

## Seen in the wild

This scaffold ships empty on purpose. The same harness, fully populated with real worked examples
(triaged, scrubbed, kept append-only), runs the public `improvements/` ledgers of the projects it came
from — look there to see what a year of actual items looks like.

## Companion

Pairs naturally with a **memory** discipline (durable artifacts kept apart from prunable interpretations,
behind a single auto-loading standing brief). Two halves of the same honesty: this keeps your *intentions*
reviewable; a memory workspace keeps your *understanding* reviewable.

## License & provenance

MIT. Built by Levi Banks with AI collaborators across two live projects; the method is the contribution.
Take it and run.
