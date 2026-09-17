# Marketplace listing card — the compatibility readings (proof round 1)

Head under proof: fbb1c598cfbb47abba2023f21fce4b32be0ac908

All four pictures are taken on a running development boot of that head, on the real page
reached through the product's own navigation — Configuration in the left sidebar, then
Extensions, then the Marketplace control. The address at every shutter is
`/configuration/marketplace` and the breadcrumb at every shutter reads
`Configuration > Marketplace`. No fixture page, no seeded row, no query string, no install.

## The pictures

| File | Cell | Palette | Shows |
| --- | --- | --- | --- |
| cell1-marketplace-grid-light.png | CELL1 | light | the marketplace grid as the boot draws it |
| cell1-marketplace-grid-dark.png | CELL1 | dark | the same grid in the dark palette |
| cell2-verdict-readings-light.png | CELL2 | light | the same page at its head, the verdict rows of the first grid rows whole in the window |
| cell2-verdict-readings-dark.png | CELL2 | dark | the same, dark palette |

CELL1 is the counted cell. CELL2 is recorded only.

## What the page draws

The grid holds 83 listing cards. Their verdict rows read:

- `Compatible` with a check mark on 30 cards — a plain mono row, 10px, the mark at 11px in the
  action accent, the label in the foreground ink, never wrapped and never a badge or pill.
- `Compatibility` — the word alone — with a question-mark mark on 53 cards, in the muted tone.
- The retired wording `Compatibility unknown` appears zero times on the page.

The third reading, `Incompatible` with a cross, could not appear here: not one listing in the
public storefront catalogue at this round's own time declares a host range this instance does
not satisfy (53 declare no range at all, 30 declare a range it satisfies). That reading is
therefore not shot on a page in this round and is not counted; it stands on the shipped work's
own rendered test, as the pull request records it.

## Recorded, not counted

- The install controls on the cards (54 read `Install now`, 29 read `Installed` and are
  disabled) belong to the merged marketplace change, not to this candidate.
- The card icon tiers, the vendor line, the price row and the rating row.
- The page chrome, and the development-only wrench control in the topbar, which exists only
  because the pictures are taken on a development boot.
- The drawing's own silence on the third reading, and its triangle mark on the incompatible
  line: a separate design change owns both.

The framework's own development indicator was switched off through the framework's own
preference before the first shutter, and zero of its elements were on screen at any shutter.
The account band is painted over in every picture. Each file's bytes, hash, pixel size, mean
luminance and region luminance are in `measurements.json`; every shutter's full page reading is
one line of `dom-readings.jsonl`.
