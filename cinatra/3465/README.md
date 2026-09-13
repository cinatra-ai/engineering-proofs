# Connector Sharing tab — identity row for a ceiling connector's own save

Proof round for cinatra#3460, shot on a development boot at head `b8c0956300124745dc94e88cb08e9cce76793230`,
stacked on the Sharing tab branch (`2ac1a342e3c5`). Every frame is the product's own page, reached through the
product's own navigation: the sidebar Connectors entry, the OpenAI connector card, then that page's tab strip.
Both palettes come from the app's own theme control in the topbar. No fixtures page, no seeded rows.

The connection the frames show was saved through the connector's OWN Setup form (API key typed into the shipped
form, Connect pressed). At the branch base that save wrote no identity row and the Sharing tab listed nothing;
at this head the same save registers the identity row, so the tab lists the connection.

## Frames

| file | cell | palette | shows |
| --- | --- | --- | --- |
| `cell1r3-openai-connector-sharing-tab-light.png` | 1 | light | the Sharing tab: one panel for `cinatra-openai`, no roll-up card, the Access picker on the stored value, the ceiling line, Save changes |
| `cell1r3-openai-connector-sharing-tab-dark.png` | 1 | dark | the same state |
| `cell2-openai-connector-connected-status-light.png` | 2 | light | the same page's Setup tab: the Connection status card reads Connected |
| `cell2-openai-connector-connected-status-dark.png` | 2 | dark | the same state |

`superseded/` holds two earlier pairs of cell 1 shot before the page was returned to its top; the pair above is
the cell's frame pair. `dom-readings.jsonl` appends one reading per shutter (URL, breadcrumb, tab strip, panel
boxes, picker text, ceiling line, Save changes box). `measurements.json` carries each file's digest, byte size,
pixel size, mean luminance and the luminance of the region the cell names.

## What the readings say at the shutter

- URL `/connectors/cinatra-ai/openai-connector/setup`, breadcrumb `Connectors / Cinatra / OpenAI`,
  tab strip `Setup · Sharing · Help`.
- Panel count 1, roll-up absent — the roll-up heads the tab only above several connections.
- Access picker text `Workspace: Admins only`; the line beneath it reads
  `Locked by this connector: access is limited to workspace admins (only:"admin").`
- Save changes present; the Ownership panel lists the signed-in account.

## A scope change through the picker was not shot

This connector declares a sharing ceiling, so its picker is locked on the stored value and a scope change through
it is not offered. That state is the cell the round could shoot, and it is shot; a saved-and-re-read scope change
belongs to a connector without a ceiling.

## The road's own artefact

The round ran on a development boot, so the app's development-only topbar control is present in the window. It is
the road's artefact, not part of any drawn region, and the framework's own indicator is switched off through the
framework's own route before the first shutter.
