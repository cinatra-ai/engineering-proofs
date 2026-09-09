# Proof round — run detail, fix leg 4

All frames are whole-window pictures of REAL agent runs dispatched through the product on the proof boot at the pushed head `5c0fbb202d6fe1bbcd22a4130dc490bab2625e75`. Both palettes come from the app's own theme control. This round ran on a development boot per the standing dev-boot road of 2026-09-03; the topbar wrench control ("Open development tools") is that road's artefact and is not counted against any cell. The framework's own development indicator is hidden through the framework's own means and proven on the pixels (the dark completion frame's bottom-right 300x300 css region reads a flat 7, the dark page ground).

The runtime container for this round was recreated from the newer image tag whose output-schema composer matches the tree (14 `additionalProperties` sites in both the container and the worktree source; the previous image read 8).

## Frames

| file | cell | palette | run | what it shows | verdict |
|---|---|---|---|---|---|
| CELL1-pending-gate-whole-run-detail-light.png | CELL1 | light | bebb48fd | the whole run detail parked on the pending review gate: rail, gate header `Review requested` with the pill `Awaiting your decision`, the targets, the decision bar closing the card, the prompt window beneath the card | PASS |
| CELL1-pending-gate-whole-run-detail-dark.png | CELL1 | dark | bebb48fd | same state, dark palette | PASS |
| CELL1-pending-gate-decision-bar-and-prompt-window-light.png | CELL1 | light | bebb48fd | the card foot: decision bar inside the frame, prompt window outside and beneath it | PASS |
| CELL1-pending-gate-decision-bar-and-prompt-window-dark.png | CELL1 | dark | bebb48fd | same, dark palette | PASS |
| CELL1-pending-review-gate-run-detail-light.png | CELL1 | light | bebb48fd | first pair of the round, head of the run detail (gate header, pill, targets); the card foot is below this frame's fold | SUPERSEDED by the whole-detail pair |
| CELL1-pending-review-gate-run-detail-dark.png | CELL1 | dark | bebb48fd | same, dark palette | SUPERSEDED by the whole-detail pair |
| CELL2-completed-run-detail-rail-and-plate-light.png | CELL2 | light | 65fef1c3 | the whole run detail of a completed run of an agent that declares no review step: the pill `completed`, one surface in the detail column, no entry marked current | PASS |
| CELL2-completed-run-detail-rail-and-plate-dark.png | CELL2 | dark | 65fef1c3 | same, dark palette | PASS |
| CELL2-completed-run-whole-detail-light.png | CELL2 | light | 65fef1c3 | same pixels as the pair above; its recorded rail reading names the tab row, not the rail | SUPERSEDED (reading) |
| CELL2-completed-run-whole-detail-dark.png | CELL2 | dark | 65fef1c3 | same | SUPERSEDED (reading) |
| CELL2-completed-run-no-review-step-light.png | CELL2 | light | 65fef1c3 | first CELL2 pair, window-height frame; rail reading empty | SUPERSEDED (reading) |
| CELL2-completed-run-no-review-step-dark.png | CELL2 | dark | 65fef1c3 | same | SUPERSEDED (reading) |
| CELL3-decided-gate-run-detail-light.png | CELL3 | light | bebb48fd | the same run after its gate was decided through the card's decision bar: the settled entry keeps its place with a settlement marker, zero entries marked current | PASS with one wording departure |
| CELL3-decided-gate-run-detail-dark.png | CELL3 | dark | bebb48fd | same, dark palette | PASS with one wording departure |
| CELL4-two-gates-waiting-at-first-light.png | CELL4 | light | 6a88c3f3 | a run that declares two review steps in order, read while it waits at the first: exactly one entry marked current, the second drawn but not highlighted, the step card ending with its decision control and the prompt window beneath it outside the card | PASS |
| CELL4-two-gates-waiting-at-first-dark.png | CELL4 | dark | 6a88c3f3 | same, dark palette | PASS |

## The two findings of the refusal, measured on these frames

1. The prompt window is NOT inside the review card's frame. On every CELL1 and CELL3 frame the review card frame is a `section` with a 16 px radius and a 1 px border; its box ends 16 px above the prompt window's mount, `promptWindowInsideReviewCardFrame` reads false, and the mount is the last element of the run detail column (no siblings after it).
2. Every rail entry is ONE label. CELL1/CELL3: `Setup`, `Review`, `What this run made`. CELL2: `Setup`, `What this run made`. CELL4: `Select blog idea`, `Review blog draft`. No second line, no reason sentence, and no machine word on any entry on any frame (`railMachineWordHits` empty everywhere).
3. Exactly one entry carries the current-step marker on CELL1 and CELL4; zero on CELL2 and CELL3.

## Departures recorded, not graded here

- The settled entry on CELL3 renders its settlement as `approve`; the ratified drawing's settlement words are `continued`, `superseded by a regeneration`, `changes requested`.
- The decided card on CELL3 still carries the header `Review requested` after the decision; the hold pill is correctly gone.
- The gate on CELL1 carries six target panels under one header and one rail entry.
- The rail draws the still-to-come entry `What this run made` with the same settled glyph as the passed `Setup`.
- The target meta line reads `organization` twice, for the ownership level and for visibility.
