# Proof round sixteen — pull request 3143 (issue 3091, lifecycle D W3 media displays)

Head under proof: `55f43bd33269769b1bbbba6c5e93486111092d48` — the previous round's head brought up to date over the default branch twice, with the media packs' pins moved by the default branch. Every frame in this folder was taken at that head on the running development boot; nothing is reused from an earlier round.

Window 1440x900 at device scale factor 2, so every file is 2880x1800. Both palettes are taken through the product's own theme control. `dom-readings.jsonl` carries one reading per shutter (appended, never rewritten) and `measurements.json` carries the file measurements (sha256, bytes, pixels, mean luminance, content-pane luminance) beside the reading of the same instant. Every reading records the page URL and the breadcrumb text of the page in the frame.

## What the frames show

- `cell1-pdf-artifact-page-*` — the artifact page of an uploaded PDF, reached through the sidebar's Artifacts entry. Breadcrumb `Artifacts / w3-media-displays-proof-round-sixteen.pdf`, the header's mono meta line, and the embedded viewer drawing the bytes.
- `cell2-json-artifact-page-*` — the artifact page of an uploaded JSON file, drawn as a value tree through the content channel.
- `cell4-text-artifact-page-*` — the artifact page of an uploaded plain text file, drawn through the content channel.
- `cell6-review-card-*` and `cell6-run-page-*` — the review surface and the run page of a real agent run whose gate pins six targets. The bands are consecutive shutters over the document; together they cover the whole island height with no unshot band, ending in the sixth target's body, the island's tail, the decision bar and the composer foot beneath it. The DOM reading of every band is taken inside the island's own document and reports the body text of all six targets.

The three files behind cells 1, 2 and 4 were put in through the product's own Upload control on this boot. The run behind cell 6 was dispatched fresh through the product's own run wizard and reached its pending review gate on its own; its rows are recorded in `measurements.json`.

## What is not shot, and why

- Cell 3 (the screenshot artifact page) — the facts row of that display needs a record of where the picture was taken, at what viewport and when. On this boot 31 agent packs are installed and none declares a produces entry naming the screenshot artifact type, so nothing here writes those facts. Recorded as a departure with that evidence; nothing substituted.
- Cell 5 (the widget rows) — the connect road was walked through the product's own connector page: credentials were generated, the site's plugin fields were filled, and the approval screen was approved. The site never completed the token exchange back to the instance, so the site origin was never registered and the assistant embed still answers `content-security-policy: frame-ancestors 'none'`; the iframe is blocked and no widget mounts. Recorded with the reading of the failing step; nothing substituted.

## The road's own artefact

The round ran on a development boot, so the application's development-only control appears in the top bar. It is an artefact of the road, not part of any drawn surface, and it is not counted against any cell.

## Anomalies

- The agent runtime serving this boot answered 500 on every agent card at first (`TaskManager was not properly initialized`) while a sibling runtime on the same machine answered 200. One restart of this round's own runtime cleared it, and the dispatch that follows ran on the restarted runtime.
