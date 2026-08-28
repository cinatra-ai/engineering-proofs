# cinatra — pull request 3064

Full-window captures (1440×900 at device scale 2, light and dark through the app's own theme control) of the widget inside a third-party page: a schedule stated in the widget's own conversation renders the scheduling card in the turn, and Confirm arms exactly one run under the widget's own credential. Every frame is from a real run with the real provider; the run and trigger rows, the brokered request and the DOM readings are on the pull request.

| file | requires | shows | verdict |
|---|---|---|---|
| `widget-schedule-card-pending-light.png` | the scheduling card in the turn, and only that: "When should this run?" over three rows, the chosen row owning its fields, the duration beneath, the floor Confirm; no cron field, no summary, no status label | one card after the assistant's line; Schedule for later chosen with Run at 09/15/2026 09:30 AM and Europe/Berlin; duration row; Confirm | PASS |
| `widget-schedule-card-pending-dark.png` | the same card in the dark palette | the same reading; widget region dark | PASS — the chosen row's edge is light in dark (the palette's primary token, on every dark surface) |
| `widget-schedule-card-decided-light.png` | the same card in place after Confirm, rows still shown, the floor Save changes, no second card, nothing summarised | the same card, same rows, Save changes drawn quiet, no Confirm | PASS |
| `widget-schedule-card-decided-dark.png` | the same settled card in the dark palette | the same reading; widget region dark | PASS — same palette note |

Observations, not defects of this change: the duration row reads "Unavailable." (no estimate exists for an agent that has not run); the host page's own heading is clipped at the top edge by a small scroll offset in the capture, its paragraph and embed log still in frame.
