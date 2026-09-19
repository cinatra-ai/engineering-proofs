# Round 1 — cinatra#3598 — the Upload Extension screen, its repository form and the resolved install panel

Proof round at candidate head 588913a509118f7d2e1224a1889695cc24579aa1, on a development boot.

Three counted cells, each read in both palettes through the app's own theme control, each DOM reading taken before its shutter, each graded region brought whole into the window before the shutter fired. Every frame comes from the product's own navigation — the sign-in page, then the app shell's topbar Configuration control, then the configuration index's Extensions card and its Installed link, then the control labelled Upload in the installed screen's own toolbar. No fixtures-harness page was opened, shot or read; no component test render was used; no typed address was used where a trail exists.

All frames are 1440 by 900, full window, with the account band painted over.

## Cells

- **CELL1** — the Upload Extension screen at rest on its File tab.
  - `cell1-upload-screen-file-tab-light-r2.png`
  - `cell1-upload-screen-file-tab-dark-r2.png`
- **CELL2** — the repository-link tab's form at rest: nothing typed, nothing pressed, no lookup started.
  - `cell2-github-repository-form-light-r2.png`
  - `cell2-github-repository-form-dark-r2.png`
- **CELL3** — the File tab with a real package archive resolved, showing the resolved install panel.
  - `cell3-resolved-install-panel-light-r2.png`
  - `cell3-resolved-install-panel-dark-r2.png`

`probe-indicator-r2.png` is the throwaway probe frame taken after the framework's development indicator was switched off through its own route, so both bottom corners could be looked at before the first counted shutter. It is not a counted frame.

`superseded-attempt1/` holds an earlier attempt's frames, set aside unaltered because its first cell pair was shot with the screen header scrolled out of the window. Those files are not frames of this record; the whole session was re-run and every counted frame above comes from that second session. No frame file was overwritten after its reading was recorded.

## Files beside the frames

- `dom-readings.jsonl` — one appended reading per shutter and per supporting reading, in order.
- `measurements.json` — per frame: sha256, bytes, pixel size, mean luminance and the graded region's box and mean luminance.
- `preflight.txt` — the proof preflight's own lines.

## The package the round resolved

A real archive cut from this head's own pinned pack tree, written into a fresh output directory outside every repository tree. Its manifest declares `@cinatra-ai/list-curation-skill` at version `0.1.0`, kind `skill`, display name `List Curation Skill`. Nothing was planted, edited, replayed or substituted.

## What the round did not do

Nothing was installed. The install control was never pressed, no repository lookup was ever started, nothing was typed into either repository field, and the installed-extension rows were read by named columns before and after the panel was cancelled and were identical both times.

## Result

All three counted claims passed at 95 percent in both palettes. Departures recorded but never counted: the resolved panel's name field taking the package name where the drawing binds it to the manifest display name (cinatra#3204); the File road's own content-digest line, which stands where the drawing's example draws the repository road's pinned-at-commit and provenance rows; the absence of the upload-consent block, which the product draws only where the workspace opt-in is on; and the product's own development-tools control in the topbar, which exists because this round ran on a development boot.
