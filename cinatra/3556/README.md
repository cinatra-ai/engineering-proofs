# Proof round 2 — the review the run owes, drawn in the conversation

These frames come from one real agent run on a development boot of the candidate at
18a2e74ba9893186e910733dd9f1025b394ede4f, met first in the assistant conversation it was
dispatched from and then on its own run page. No decision control of the review floor was
pressed at any point: the review is still owed in every frame.

## Frames

- `cell1-chat-thread-review-card-light-v2.png` — the review card a reader meets inside the
  assistant conversation, light palette. Graded.
- `cell1-chat-thread-review-card-dark-v3.png` — the same reading, dark palette, reached
  through the app's own theme control. Graded.
- `cell2-run-page-review-slot-light-v4.png` — the same run's own run page review slot,
  light palette. Recorded, not graded.

## What the frames show

The card is drawn whole in the conversation, with its decision floor live
(Comment, Reject, Approve) and its status reading "Awaiting your decision". Its root
publishes the chat-thread host with a pending state, and no ancestor between that root and
the transcript carries `hidden`, `aria-hidden="true"` or a stand-down name. On the run page
the same card is drawn in the run's review slot under the run-card host.

## Recorded, not graded

- The answered schedule record stays in view above the review card; it is the record of a
  schedule that has already fired.
- The artifact preview region inside the card reads "The preview did not load" in the
  conversation frames and a loading placeholder on the run page. That region belongs to the
  installed artifact package's own display, not to this change.
- The development wrench in the topbar exists only because these frames were taken on a
  development boot.
- The account band is painted over in every frame.

## Readings beside the frames

`dom-readings.jsonl` holds one reading per shutter: the path at the shutter, the card
root's conformance id, host, state and box, the root's ancestor chain up to the transcript
with each ancestor's display, `hidden`, `aria-hidden` and stand-down name, and the count of
elements carrying a host declaration with each value. `measurements-frames.json` holds each
file's sha256, size, pixel size, mean luminance and the luminance of the card region.
