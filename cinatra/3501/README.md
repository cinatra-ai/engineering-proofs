# Proof round — the review floor on a real run

Frames from one real agent run on a development boot of the candidate head
1eee5448b8aa5c37a247ee38bf6a9bf99bf5943b.

**In simple words:** an agent was started from the product's own Run-agent wizard, it
produced blog ideas, and the pages where a person decides what happens to that work were
photographed. Every decision place now offers the same three choices — Comment,
Regenerate and Continue — and nothing else. There is no Reject and no Approve. After
Continue was pressed with a real pointer click, the page settled to a marker that reads
"Continued" and names the act rather than a person, and the run moved on to its next
review step.

Each page was reached by clicking through the product itself: Agents in the sidebar, then
the Reviews or Executions listing, then the run. No test harness page appears in any
frame. Both palettes were set through the product's own theme control. The account band
at the foot of the sidebar is painted over.

| File | Cell | Palette | What it shows |
| --- | --- | --- | --- |
| cell1-review-page-floor-v2-light.png | 1 | light | The pending review page of the run: the decision floor reads Comment, Regenerate, Continue beside the note field. |
| cell1-review-page-floor-v2-dark.png | 1 | dark | The same page and the same three controls. |
| cell2-run-page-review-step-light.png | 2 | light | The run's own page on the one rail, its Review step current, the same three controls. |
| cell2-run-page-review-step-dark.png | 2 | dark | The same step and the same three controls. |
| cell3-continued-settled-marker-light.png | 3 | light | After a real pointer click on Continue: the settled marker "Continued" under the whole card, and the rail entry now reading "Review · continued" with the next review step ahead. |

Cell 4 asked for the same floor on the review card drawn inside a chat conversation. At
this head no such card is drawn for this run: the assistant conversation reached from Chat
in the sidebar holds no thread and no review card, and the conversation and run-message
tables are empty. The cell is recorded as not shot, with that reading, rather than filled
from any other page.

Measurements for every file — checksum, byte count, pixel size, mean luminance and the
luminance of the decision-floor region — are in measurements.json. The reading taken at
each shutter is in dom-readings.jsonl.

Two things seen in passing, neither of them the subject of this round: one artifact
preview panel reported "The preview did not load" in a single light frame of cell 2 and
offered a retry, which the page itself says does not block the decision; and the wrench
in the topbar is the development-only control that exists because these frames were shot
on a development boot.
