# Proof round 3 — issue #2702, the extension settings screen without the Skills section

Pull request: cinatra-ai/cinatra#3406
Head proved: ea9c8d5e49265f6c1aaba799d3492bcde34c01ce

Every cell is a no-run cell: the change is a retirement of a settings section, so no
agent run is needed and none was dispatched (the run table holds 0 rows).

Road: the administrator account signs in through the product's own sign-in page in a
headless browser; that session is reused for every frame. Frames at 1440x900 with a
device scale factor of 2, so each file measures 2880x1800 (the whole-page files are
taller). Both palettes are reached through the product's own Toggle theme control in
the topbar. The framework's own development indicator was switched off through the
framework's own route before the first shutter, and its box reads 0 by 0 under every
frame.

Subject: the installed agent extension `@cinatra-ai/web-research-agent`, opened from
Installed extensions by its own Settings action. Agent kind is the one kind whose
settings screen drew the retired Skills section.

## Frames

| File | Cell | Palette | What it shows |
| --- | --- | --- | --- |
| extension-settings-screen-agent-light.png | CELL1 | light | the extension settings screen at the window's own bounds |
| extension-settings-screen-agent-wholepage-light.png | CELL1 | light | the same screen, whole page |
| extension-settings-screen-agent-dark.png | CELL2 | dark | the extension settings screen at the window's own bounds |
| extension-settings-screen-agent-wholepage-dark.png | CELL2 | dark | the same screen, whole page |
| extension-settings-view-light.png | CELL3 | light | the settings view mounted against seeded props, window's own bounds |
| extension-settings-view-wholepage-light.png | CELL3 | light | the same view, whole page |

## Readings

The section headings of the settings screen in document order, read through the page
at each shutter:

Permissions, Execution, Marketplace, Maintenance, Danger zone

No heading, no row and no control of the settings screen reads Skills, and the
settings body text holds the word zero times. The section element the retired
section used to carry is absent from the document.

On the settings view (CELL3) the same four headings that apply to a connector are
drawn — Permissions, Marketplace, Maintenance, Danger zone — with no Skills heading,
row, control or section element. Four occurrences of the word appear in that view's
seeded text, all of them the extension KIND word: a seeded case labelled for a skill
package, its kind badge, and the Permissions note pointing at the separate Skills
configuration page. None of them is the retired per-agent section.

Note on the frames: the product's left navigation carries a Skills entry under TOOLS.
That is the instance-wide Skills surface, which this change does not touch; it is
outside the settings screen the cells grade.

Road artefact: the wrench in the topbar is the app's own development-only control. It
exists only because the round ran on a development boot, and it is not part of any
graded surface.

Measurements for every file — checksum, byte count, pixel size, mean luminance, the
luminance of the settings body column, and the full reading taken at each shutter —
are in measurements.json; the per-shutter log is dom-readings.jsonl.
