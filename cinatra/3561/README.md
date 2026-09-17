# Proof round 1 — the Skills directory zebra band in both palettes

Two frames of the Skills directory, taken through the product's own navigation on a
running development boot at the candidate head 8362727364116583a654c7f5a62b6e528755c506,
at 1440x900, each frame whole with the same eight body rows in the window.

| file | cell | palette | what it shows |
| --- | --- | --- | --- |
| cell1-skills-directory-dark.png | CELL1 (counted) | dark | the alternate-row band and the ink on it |
| cell2-skills-directory-light.png | CELL2 (recorded, not counted) | light | the same eight rows in the light palette |

Readings taken at each shutter are in dom-readings.jsonl; file hashes, pixel sizes and
the colour measurements are in measurements.json.

Band and ink, measured from the pixels of the frames themselves:

- dark: band rgb(16, 24, 43) against the page ground rgb(2, 6, 24); the Skill cell reads
  16.9:1 on the band and the four muted cells 6.72:1.
- light: band rgb(234, 236, 237) against the ground rgb(241, 241, 237); the Skill cell
  reads 13.52:1 and the four muted cells 5.03:1.

The page drew 28 body rows; the breadcrumb read Skills and the path was /skills at both
shutters. No agent run was dispatched for either cell — both are pages of the installed
fleet. The development wrench in the top bar is an artefact of the development boot the
round ran on and is not part of what either frame is about.

The portable package layer carries the same declaration; that half is proven by the
suite arms of the change and not shot here, because the application stylesheet does not
import that token file.
