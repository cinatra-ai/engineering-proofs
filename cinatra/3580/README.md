# Proof round — installed extensions list, skill cards (cinatra#3580, issue #3569)

Head under proof: 23aa67b1008c9244bd1ca31087ffe3d49414358b. Development boot, 1440x900, headless, both palettes through the app's own theme control.

Every frame comes from the product's own navigation: sign-in, the app shell's topbar Configuration control, the configuration index's Installed link. No address was typed. No run was created — this surface lists what the instance already has.

## What the two counted cells claim

- CELL1 — the default Active view at `/configuration/extensions`: the number of skill cards drawn equals the number of distinct package names among the canonical skill install rows whose status reads `active`.
- CELL2 — the All view at `/configuration/extensions?tab=all`, reached by pressing the toolbar's own status filter once: the number of skill cards drawn equals the number of distinct package-and-status-class pairs among the canonical skill install rows of every status.

## What was read

The instance's own canonical install rows, read by named columns in the same minute as each cell's first shutter: eight skill rows, eight distinct package names, every one `active`, platform scope, no organisation.

The page drew 94 installed-extension cards in total, eight of them with the byline kind label `Skill`, and the eight Settings destinations name exactly those eight packages — one card per package, none missing and none extra, on both views and in both palettes.

## Frames

| File | Cell | View | Palette | Shows |
| --- | --- | --- | --- | --- |
| cell1-light-a.png | CELL1 | Active | light | seven whole skill cards |
| cell1-light-b.png | CELL1 | Active | light | the eighth whole skill card |
| cell1-dark-a.png | CELL1 | Active | dark | seven whole skill cards |
| cell1-dark-b.png | CELL1 | Active | dark | the eighth whole skill card |
| cell2-light-a.png | CELL2 | All | light | seven whole skill cards |
| cell2-light-b.png | CELL2 | All | light | the eighth whole skill card |
| cell2-dark-a.png | CELL2 | All | dark | seven whole skill cards |
| cell2-dark-b.png | CELL2 | All | dark | the eighth whole skill card |
| probe-dev-indicator.png | — | — | light | throwaway probe frame, both bottom corners clear |

The skill block does not fit one window, so each cell's frames are consecutive whole-window frames of that block, each with its own reading. No counted card is cropped.

## Hygiene

The framework's development indicator was switched off through its own route before the first shutter; the probe frame's bottom corners were looked at and are clear, and the indicator box read 0 by 0 before every shutter. The account band is painted over in every frame. The development wrench in the topbar is the artefact of a development boot and is counted against nothing.

`dom-readings.jsonl` holds one reading per shutter. `measurements.json` holds each file's sha256, bytes, pixels, mean luminance and region luminance. `dom-readings-superseded-first-attempt.jsonl` belongs to a first set of frames of this same proof round whose top card sat under the sticky header; those files were deleted and re-shot under new names rather than kept as stand-ins.
