# Connector Sharing tab — proof round 2

Eight frames, four cells, both palettes. Every frame is a real product page reached
through the product's own navigation (sidebar Connectors, then the connector's card,
then the Sharing tab) and carries that page's breadcrumb and tab strip. The framework's
own development indicator was switched off through its own route before the first
shutter (the route answered 204 each time) and is absent from every frame.

## Cells

### cell3 — the Sharing tab with one saved connection

`cell3-openai-sharing-one-connection-light.png` / `-dark.png`

The OpenAI connector's Sharing tab. One connection is saved, so the list starts with
that connection's own panel and no summary card stands above it. The panel carries the
connection name and its mono line with no status badge and no per-row action; beneath
it the access picker sits on the stored value, the connector's ceiling sentence sits
under the picker with a lock, and one right-aligned Save changes closes the card.

### cell3b — the Sharing tab with two saved connections

`cell3b-mcp-servers-sharing-two-connections-rollup-light.png` / `-dark.png`

The MCP Servers connector's Sharing tab after two external servers were registered,
each with an API key, through that connector's own Setup form. Two connections are
saved, so the summary Connections status card heads the list (no Check, no all-connections
link) with both panels beneath it, each panel deciding its own access.

### cell4 — a scope change saved and read back

`cell4-mcp-servers-scope-saved-workspace-all-reread-light.png` / `-dark.png`

The same page after the second connection's access was changed through its own picker
from Personal: Only me to Workspace: All, saved, and the page loaded again. The frame
shows that second panel with its picker on the saved value; the first panel is unchanged
on Personal: Only me with its recommendation line. The two frames differ from the cell3b
frames by 86218 (light) and 88400 (dark) pixels.

### cell6 — the ceiling a connector declares

`cell6-openai-sharing-locked-ceiling-picker-light.png` / `-dark.png`

The OpenAI connector declares a ceiling. The frame shows its access picker open: the
options above the ceiling are drawn unavailable, the two at or below it are selectable,
and the current value is ticked. The ceiling sentence itself is read under the picker in
the cell3 frames of the same page.

## Readings

`dom-readings.jsonl` holds one appended reading per shutter: the page path, breadcrumb,
tab strip, every panel box with its access picker, scope line and Save changes box, the
summary card box, the palette, the scroll position and the window size. `measurements.json`
holds each file's sha256, byte size, pixel size, mean luminance and the luminance of the
panel region named by its cell.

## What was read back from the product's own store

The connection identity rows show the two external registrations and the provider
connection. The access grant row for the connection changed in cell4 reads workspace
visibility and no longer carries the seeded-default marker, while the untouched
connection still reads the seeded default.


Note: in every picture the sealed administrator's address on the Ownership row is painted over with the card's own background (it carried an internal account name, not product content); nothing else is changed. The originals and their checksums are in the pull request's record.
