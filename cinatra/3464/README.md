# Review floor proof round — pull request 3100 (issue 3080)

Seven frames from one proof round on a development boot at the pushed head
`1d61a1befc776f032c05936c55c7ac6bd7b0fe9f`. Every frame is a page reached through the
product's own navigation and carries that page's own breadcrumb; the framework's own
development indicator was switched off through the framework's own route before the first
shutter and read again immediately before every shutter (0 by 0 on all seven). The sidebar's
account row is painted over with the page ground colour in every frame. The topbar's
"Open development tools" wrench is the development boot's own artefact and is not part of any
cell. Viewport 1440 CSS pixels wide at device scale factor 2; light and dark through the
application's own theme control.

## The runs

Two real runs of the marketplace-installed Blog Idea Generator Agent were dispatched on this
boot: one through the agent's own Run-agent wizard (its review gate answers cells 1 to 3), one
from the assistant conversation (its review card is cell 4). Both produced a runtime task and an
execution attempt and raised a real review gate.

## The frames

| file | cell | palette | what it shows |
|---|---|---|---|
| cell1-review-page-pending-light.png | 1 | light | the pending review page of the wizard run; the decision floor reads Comment, Regenerate, Continue |
| cell1-review-page-pending-dark.png | 1 | dark | the same page, dark |
| cell2-run-page-review-step-pending-light.png | 2 | light | the same run's page with the Review step on the rail and the same three controls |
| cell2-run-page-review-step-pending-dark.png | 2 | dark | the same page, dark |
| cell3-run-page-settled-continued-light.png | 3 | light | after Continue: the settled marker below the whole card reads Continued, and the rail has moved on to "What this run made" |
| cell4-chat-review-card-floor-light.png | 4 | light | the review card drawn inside the assistant conversation, same three controls |
| cell4-chat-review-card-floor-dark.png | 4 | dark | the same card, dark |

No frame carries a Reject control and no frame carries an Approve control; the whole-page text
of every frame was scanned for both words and neither is present.

## Anomalies

- Three earlier cell 4 attempts were set aside under `superseded-attempts/`: the conversation
  list panel stayed open over the card's left edge, so the Comment control was partly covered.
  The delivered pair was shot after that panel was closed through its own Close control.
- In the cell 2 dark frame the review target inside the card is still an unresolved loading
  placeholder; the decision floor the cell is about is drawn and readable.
- The measurement of every delivered frame is in `measurements.json`; every shutter's own DOM
  reading is appended to `dom-readings.jsonl`, including the set-aside attempts.
