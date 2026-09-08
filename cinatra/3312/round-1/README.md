# First proof round — cinatra#3312 (issue #3149), proof head 1aad52ab71a462406e81da326e86cd93239b0c02

Eight frames of the run detail on a development boot, four cells, both palettes, shot from a single headless chromium on the boot's own machine. No provider on the boot: every cell reads a run STATE, not model output; the four runs are seeded fixture rows written through the product's own store road.

## Frames

| file | cell | palette | what it shows |
| --- | --- | --- | --- |
| cell1-terminal-run-pending-gate-run-detail-light.png | CELL1 | light | terminal run, pending review gate: the gate's own card, header `Review requested` + pill hold `Awaiting your decision`, no run-progress plate, one marked rail entry |
| cell1-terminal-run-pending-gate-run-detail-dark.png | CELL1 | dark | the same, dark |
| cell2-terminal-run-no-gate-run-detail-light.png | CELL2 | light | terminal run, no gate: the plate `Agentic Run Progress` with the pill `completed`, one surface, no marked rail entry |
| cell2-terminal-run-no-gate-run-detail-dark.png | CELL2 | dark | the same, dark |
| cell3-terminal-run-decided-gate-run-detail-light.png | CELL3 | light | terminal run, gate decided: the settled gate's read-only page, the settled entry keeping its place, no marked rail entry |
| cell3-terminal-run-decided-gate-run-detail-dark.png | CELL3 | dark | the same, dark |
| cell4-run-parked-on-first-of-two-pending-gates-light.png | CELL4 | light | two pending gates: the first marked, the second drawn and unmarked, one surface in the detail |
| cell4-run-parked-on-first-of-two-pending-gates-dark.png | CELL4 | dark | the same, dark |

## Files

- `measurements.json` — per frame: sha256, bytes, pixels, mean luminance, the bottom-right 300x300 css region luminance, the rail glyph region luminance per drawn entry, and the DOM state read in the same instant; plus the boot, the row readback and the development-indicator proof.
- `dom-readings.jsonl` — one appended reading per shutter, in shutter order.
- `rail-row-retake-readings.jsonl` — readings only, no new frames: the re-measurement of the rail row count asked for by the early grade.
- `rail-drawn-entry-readings.jsonl` — the drawn entries of the rail column, their boxes and their marked state.
- `early-grade.json` — the early grade written after the CELL1 pair (decision CONTINUE).
- `pr-body-section.md` — the one compact record section, per-item verdicts for items 1 to 3.
- `pr-full-record-comment.md` — the full record: readings, routes, rows, timed breakdown, boot lines, one check read.

Publication of the two Markdown files is left to the next step; this round wrote nothing to the pull request.
