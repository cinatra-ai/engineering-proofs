# First proof round — the closed access-scope picker's prefix on its real pages (#3523)

Round of 2026-09-17 on a development boot, at the pull request's pushed head
`c786905b642143806537e77eb557732d4b2f79e0`. Two counted cells, each in both
palettes, reached through the product's own navigation (sign-in page, then the
left sidebar entry, then the page's toolbar picker). No run was dispatched —
both cells are [no run].

## Frames

| file | cell | page | palette | state |
| --- | --- | --- | --- | --- |
| cell1-skills-scope-picker-closed-light.png | CELL1 | Skills directory | light | access-scope picker CLOSED |
| cell1-skills-scope-picker-closed-dark.png | CELL1 | Skills directory | dark | access-scope picker CLOSED |
| cell2-assistants-scope-picker-closed-light.png | CELL2 | Assistants directory | light | access-scope picker CLOSED |
| cell2-assistants-scope-picker-closed-dark.png | CELL2 | Assistants directory | dark | access-scope picker CLOSED |

Every frame is the whole window at 1440x900, uncropped, with the account band
painted over. The framework's development indicator was switched off through the
framework's own route before the first shutter (zero indicator elements at every
shutter). The topbar wrench is the development boot's own artefact and is not
counted against either cell.

## Readings

`dom-readings.jsonl` carries one appended reading per shutter: the page URL and
breadcrumb, the trigger's id and whole text, and the computed font-size,
text-transform, letter-spacing, color, font-family and flex of the prefix node
and of the value node beside it. `measurements.json` carries each frame's
sha256, byte size, pixel size, mean luminance and the luminance of the picker
region.

Both pages already drew the `Type: name` pair, so each closed trigger was shot
as the page drew it; the picker was never photographed open
(`aria-expanded` reads false at every shutter).
