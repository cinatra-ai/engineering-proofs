# Proof round 2 — cinatra#3536 at 8b54c3ddb57e2b0bea3dfa9548a70921ff981b2b

The marketplace grid page reached through the product's own navigation: Configuration in the
left sidebar, then Extensions, then the Marketplace control. Breadcrumb at every shutter:
Configuration / Marketplace. Path: /configuration/marketplace. No run was dispatched.

## Frames

| file | cell | palette | pixels | mean luminance |
| --- | --- | --- | --- | --- |
| cell1-marketplace-grid-light.png | CELL1 (counted) | light | 2880x2000 | 213.54 |
| cell1-marketplace-grid-dark.png | CELL1 (counted) | dark | 2880x2000 | 39.36 |
| cell2-verdict-readings-light.png | CELL2 (recorded) | light | 2880x2000 | 212.61 |
| cell2-verdict-readings-dark.png | CELL2 (recorded) | dark | 2880x2000 | 38.81 |

## What the page drew

83 listing cards, each with one verdict node. 30 read `Compatible` with a check mark; 53 read
`Compatibility` with a question-mark circle. The retired wording counted zero on the page. The
catalogue at this round's time offered no listing declaring a range the instance does not
satisfy, so the incompatible reading could not occur on the page and was not shot; it stands on
the rendered test recorded in the pull request.

Anatomy of the verdict node, identical in both palettes: a plain row, mono face at 10px, the mark
11px beside its word, never wrapped, no pill and no background. The check carries the accent; the
third reading is drawn in the muted tone.

## Recorded, not counted

The install controls, the card icon tiers, the vendor line, the price and rating rows and the page
chrome are not drawn by this candidate. The development-tools control in the topbar is an artefact
of the development boot this round ran on. The drawing's missing third reading and its triangle on
the incompatible line belong to the separate design follow-on.
