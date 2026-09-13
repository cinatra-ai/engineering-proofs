# Proof round — each artifact renders itself, and a list payload is never a review target

Four frames from one real agent run, shot on a development boot of the branch head
`c9a67b23d4d63fed88575051e0ff2492e38ab938`, both palettes through the application's own
theme control, every frame whole (full page).

## The run

The Blog Idea Generator agent is installed from the product's own marketplace (its
detail page offers Uninstall, so it is installed). One run was dispatched through the
Run-agent wizard on the signed-in administrator session: Setup with a brief asking for
five distinct blog post ideas, Schedule "Run right after setup", then the context step,
which reported no eligible context artifacts and was continued through. The run filed
six artifacts — five blog ideas and the generator's own JSON ideas payload — and parked
on its pending review gate. The gate pinned five targets: the five ideas. The JSON
payload that represents the set is not among them.

## The frames

| file | cell | shows |
|---|---|---|
| cell1-review-page-artifact-blocks-light.png | 1 | the review page, reached through Agents then Reviews then the gate's own link; whole page, light |
| cell1-review-page-artifact-blocks-dark.png | 1 | the same page, dark |
| cell2-run-page-review-step-blocks-light.png | 2 | the run page parked on its Review step, reached through Agents then Executions; whole page, light |
| cell2-run-page-review-step-blocks-dark.png | 2 | the same page, dark |

## What the pixels show

Five blocks are drawn, one per pinned artifact. Each is one bordered block whose
immutable header sits directly over its own body — measured, the head's foot meets the
body's top within four pixels and the two share the same left edge and the same width in
every block on both pages. The blocks follow one after another down a scrolling page
(scroll height 2764 on the review page, 3129 on the run page, against a 900-pixel
window). No column of headers followed by a region of bodies appears, and no inner
capped scroll region was measured on either page.

No JSON list block appears among the targets on either page: every block carries the
Blog Idea badge.

## Readings

`measurements.json` carries, per frame, the sha256, the byte size, the pixel size, the
mean luminance and the luminance of the block column, together with the page path, the
page's own breadcrumb, the heading, the scroll height, the palette the application's own
control was set to, the state of the framework's development indicator at the shutter,
and the per-block boxes. `dom-readings.jsonl` carries one appended reading per shutter.

## Notes

The framework's development indicator was switched off through the framework's own route
before the first shutter; the route answered 204 and no indicator node was present at any
shutter.

The application's own development-only control in the top bar (the "Open development
tools" wrench) is present because this round ran on a development boot. It is the road's
artefact and is not part of any cell.

Anomaly, not part of any cell: each artifact body renders the placeholder "The preview
did not load" on this boot. The composition under test — one header directly over its own
body, blocks one after another, no list target — is unaffected and is what the frames
show.

The grey band over the lower left of each frame is painted over the account strip before
the shutter. An earlier set of four frames in this round was shot before that band was
added; those files were deleted rather than reused, and the two surfaces were shot again
under the file names above. The withdrawn readings are left in the readings log, unedited,
with a line naming the replacement.
