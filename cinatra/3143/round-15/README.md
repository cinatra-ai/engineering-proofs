# Proof round fifteen — pull request 3143 (issue 3091, lifecycle D W3 media displays)

Head under proof: a5e8a7a365c839fd886277fc42d3185d07295f64 — a forward merge of the default branch onto the branch head, carrying the located fix of the json rows inside the review island body wrapper. Every frame in this folder was taken at that head on the running development boot; nothing is reused from an earlier round.

Window 1440x900 at device scale factor 2, so every file is 2880x1800. Both palettes are taken through the product's own theme control. `dom-readings.jsonl` carries one reading per shutter (appended, never rewritten) and `measurements.json` carries the file measurements (sha256, bytes, pixels, mean luminance, content-pane luminance) beside the reading of the same instant.

## What the frames show

- `cell1-pdf-artifact-page-*` — the artifact page of an uploaded PDF. Header, kind and revision line, and the embedded viewer drawing the bytes.
- `cell2-json-artifact-page-*` — the artifact page of an uploaded JSON file, drawn as a value tree.
- `cell4-text-artifact-page-*` — the artifact page of an uploaded plain text file, drawn through the content channel.
- `cell6-review-card-*` and `cell6-run-page-*` — the review surface and the run page of a real agent run whose gate pins six targets. The bands are consecutive shutters over the document; together they cover the whole island height with no unshot band, ending in the sixth target's body, the island's tail, the decision bar and the foot beneath it. The DOM reading of every band is taken inside the island's own document and reports the body text of all six targets.

The three files behind cells 1, 2 and 4 were put in through the product's own Upload control on this boot. The run behind cell 6 was dispatched fresh through the product's own run wizard and reached its pending review gate on its own; its rows are recorded in `measurements.json`.

## What is not shot, and why

- Cell 3 (the screenshot artifact page) — the facts row of that display needs a record of where the picture was taken, at what viewport and when. Of the thirty-one installed agent packs on this boot none declares a produces entry for the screenshot artifact type, so nothing here writes those facts. Recorded as a departure with that evidence; nothing substituted.
- Cell 5 (the widget rows) — sign-in inside the frame fails on a development boot through a filed host defect, cinatra#3330. Recorded as a pre-existing filed departure; nothing substituted.

## The road's own artefact

The round ran on a development boot, so the application's development-only control appears in the top bar. It is an artefact of the road, not part of any drawn surface, and it is not counted against any cell.
