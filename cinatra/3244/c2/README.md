# Pull request 3244 — second proof round (2026-09-06)

Issue #3214: every schema-config connector's setup page draws the drawing's two columns, the Connection status card and the Connect / Disconnect pair, probe-declaring or not.

Frames, 1440x900 CSS at device scale 2, light and dark through the app's own theme control, the framework's development indicator off on pixels:

- `cell1-reshoot-at-rest-probeless-appointment-schedules-setup-two-columns-{light,dark}.png` — the frames of record for cell 1: the appointment-schedules connector (no status probe) drawn in two columns with the Connection status card.
- `cell2-reshoot-at-rest-openai-setup-two-columns-connect-disconnect-disabled-{light,dark}.png` — the frames of record for cell 2: a probe-declaring connector, the same shape, Connect and Disconnect side by side with Disconnect disabled.
- `cell3-check-flow-checking-badge-spinning-{light,dark}.png` and `cell3-check-flow-resolved-disconnected-{light,dark}.png` — the Check flow: the spinning Checking… badge, then the resolved badge.
- `cell4-disconnect-confirmation-dialog-{light,dark}.png` — the disconnect confirmation.
- `cell1-probeless-…` and `cell2-openai-…` without `reshoot-at-rest` — the first shutters, superseded by the frames of record above.

`measurements.json` and `dom-readings.jsonl` carry the readings taken at each shutter. The full record is the bot comment on the pull request.
