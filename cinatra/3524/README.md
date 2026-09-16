# Proof round — the review floor on one real run

Frames from a single real agent run on a development boot of the candidate head
d609f3d141aa837869de084c7855c0730b181244.

**In simple words:** a person asked the assistant, in their own words, to run the Blog
Idea Generator. The run was scheduled and started from the conversation itself, it wrote
three blog ideas, and it then asked for a decision. Every place where that decision can be
made — the card drawn inside the conversation, the run's own page, and the review page —
offers the same three choices: Comment, Regenerate and Continue. There is no Reject and no
Approve anywhere. After Continue was pressed with a real pointer click, the run's rail
entry reads "Review · continued" and the card in the conversation settles and stops
offering the floor.

The card inside the conversation is the point of this round: at the earlier head no such
card was painted at all, and here it is drawn, whole, with its floor.

Each surface was reached by walking the product itself: Chat in the sidebar for the
conversation, and Agents in the sidebar then the Executions and Reviews listings for the
run and the review. No test page appears in any frame. Both palettes were set through the
product's own theme control. The account band at the foot of the sidebar is painted over.

| File | Cell | Palette | What it shows |
| --- | --- | --- | --- |
| cell1-chat-review-card-painted-whole-v8-light.png | 1 | light | The review card drawn inside the conversation, whole: its header, the three blog ideas it made, and the floor reading Comment, Regenerate, Continue. |
| cell1-chat-review-card-painted-whole-v8-dark.png | 1 | dark | The same card and the same three controls. |
| cell1-chat-review-card-painted-v7-light.png | 1 | light | The same card closer in, with the note field and the floor. |
| cell1-chat-review-card-painted-v7-dark.png | 1 | dark | The same, in the dark palette. |
| cell2-run-page-review-step-light.png | 2 | light | The run's own page with its Review step current and the same three controls. |
| cell2-run-page-review-step-dark.png | 2 | dark | The same step and the same three controls. |
| cell3-review-page-floor-light.png | 3 | light | The review page of this run: the same three controls beside the note field. |
| cell3-review-page-floor-dark.png | 3 | dark | The same page and the same three controls. |
| cell4-continued-settled-marker-light.png | 4 | light | After a real pointer click on Continue: the run's rail reads "Review · continued" and the next review step stands ahead. |
| cell4-continued-settled-marker-dark.png | 4 | dark | The same rail entry in the dark palette. |
| cell5-chat-card-departed-light.png | 5 | light | Back in the conversation after the decision was taken there: the card is settled, its decision floor is gone and its header no longer awaits a decision. |
| cell5-chat-card-departed-dark.png | 5 | dark | The same settled card in the dark palette. |

Measurements for every file — checksum, byte count, pixel size, mean luminance and the
luminance of the decision-floor region — are in measurements.json. The reading taken at
each shutter is in dom-readings.jsonl, which is written one line per shutter and also
holds the readings of frames that were re-shot and not kept.

Two things seen in passing, neither of them the subject of this round: the artifact
preview panel inside the conversation card reported "The preview did not load" in several
frames and offered a retry, which the page itself says does not block the decision; and the
wrench in the topbar is the development-only control that exists because these frames were
taken on a development boot.
