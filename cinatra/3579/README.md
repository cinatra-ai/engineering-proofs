# Marketplace listing descriptions — proof round 1 at 0aa785a8

Frames from the real Marketplace listing grid at `/configuration/marketplace`, reached
through the product's own navigation on a development boot: sign-in, the app shell's
topbar Configuration control, the configuration index's Marketplace card and its
"Browse marketplace" link. Breadcrumb at every shutter: `Configuration › Marketplace`.
Viewport 1440x900. Both counted cells were read on the same page load, in the same
signed-in session, with the toolbar left exactly as the page draws it — no tab pressed,
nothing typed into the search control.

## Frames

| file | cell | palette | shows |
| --- | --- | --- | --- |
| `cell1-light.png` | CELL1 | light | the Chart card (`@cinatra-ai/chart-artifact`), whole in the window |
| `cell1-dark.png` | CELL1 | dark | the Chart card, whole in the window |
| `cell2-light.png` | CELL2 | light | the Twenty CRM card (`@cinatra-ai/twenty-connector`), whole in the window |
| `cell2-dark.png` | CELL2 | dark | the Twenty CRM card, whole in the window |
| `probe-dev-indicator.png` | throwaway probe | light | both bottom corners, after the framework's development indicator was switched off through its own route |

## What the frames show

CELL1 — the storefront cut this description short. The card's description paragraph draws
`Renders data charts in the Cinatra chat surface. Agents describe a chart as a small data
spec — a type (bar, line, or area),…` : zero named entity tokens, zero numeric entity
tokens, zero angle brackets, exactly one ellipsis character, and that character is the last
one in the text. Computed line clamp 3.

CELL2 — the storefront did not cut this description short. The card draws
`Connect Twenty CRM to Cinatra so your agents can look up companies and contacts and keep
your CRM records up to date.` character for character: zero entity tokens, zero angle
brackets, no ellipsis character anywhere. Computed line clamp 3.

## Recorded, not counted

The page header and its description line, the filter toolbar with its five tabs and the
search control, the 83 grid items drawn, every other part of both cards (name node and its
hover title, kind-and-vendor byline, price slot, install control, footer meta), and the
development wrench in the topbar, which exists only because this proof round ran on a
development boot. The screen's "Installing requires the package registry" notice was not
drawn — this boot's registry reads connected. No listing in the catalogue carried a markup
tag, so the tag-removal half of the change had nothing to exercise here and is not claimed.

The account band is painted over in every frame. No install, update, restore or
more-details control was pressed; no run was created.

`measurements.json` carries each frame's sha256, byte size, pixel size, mean luminance and
the luminance of the card region, plus the catalogue reading the two cards were chosen
from. `dom-readings.jsonl` carries one reading per shutter.
