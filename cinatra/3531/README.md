# Proof round 1 — installed marketplace listings

Head under proof: 5414605604a06d63df6a48a7ff488d1cddf94408.
Instance: a production-built preview of that head. The frames draw no development
indicator and no development control; the readings record that too.

Page: Configuration then Marketplace, reached through the product's own navigation
after signing in on the product's own sign-in page. The account band is painted over.

## CELL1 — the six bundled listings draw the disabled Installed pill

No agent run was dispatched for this cell; the run table is empty.

| package | install row | control drawn | disabled |
|---|---|---|---|
| @cinatra-ai/chat-assistant-core-skill | 0.1.2, live | Installed | yes |
| @cinatra-ai/google-appointment-schedules-connector | 0.1.1, live | Installed | yes |
| @cinatra-ai/chart-artifact | 0.1.0, live | Installed | yes |
| @cinatra-ai/pdf-artifact | 0.1.1, live | Installed | yes |
| @cinatra-ai/image-artifact | 0.1.1, live | Installed | yes |
| @cinatra-ai/video-artifact | 0.1.1, live | Installed | yes |

Frames: `cell1-marketplace-six-bundled-listings-top-light.png` and
`cell1-marketplace-six-bundled-listings-top-dark.png`, both at the app's own
theme control, 2880 by 2800 pixels. Every one of the six cards sits inside the
visible window at the shutter; each card's box is in `dom-readings.jsonl`.

Grid reading at the shutter: 83 listing cards, 77 drawing Installed, 6 drawing
Install now.

## Readings beside the cell

- No card states a version: the pill reads the bare word Installed and no version
  string appears in any of the six cards.
- Five of the six listings still drawing Install now hold no install row at all,
  so that control is right for them.
- The storefront draws two listings named MCP Clients, one Installed and one
  Install now, stable across a reload.
- Several descriptions print a literal HTML entity instead of an ellipsis.

The last three readings sit outside this cell.
