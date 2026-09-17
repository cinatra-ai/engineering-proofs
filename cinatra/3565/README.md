# Proof round 2 — the run page of one undispatched run holding its Skills question

Scope: the run page of a single undispatched agent run parked on its recommendation
checkpoint, in both palettes, at the pull request head 76477c53.

Frames

- cell1-skills-question-held-light.png — CELL1, light palette. The step rail and the
  run detail are both whole in the window. The Skills entry heads the rail and is the
  selected step; the run detail shows the Skills card with the one offered skill and
  the Continue control. The three numbered entries below sit unreached and are not
  selectable.
- cell1-skills-question-held-dark.png — CELL1, dark palette, the same state through
  the product's own theme control.
- cell2-after-press-schedule-light.png — CELL2, recorded and never counted. The same
  page one moment later, after the second numbered entry further down the rail was
  pressed. That entry reads not selectable, the press changes no selection, and the
  run detail keeps the card it was showing rather than going blank.
- cell2-after-press-schedule-dark.png — CELL2 in the dark palette.
  indicator was switched off through its own route; both bottom corners are clear of
  any round badge. Not a graded frame.

Readings

- dom-readings.jsonl — one appended reading per shutter: the page path, the breadcrumb,
  every rail entry with its numeral, label, selected and not-selectable readings, and
  whether the Skills card is present.
- frame-measurements.json — per frame: sha256, bytes, pixel size, mean luminance and
  the luminance of the rail-and-detail region.

Notes

- No agent executed and no model call was made: the run parked before any dispatch, so
  both cells are marked no run.
- The account band is painted over in every frame.
- The wrench control in the top bar is the development-boot road's own artefact and is
  not counted against any cell.
