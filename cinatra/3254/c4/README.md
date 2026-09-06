# cinatra#3254 FOURTH proof round (issue #3184): the Skills step after the forward onto the re-composed rail

Proof head eace81ff1eb2f57e77d634f40779e1a1fb5f410d — the pull request's own head at shutter time,
checked out in the worktree, tree clean. Design main 033a697c3fede6920bac3d4c61e08def57436f02.
Dev boot on port 3254 out of that worktree, per the standing 2026-09-03 decision. The boot was proven
to serve THIS head before the first shutter: both the branch's own `runInDispatchHandoff` and the
merged rail's `gateStepInRail` are present in the boot's compiled server chunks.

Frames at 1440x900 css, device scale 2 (2880x1800 px), both palettes reached through the app's own
theme control, full window, at rest. Real runs of the installed Author Agent dispatched from the
agent's own new-run road; two skills offered, one ticked before Continue.

## The cells and the two run rows

SIX frames, six appended readings, no re-shoot, no overwrite.

- **CELL1** — the run page on the Skills step of a fresh run, before any choice. Shot FIRST in both
  palettes for the early gate.
- **CELL3** — the regression smoke: the rail's rhythm on the Skills step (mark centres, separator
  margins, pitch) measured against the rail rules as pull request 3236 lands them, one skill ticked.
- **CELL2** — the same run after Continue on the Skills step, on the client road with no reload.

Each palette is ONE run row: light 52d08271-60b3-40dd-8294-683d8593e1de, dark
05ea6256-afda-48cf-9c9b-41119fae78f6. CELL1 was shot on that row first; CELL3 and CELL2 continue on
the same row (CELL3 precedes CELL2 in time, because the rhythm cell names the Skills step and CELL2
is what follows Continue).

## The reading, identical on all six frames

railOrder ["Skills", "1 Setup", "2 Schedule", "3 Review"] on every frame, both palettes. tabsLit []
on every frame. detailHeadingCount 0 on every frame. No scheduling form on the Skills page on any
frame. railCurrent ["Skills"] on CELL1 and CELL3; on CELL2 the Skills entry reads settled and the
detail carries the next step's own page with no chip row (pillCount 0, Continue count 0).

## The rail's rhythm (CELL3, both palettes, identical)

Four rows, three marks between them. Every row: display flex, align-items center, 8px gap,
2px/2px padding, 14px font over a 16.1px line box, row box 28px, mark 24x24 fully rounded, mark
centre exactly the row-box centre (delta 0.0000 px). Every separator: 2x8, margins 4 above and 4
below, 11px in from the rail column, 1px radius, static, a sibling of the rows and never inside one.
Pitch a uniform 44.0 px across all three pairs. Zero violations of the drawing's rules.

## Frames

| picture | cell | theme | run |
|---|---|---|---|
| c4-cell1-skills-step-fresh-run-before-any-choice-light.png | CELL1 - the Skills step of a fresh run, before any choice | light | 52d08271 |
| c4-cell1-skills-step-fresh-run-before-any-choice-dark.png | CELL1 - the same, dark palette | dark | 05ea6256 |
| c4-cell3-regression-smoke-rail-rhythm-on-the-skills-step-one-skill-ticked-rail-four-entries-no-tab-lit-light.png | CELL3 - the rail's rhythm on the Skills step, one skill ticked | light | 52d08271 |
| c4-cell3-regression-smoke-rail-rhythm-on-the-skills-step-one-skill-ticked-rail-four-entries-no-tab-lit-dark.png | CELL3 - the same, dark palette | dark | 05ea6256 |
| c4-cell2-after-continue-next-step-page-in-the-detail-rail-four-entries-no-tab-lit-light.png | CELL2 - after Continue, the next step's page in the detail | light | 52d08271 |
| c4-cell2-after-continue-next-step-page-in-the-detail-rail-four-entries-no-tab-lit-dark.png | CELL2 - the same, dark palette | dark | 05ea6256 |

FRAME INTEGRITY: every file is named for what its window actually carries at the shutter — the rail
entry count and the lit-tab state are in the CELL2 and CELL3 file names, so a frame can never stand
in for a state it does not show.

## The framework's own development indicator

Hidden on all six frames through the framework's own means (the persisted preference plus the
framework's own disable call), and proven on PIXELS per recipe 9c: the bottom-right 300x300 css
region reads one flat value on every frame, minimum equal to maximum — light 240.71, dark 6.45;
portal box 0x0. The app's own development-only wrench in the topbar is the dev-boot road's artefact
and counts against no cell.

## One instrument note, not a product finding

The repository's own opt-in rail-rhythm grader
(`tests/e2e/run-page-rail/rail-rhythm.spec.ts`) selects a rail row's mark by
`[data-slot="stepper-indicator"], [data-conformance-id="run-surface-rail-indicator"]`. The Skills row
draws its mark as `[data-conformance-id="recommendation-rail-indicator"]`, which that list does not
name, so the shipped instrument reads three rows where the rail draws four. This round's driver adds
that selector and reads all four. The CELL1 light frame was shot before the driver carried it, so its
own rhythm sub-reading covers three of the four rows; every other reading on that frame is complete,
and the rhythm cell is CELL3, which is complete in both palettes. This is a defect of the test
instrument, not of the drawn rail.
