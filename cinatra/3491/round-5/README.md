# Proof round 5 — cinatra#3491 at 215f87e0

The review prompt window belongs to the run page's chrome. It is never drawn inside a
lifecycle screen or inside a lifecycle card, and inside a conversation the thread's own
composer is the request road, so no review prompt window is drawn at all.

Six frames, three cells, two palettes, taken on two real agent runs on a development boot
at the pushed head 215f87e0cf0d44b8f9af527590840e89cb6ffe33.

## The words, used here and nowhere loosely

- A **review prompt window** is the box the review gate draws outside a conversation. It is
  counted by its own anchor, a node carrying `data-conformance-id="review-prompt-window"`.
- The **chat's own composer** is the chat host's single primary input at the foot of the
  thread. It is never called or counted as a prompt window.
- The **floor's note field** is the decision floor's own text field, where the reader's note
  for the run and the audit trail goes. It is expected present and is never counted as a
  prompt window.
- The **page chrome's window host** is the run page's container node, marked
  `data-run-window-host="page-chrome"`.

## The frames

| File | Cell | Palette | Path | Reading |
| --- | --- | --- | --- | --- |
| cell1-chat-thread-zero-review-prompt-windows-one-composer-light.png | CELL1 | light | /chat/{org}/{assistant}/{threadId} | 0 review prompt window anchors on the page; 1 chat composer of the host's own |
| cell1-chat-thread-zero-review-prompt-windows-one-composer-dark.png | CELL1 | dark | /chat/{org}/{assistant}/{threadId} | the same, dark palette |
| cell2-chat-host-pending-review-card-drawn-light.png | CELL2 | light | /chat/{org}/{assistant}/{threadId} | the pending review card laid out 686 by 940, no hidden ancestor, 0 window anchors and 0 window send controls in the card root, the floor's note field present |
| cell2-chat-host-pending-review-card-drawn-dark.png | CELL2 | dark | /chat/{org}/{assistant}/{threadId} | the same, dark palette |
| cell3-run-page-one-review-prompt-window-in-the-page-chrome-dispatched-light.png | CELL3 | light | /agents/{org}/{agentSlug}/{runId} | exactly 1 review prompt window, mounted under the page chrome's window host, 0 window anchors inside any lifecycle screen or card, while the step screen holds input the person can manipulate |
| cell3-run-page-one-review-prompt-window-in-the-page-chrome-dispatched-dark.png | CELL3 | dark | /agents/{org}/{agentSlug}/{runId} | the same, dark palette |

`measurements.json` carries each frame's digest, byte count, pixel size, mean luminance,
the luminance of the region the cell fixes, and the DOM reading taken at the same instant.
`dom-readings.jsonl` carries one appended reading per shutter, including two earlier CELL3
frames that were not shot on an attested run and are therefore not part of this set.

## The two real runs

Both runs were dispatched through the product's own roads on this boot and both are
attested from the instance database on named columns alone.

- The conversation run, which CELL1 and CELL2 were shot on, was dispatched by naming the
  agent in one message typed into the thread's own composer.
- The run page's run, which CELL3 was shot on, was dispatched from the agent's own Run
  entry and parked on its own page.

Neither run id is one of the sixteen rows that existed before this round, and both rows
were created after the newest of those.

## Recorded, not counted

The card's composition, the review composition and the decision floor's wording are
pre-existing and filed under their own issues. The preview region of the review target
draws a loading placeholder rather than content. The decision floor reads Comment, Reject,
Approve. None of these touch the placement claims this round counts.

The development-only control in the topbar exists only because this round ran on a
development boot. It is the road's own artefact and is not counted against any cell. The
framework's own development indicator was switched off through the framework's own
preference before the first shutter and no element of it was drawn in any frame.

The account band is painted over in every frame.
