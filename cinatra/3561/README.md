# Proof round 2 (cinatra#3552) — the Skills directory zebra band in both palettes

Two frames of the Skills directory, taken through the product's own navigation on a
development boot at the pushed head bb85839f468bbc6907c0a3bca85821ba8944208b of
cinatra#3561, window 1440x900, the account band painted over.

The head moved by one commit since proof round 1, and that commit touched only a stored
picture golden and no product file, so the same two cells were shot again at the pushed
head rather than re-claimed from the earlier round.

## Frames

- `cell1-skills-directory-zebra-band-dark.png` — CELL1, dark palette, counted.
  sha256 bde9c36d4671e992a3f2604a0e39c204ccd45902d079606ea774759a2d2e907c, 164227 bytes,
  1440x900, mean luminance 21.49.
- `cell2-skills-directory-zebra-band-light.png` — CELL2, light palette, recorded and not
  counted. sha256 3ed186e06dbea35d339a073fdf56e30d69fef67553ee004610cae26e05d3d01a,
  163122 bytes, 1440x900, mean luminance 229.96.

Both frames stand at the same scroll position, 116, with the same 28 body rows drawn and
ten of them whole inside the window; the table box reads x 273, y 90, width 1150.

## Readings

`dom-readings.jsonl` carries one appended line per shutter, and `measurements.json` the
per-file and per-region readings.

Dark frame: the alternate row's declared background is `oklab(0.278998 -0.00710082
-0.0403727 / 0.5)` over a transparent odd row; composited, the band region reads
rgb(16, 24, 43) against an odd-row region of rgb(2, 6, 24) and a page ground of
rgb(2, 6, 24). The five cell inks on that row read lab(98.1434 -0.369519 -1.05966) for
the Skill cell and rgb(144, 161, 185) for the extension, used-in, skill-id and
description cells.

Light frame: the alternate row's declared background is `oklab(0.928915 -0.00283852
-0.00929552 / 0.5)`; composited, the band region reads rgb(234, 236, 237) against an
odd-row region of rgb(241, 241, 237). The inks read rgb(21, 33, 58) for the Skill cell
and rgb(90, 100, 119) for the other four.

## Road

The framework's development indicator was switched off through its own route before the
clean, with every indicator box measuring 0 by 0, and the boxes were read again before
each shutter. The palette was changed between the two frames through the application's
own theme control, never by a query string or a device-preference override. Both cells
are pages the boot draws from its own data, so no agent run was started for this round
and none was needed.

The development wrench in the topbar is an artefact of a development boot and is not
counted against either cell. The portable package layer's identical token declaration is
proven by the pull request's own suite arms and not by a frame, because the application's
stylesheet does not import that token file.

No frame here is of the repository's fixtures page; that page was not opened at all.
