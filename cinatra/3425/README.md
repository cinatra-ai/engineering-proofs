# Proof round 1 — issue #2738 / pull request 3425

The connector setup page's Help tab drew its read-only how-to prose inside a card
container. The ratified connectors drawing, section II, draws no card, panel or
chrome around that prose: it sits directly on the page ground at the Narrow width,
flush under the Wide tab strip, Help always last, read-only, no form and no Save.
These frames are the Help tab at the pushed head 21a9db7198c5ddd31ca02a1736a7a6c0517b3d0e.

Graded against app-connectors section II (drawing revision 09208ad2e81a) and the
issue's sentences. Window 1440x900 at a 2x device pixel ratio, both palettes
switched through the application's own Toggle theme control.

## Frames

| file | cell | palette | state |
| --- | --- | --- | --- |
| cell1-appointment-help-tab-r2-light-masked.png | CELL1 | light | Help tab of the google-appointment-schedules connector setup page |
| cell1-appointment-help-tab-r2-dark-masked.png | CELL1 | dark | same state, dark palette |
| cell2-calendar-help-tab-light-masked.png | CELL2 | light | Help tab of the google-calendar connector setup page |
| cell2-calendar-help-tab-dark-masked.png | CELL2 | dark | same state, dark palette |

The `-masked` files are the ones for publication: the sidebar account row carries a
machine-derived label, and a solid block covers it. The unmasked files of the same
names are the round's own record. `dom-readings.jsonl` holds one reading per shutter
and `measurements.json` the per-file measurements.

## What the pages read through the DOM

Both connectors, both palettes:

- tab strip labels in order: Setup, Help — Help is the last tab, and it is the
  selected tab in every frame
- the prose container computes to 576px wide (the Narrow width), left-aligned under
  the tab strip; its top sits 24px (CELL1) and 32px (CELL2) below the strip's bottom
- the prose container itself has a 0px border, `box-shadow: none` and a transparent
  background, and no ancestor between it and the page ground carries a border, a
  shadow or a background different from the page ground — the list of such ancestors
  is empty in all four readings
- no card, panel, rounded or shadowed element renders inside the Help tab panel
- no form, input, textarea, select or switch renders on the tab, and there is no
  Save control (the tab carries no button at all)

## Notes

- The framework's own development indicator is switched off through the framework's
  own route before the page renders; its box reads 0x0 before every shutter, and a
  70x70 corner crop taken immediately before each shutter is a single uniform value,
  so no badge is painted in any published frame. The first pair of CELL1 was shot on
  a load where the route had been called on that same load; the badge still painted,
  so that pair was deleted and re-shot under new names (the `-r2` files).
- The application's own development-only topbar control (the wrench) is visible in
  every frame. It exists only because this proof round ran on a development boot and
  is not counted against any cell.
- Both cells need no agent run, so none was dispatched.
- Neither connector's strip carries a Sharing tab, which the drawing makes fixed on
  every connector. That is a pre-existing departure outside this issue's scope:
  recorded, not counted.
