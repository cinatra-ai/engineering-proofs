# cinatra#3236 — seventh proof round (2026-09-06)

Proof head 873fbed6d6cc6ac2e568e5bcdfa66e933688738a, on a dev boot per the 2026-09-03 decision. Twelve frames across five cells, both palettes, on real runs of the blog draft writer agent. The framework's development indicator is off and proven flat on pixels in the bottom-right region of every frame.

Graded against the ratified drawing (app-artifact-review section I, IX and X; app-components Breadcrumb and Standard scheduling step), item by item:

- C1 the 24 px mark centred in its own row box: delta 0.00 CSS px on every rail row (pixel cross-read 0.5 / 0.36 / 0.22).
- C2 the wrapped title occupies three 16.1 px line boxes inside its own row box (14 px × 1.15).
- C3 every mark 24 × 24, round, never stretched.
- C4 every separator 2 × 8 px, 4 px clear above and below, 11 px from the rail column edge, on the one-line and the wrapped pair alike.
- C5 no separator box overlaps any row box; the wrapped row's last text line ends at y 317.5 and the separator starts at y 328.0.
- C6 pitches 56.0 for a one-line/three-line pair and 44.0 for one-line pairs, both palettes.
- C7 settled and upcoming marks muted with a paper tick; exactly one elected row on a gate-parked run, none on a resolved run.
- C8 the review reading's prompt window: the placeholder sentence inside the field box, the send control beside it with 25 CSS px clearance.

Frames:

- cell1-2-panel-rail-wrapped-row-rowbox-measured-run-2e37fd05-{light,dark}.png — the run page's panel rail with a three-line wrapped work-step row (resolved run).
- cell3-panel-rail-gate-parked-active-row-run-cfa85a64-{light,dark}.png — the rail on a run parked on a gate, one active row in ink.
- cell4-review-reading-prompt-window-sentence-inside-field-run-7d274bed-{light,dark}.png — the review reading's prompt window.
- cell5-scheduling-gate-elected-breadcrumb-duration-line-run-621e62a1-{light,dark}.png — the scheduling gate class with the instance breadcrumb and the duration line above the actions.
- Two earlier frames of cells 1–2 and 4 are kept as superseded shutters (same pixels, an earlier DOM reading that measured the per-item wrapper).

Recorded, not counted: pre-existing filed departures; the run page's tab strip carries the work step's title as a third tab; the settled review entry's kind label typography.
