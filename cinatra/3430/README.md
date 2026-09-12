# Proof round 1 of issue #3279 — the chosen option row in both palettes

Head proved: `f471ed3392da761db7fdbc60b853a5080ee8b4b6` (pull request cinatra-ai/cinatra#3430).

Four frames, 1440x900 at device scale 2, both palettes switched through the app's own theme
control, the signed-in administrator's session reused for every frame. No agent run is part of
these cells; the schedule they show is a recurring schedule armed earlier through the product.

| frame | cell | palette | state |
|---|---|---|---|
| r2-trigger-screen-recurring-chosen-dark.png | CELL1 | dark | trigger screen, schedule step, the Recurring row chosen through the drawn control |
| r2-run-surface-schedule-card-chosen-row-dark.png | CELL1 | dark | the run surface's schedule card with its chosen option row |
| r2-trigger-screen-recurring-chosen-light.png | CELL2 | light | trigger screen, schedule step, the Recurring row chosen through the drawn control |
| r2-run-surface-schedule-card-chosen-row-light.png | CELL2 | light | the run surface's schedule card with its chosen option row |

## What the page reported at each shutter

Every value below was read through the page with `getComputedStyle` in the same instant as its
frame and is recorded per frame in `measurements.json` and `dom-readings.jsonl`.

| reading | dark | light |
|---|---|---|
| chosen row border colour | rgb(54, 78, 129) | rgb(54, 78, 129) |
| radio dot background colour | rgb(54, 78, 129) | rgb(54, 78, 129) |
| radio disc border colour | rgb(54, 78, 129) | rgb(54, 78, 129) |
| chosen row tint | the same colour at alpha 0.05 | the same colour at alpha 0.05 |
| `--indigo-ink` at the document root | #364e81 | #364e81 |
| `--primary` at the document root | #e2e8f0 | #364e81 |

The tint is reported by the page in the oklab form the framework emits,
`oklab(0.42993 -0.00946347 -0.0894125 / 0.05)`; that value converts to rgb(54, 78, 129), so edge,
dot and tint are one colour. On the trigger screen it arrives as the two-stop gradient of that
same colour over the card surface, on the schedule card as the flat 5 percent background.

The `--primary` row is the defect itself: the palette's action colour is near-white in the dark
palette and the drawn indigo in the light one. The chosen row no longer reads from it, so both
palettes now paint the same edge, the same dot and the same tint.

Unchosen rows in the same frames keep the control boundary and no tint — recorded per frame under
`unchosenRows`.

## Hygiene

The framework's own development indicator was switched off through the framework's own route and
the page reloaded before the first shutter; its box was read inside its shadow root before every
shutter and is 0 by 0 in all four frames (recorded as `devIndicatorBox`). The first pair of each
state was shot before that road had taken effect, carried the indicator badge, and was deleted;
every state was re-shot under a new name with a new reading. The app's own development-tools
wrench in the topbar is the road's artefact — these frames were shot on a development boot — and
is not part of any cell.

The minute grid, the 05:12 reading and the read-only rendering belong to another issue and were
not shot here.
