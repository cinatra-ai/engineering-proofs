# Proof round 1 frames — shared primitives on the product's own screens (#3189)

Every frame below was taken through the product's own navigation on a running
development build at the candidate head, in both palettes, switched through the
application's own theme control. No fixtures page, no component test render and
no harness breadcrumb appears in any frame; the path recorded at each shutter is
listed beside it. The account band is painted over in every frame. The
framework's development indicator was switched off through the framework's own
route before the first shutter and measured 0 by 0 at every shutter.

The wrench in the topbar is the application's own development-only control. It
is present because the frames were taken on a development build, and it is not
part of any graded primitive.

## Counted cells

| Frame | Primitive | Screen path | Palette |
| --- | --- | --- | --- |
| CELL1-sidebar-collapsed-rail-light.png | Sidebar, collapsed icon rail | /workspace | light |
| CELL1-sidebar-collapsed-rail-dark.png | Sidebar, collapsed icon rail | /workspace | dark |
| CELL2-select-trigger-vs-input-r2-light.png | Select trigger beside the form text input | /projects/new | light |
| CELL2-select-trigger-vs-input-r2-dark.png | Select trigger beside the form text input | /projects/new | dark |
| CELL3-switch-control-box-light.png | Switch control box | /configuration/access-control | light |
| CELL3-switch-control-box-dark.png | Switch control box | /configuration/access-control | dark |
| CELL4-toggle-group-filter-rail-light.png | Toggle group filter rail | /notifications | light |
| CELL4-toggle-group-filter-rail-dark.png | Toggle group filter rail | /notifications | dark |
| CELL5-scroll-area-command-list-light.png | Scroll bar of the command list | /workspace | light |
| CELL5-scroll-area-command-list-r2-dark.png | Scroll bar of the command list | /workspace | dark |

The select trigger is drawn by the new-project form only once an ownership level
of team or organization is chosen, so that radio was chosen on the unsubmitted
form to reach it. The form was never submitted and nothing was written. Neither
switch on the access-control screen was pressed, because each writes a real
platform setting; both are shown at the state the screen drew them.

## Recorded, not counted

| Frame | What it records | Screen path | Palette |
| --- | --- | --- | --- |
| CELL6-toggle-recorded-light.png | Toggle chrome as it reaches a real screen — only as the toggle group's item | /notifications | light |

CELL6 is its own shutter with its own reading taken on the toggle group's item.
It shows the same screen as the light frame of CELL4 and its pixels are
identical to it.

The one-time-code primitive has no frame, because no real page draws it. Its
only render sites in the tree are the repository's own conformance fixtures
module and its own drawing checklist, neither of which is a real screen:

    grep -rln "components/ui/input-otp" src --include=*.tsx
    src/app/design-fixtures/conformance/primitive-wave-leg2-fixtures.tsx
    src/components/ui/__tests__/input-otp-drawing-conformance.test.tsx

Its clauses are proven by that checklist and by the repository's own design
suite, not by a picture.

## Files beside the frames

- `dom-readings.jsonl` — one appended reading per shutter: the path and query at
  the shutter, the breadcrumb the chrome drew, the computed values each cell
  names, and the development-indicator box.
- `measurements.json` — per frame: sha256, bytes, pixel size, mean luminance and
  the luminance of the named region.

Two earlier shutters were discarded rather than kept: a select-trigger pair taken
before the ownership radio was chosen, which did not contain the primitive, and a
scroll-bar frame named dark whose palette had not in fact changed because the
open command list covered the theme control. Both were re-shot under new file
names, which is why the kept select and dark scroll-bar frames carry `r2`.
