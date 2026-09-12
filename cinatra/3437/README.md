# Review gate: a second answer to a decided gate — proof round frames

Three cells, shot on a development boot of the branch head that the pull request
ships, on real runs of the Blog Idea Generator Agent dispatched through the
product's own screens. Every run reached the runtime and carries a runtime task
id, an execution attempt id and a trigger row; no row was written into a
database and no state was seeded or substituted.

## What the round did

Two browser contexts, both signed in through the product's own sign-in page,
opened the same run page while the run stood at its mid-run review gate. Both
armed a real click on the gate's own Continue control for the same wall-clock
millisecond. One answer was accepted, the run continued on it and completed; the
other was refused with the typed no-longer-pending outcome, and that context
drew the Blocked-state card instead of an empty panel.

## The frames

| file | cell | theme | what it shows |
|---|---|---|---|
| cell1-blocked-card-light-second-context-light.png | CELL1 | light | the losing context's Blocked-state card: "This review is no longer open" over "The gate was already decided or the run moved on." with the Refresh back to the live gate, and no decision floor left in the gate region |
| cell2-blocked-card-dark-losing-context-dark.png | CELL2 | dark | the same card on a SECOND gate of a second real run, in the dark palette |
| cell3-run-page-after-the-race-light.png | CELL3 | light | the run page after the race: the run moved on and its output stands at the next step |
| cell3-run-page-after-the-race-dark.png | CELL3 | dark | the same page in the dark palette |

Both presses landed in the same millisecond (recorded per frame in
dom-readings.jsonl as pressedTogetherAt), so the refusal is a real race, not a
staggered second answer.

## How to read the records

* `dom-readings.jsonl` — one line per shutter: the card's bounds, its
  no-longer-pending reason attribute, its title and body text, the Refresh
  control's bounds, what buttons remain in the gate region, whether the panel
  was empty, the palette, the theme road (the app's own theme control) and the
  run id. Append-only; a later line corrects an earlier one rather than
  rewriting it.
* `frame-measurements.json` — per frame: sha256, bytes, pixel size, mean
  luminance and, where a card is drawn, the luminance of the card's own box.

## Notes on the road

* The frames were taken on a development boot, so the topbar carries the app's
  own development-only control (the wrench). It exists only because the round
  ran on such a boot and is not part of any cell.
* The framework's own development indicator was switched off through the
  framework's own route before the first shutter (its box reads zero by zero in
  every reading).
* The band at the bottom of the sidebar, which names the signed-in person, is
  painted over in every frame.
* One earlier CELL2 attempt was discarded because the losing context drew the
  card in the wrong palette; the file was deleted rather than renamed, and the
  cell was shot again on a fresh gate. The correction stands in
  dom-readings.jsonl.
