# Seventh proof round, part b — pull request 3143 (issue 3091), 2026-09-08

Proof head `17861c50905dce4003c8eaf078e9fd2e24288db7`. Every frame is a whole window at
1440x900 css, device scale factor 2 (2880x1800 pixels), shot on a development boot per the
2026-09-03 ruling, on the full browser build, in both palettes through the product's own theme
control. The framework's own development indicator is disabled through the framework's own
means and reads 0x0 on every frame. The topbar development-tools control is the
development-boot road's own artefact, named once here and never counted against a cell.

Cells 1 to 4 are the eight frames of this round's first pass, reused verbatim with their own
readings; they draw artifacts, not runs, and carry the marker [no run]. Cell 6 was driven fresh
from ONE real agent run dispatched through the product's own chat.

| frame | cell | palette | what it shows | verdict |
| --- | --- | --- | --- | --- |
| cell1-pdf-artifact-page-light.png | CELL1 | light | the uploaded pdf's artifact page: the embedded viewer fills the panel and draws page 1 of 2; the header closed at the six-fact mono meta line; no download floor | state captured |
| cell1-pdf-artifact-page-dark.png | CELL1 | dark | the same surface in the dark palette | state captured |
| cell2-json-artifact-page-light.png | CELL2 | light | the uploaded json's artifact page: the value tree through the content channel; no download of its own | state captured |
| cell2-json-artifact-page-dark.png | CELL2 | dark | the same surface in the dark palette | state captured |
| cell3-screenshot-artifact-page-light.png | CELL3 | light | the screenshot artifact page: the picture drawn to its own aspect through the byte road; the screenshot line drawn by its pack | state captured |
| cell3-screenshot-artifact-page-dark.png | CELL3 | dark | the same surface in the dark palette | state captured |
| cell4-text-artifact-page-light.png | CELL4 | light | the text artifact page: the content channel draws the body; the same header | state captured |
| cell4-text-artifact-page-dark.png | CELL4 | dark | the same surface in the dark palette | state captured |
| cell6-review-card-pending-light.png | CELL6 | light | the review card of the real run, PENDING: the two-entry step rail, the six pinned targets with their meta lines, the decision bar (Reject, Approve) and the prompt window beneath the card | state captured |
| cell6-review-card-pending-dark.png | CELL6 | dark | the same surface in the dark palette | state captured |
| cell6-review-card-settled-light.png | CELL6 | light | the same review card SETTLED by Approve: the decision bar and the prompt window are gone, the targets stand | state captured |
| cell6-review-card-settled-dark.png | CELL6 | dark | the same surface in the dark palette | state captured |
| cell6-run-page-light.png | CELL6 | light | the run page of the same real run: the run-made panel with the six produced artifacts and the settled review marker | state captured |
| cell6-run-page-dark.png | CELL6 | dark | the same surface in the dark palette | state captured |
| cell6-review-card-settled-foot-light.png | CELL6 | light | the same settled surface scrolled to its foot: the settlement card reading approved, beneath an unresolved skeleton region | state captured |
| cell6-review-card-settled-foot-dark.png | CELL6 | dark | the same surface in the dark palette | state captured |
| cell6-run-page-foot-light.png | CELL6 | light | the run page scrolled to its foot | state captured |
| cell6-run-page-foot-dark.png | CELL6 | dark | the same surface in the dark palette | state captured |

## Frame integrity

- The two PENDING frames show the review card from the top of the surface. The decision bar and
  the prompt window sit below the 900 css window on that pair, so those two regions are not shown
  on pixels there. The gate was settled before this was seen, and a later real run produced no
  second pending gate, so the pending decision bar is reported as NOT CAPTURED rather than as
  shown. The foot frames prove the foot of the settled card and of the run page.
- On every frame of this cell a large region between the pinned targets and the foot of the
  surface paints as an unresolved skeleton, in both palettes and on both surfaces. It is recorded
  as a reading here and left to the grading stage.

## Not captured

- **CELL5 (the widget rows)** — NOT CAPTURED. The mount itself is correct: the frame answers
  200 with `content-security-policy: frame-ancestors` naming the connected application's own
  origin for the wordpress assistant handle, and the launcher and the panel mount on the seeded
  editor screen. The first-party sign-in inside the frame then answers **401 on
  `POST /api/widget-auth/frame/init`**, so no session is established and no row can be drawn.
  Nothing was shot and no substitute was used.
- **CELL6's featured image** — NOT CAPTURED. The pipeline declared and produced no image output
  on this instance: its six produced artifacts are five text/plain blog ideas and one
  application/json index. The review card and the run page above were therefore shot over the
  artifacts the real run actually produced, and every frame is named for what it shows. The
  image subject of the cell is not proven by this round.

`measurements.json` carries, per frame: the cell, the palette, the run id where the cell draws a
run, sha256, byte count, pixel size, whole-frame mean luminance, the bottom-right 300 by 300
region reading, and the DOM measurement of the header, the step rail, the decision bar, the
prompt window and the drawn regions taken in the same instant. `dom-readings.jsonl` is the
append-only shutter log; where a cell carries more than one pair, the LAST rows for that cell and
palette are the live ones.
- **CELL6's pending decision bar and prompt window** — NOT CAPTURED on pixels (see Frame
  integrity above). Their boxes were measured in the same instant and are carried in
  `measurements.json`.
