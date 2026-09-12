# Proof round — cinatra#3420 (issue #3278): the recurring minute controls offer every minute

Head under proof: `0d82337fbe05bbc105898e7dc22746729e4607be`.

Both cells are [no run] cells: no agent run was dispatched. An installed agent that
carries a schedule step was launched from the product's own Agents surface, its
schedule step was set to a recurring daily schedule at 05:12 through the DRAWN
pickers only (repeat unit, hour, minute — no raw cron field was typed anywhere),
and the schedule was saved with the step's own Continue.

Every frame is the full 1440x900 window at device scale 2 (2880x1800), shot in both
palettes through the app's own theme control. The framework's own development
indicator was switched off through its own route before the first shutter (its
element measures 0x0 in every reading). The sidebar's bottom band is painted over
in every frame. The wrench in the topbar is the development-boot road's own
artefact and counts against no cell.

## Frames

| file | cell | palette | what it shows |
|---|---|---|---|
| `cell1-trigger-screen-recurring-05-12-editable-light.png` | CELL1 | light | the schedule step's recurring controls, editable, holding a daily 05:12 before it is saved |
| `cell1-trigger-screen-recurring-05-12-editable-dark.png` | CELL1 | dark | the same state in the dark palette |
| `cell2-schedule-card-read-back-05-12-light-r2.png` | CELL2 | light | the saved schedule as the product reads it back on the Schedule tab: 05 : 12, no empty segment |
| `cell2-schedule-card-read-back-05-12-dark-r2.png` | CELL2 | dark | the same reading in the dark palette |
| `cell2-schedule-card-read-back-05-12-light.png` | CELL2 | light | the first pair of this cell, superseded by the `-r2` pair, which adds the measured region around the minute segment |
| `cell2-schedule-card-read-back-05-12-dark.png` | CELL2 | dark | as above |

`measurements.json` carries, per frame, the sha256, the byte count, the pixel size,
the mean luminance, the luminance of the region around the minute segment, and the
DOM reading taken in the same instant. `dom-readings.jsonl` is the append-only log of
those readings, one line per shutter.

## What the readings say

* CELL1 — the minute control holds the value `12`, its option set counts **60**
  entries running `0` to `59`, and the drawn segment reads `12`. The hour control
  holds `5`; the repeat unit holds `daily`.
* CELL2 — the drawn minute segment of the read-back schedule card reads `12` and is
  not empty. The option count of that control was read from the product's own picker,
  opened and closed a moment before each shutter: **60** options, `00` first, `59`
  last, `12` checked.
* No raw cron field is drawn on either surface in any frame.

## Read back from the store

    TRIGGER | type=recurring | cron=12 5 * * * | tz=UTC | enabled=true | fired=

The stored schedule is the one the reader stated and the one the surfaces draw.
