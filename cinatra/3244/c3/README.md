# Pull request 3244 — third proof round (2026-09-06)

Issue #3214: every schema-config connector's setup page draws the ratified drawing's two columns, the Connection status card and the Connect / Disconnect pair, probe-declaring or not. This round proves the setup pages are unchanged at the fix-leg-3 head 674d98ddf9c10d55ecc90c975fb86adda2193c3a (the crumb publisher's contributions restored).

Frames, 1440x900 CSS at device scale 2, light and dark through the app's own theme control, the framework's development indicator off on pixels.

Frames of record:

- `cell1-corrected-reading-at-rest-probeless-appointment-schedules-setup-two-columns-{light,dark}.png` — CELL1: the appointment-schedules connector (no status probe) in two columns with the Connection status card.
- `cell2-corrected-reading-probe-declaring-openai-setup-two-columns-connect-disconnect-disabled-{light,dark}.png` — CELL2: a probe-declaring connector, the same shape, Connect and Disconnect side by side with Disconnect disabled while not connected.
- `cell3-check-flow-checking-badge-spinning-{light,dark}.png` and `cell3-check-flow-resolved-badge-{light,dark}.png` — CELL3: the spinning Checking… badge, then the resolved badge.
- `cell4b-connected-at-rest-openai-setup-disconnect-enabled-{light,dark}.png` and `cell4b-disconnect-confirmation-dialog-on-a-connected-connector-{light,dark}.png` — CELL4: the connector genuinely connected with Disconnect enabled, then the drawn confirmation dialog.

Superseded, kept on the record: `cell1-at-rest-…` and `cell2-probe-declaring-…` (the early-gate pair and the first CELL2 pair — good pixels, three reading defects the early grade named, fixed in the corrected pairs) and `cell4-disconnect-confirmation-dialog-{light,dark}.png` (the dialog reached through the page's own Connect with a placeholder value — the connector was NOT genuinely connected there, and an error toast is in frame).

`measurements.json` carries every frame's sha256, bytes, pixels, mean luminance, the three region luminances and the DOM reading taken at that shutter; `dom-readings.jsonl` is the append-only shutter log; `early-grade.json` is the independent early grade. The full record is the bot comment on the pull request.
