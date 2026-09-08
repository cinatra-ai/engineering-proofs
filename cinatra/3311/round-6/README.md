# Sixth proof round — cinatra#3311 (issue #3029)

Candidate: b72c2d8d3d1917fff56fe21831c84172c631cf7b
Graded against the ratified drawing at design main 033a697c3fede6920bac3d4c61e08def57436f02,
specs/app-artifact-review.html sections I.2 and V.2.
Every frame: whole window, 1440x1200 at deviceScaleFactor 2 (2880x2400 pixels), taken on a
development boot per the 2026-09-03 decision. The topbar wrench ("Open development tools") is
that road's own artefact and is never counted against a cell. The framework's own development
indicator is off through the framework's own means and absent on the pixels of all eight frames.

| frame | cell | palette | what it shows | verdict |
|---|---|---|---|---|
| cell1-run-made-listed-rows-light.png | CELL1 | light | the last step of a real run whose undeclared end-node outputs above the floor were picked up: two bordered rows (written solid, used dashed with the Used tag), title 13px, type tag 10px, fact line 10px with 0.04em, the Open control, the Finished pill, one rail whose last entry is the run's record | PASS |
| cell1-run-made-listed-rows-dark.png | CELL1 | dark | the same state in the dark palette | PASS |
| cell2-run-made-empty-reading-light.png | CELL2 | light | a real run that made nothing: the empty reading verbatim under the heading at 12.5px, the Finished pill, zero rows, no empty panel, one rail | PASS |
| cell2-run-made-empty-reading-dark.png | CELL2 | dark | the same state in the dark palette | PASS |
| cell3-artifact-page-opened-from-row-light.png | CELL3 | light | the artifact page opened from the listed row's own control, at the top of the page: the artifact of the base the ladder chose (JSON), its content and its size | PASS with a recorded reading |
| cell3-artifact-page-opened-from-row-dark.png | CELL3 | dark | the same state in the dark palette | PASS with a recorded reading |
| cell4-uploaded-bytes-download-card-light.png | CELL4 | light | an uploaded file of undetectable bytes above the floor: the BINARY kicker, application/octet-stream, 2048 bytes, and the download card with the file name, its form, its size and the download — never the floor | PASS with a recorded departure |
| cell4-uploaded-bytes-download-card-dark.png | CELL4 | dark | the same state in the dark palette | PASS with a recorded departure |

Readings: dom-readings.jsonl (one appended line per shutter, plus one supplementary
reading taken without a shutter). Measurements: measurements.json.

Recorded, not counted against a cell:
- CELL3: the artifact page draws no "revision N" text. The revision the run filed is drawn on
  the run page row ("revision 1") and stands in the store as representation revision 1 filed by
  the same run.
- CELL4: the download card carries a fourth line the drawing does not give it ("The form of this
  file could not be determined. Download it to open it."). It reports no failure, so it does not
  turn the card into the floor.
- CELL4: the specimen file is the one carried over from an earlier round; it is not a stale frame.
