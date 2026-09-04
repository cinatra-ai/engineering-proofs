# cinatra#3058 ninth proof round (issue #3051): the named review inside the widget

Proof round on a dev boot; frames at 1440x900 css, device scale 2, both palettes through the app's own theme control. Graded against the ratified drawing at design main 033a697c3fede6920bac3d4c61e08def57436f02.

| picture | cell | theme |
|---|---|---|
| v9-widget-review-first-paint-light.png | cell 1 — the named review inside the widget's thread at the gate, FIRST PAINT; run completed, gate pending | light |
| v9-widget-review-first-paint-dark.png | cell 1 — first paint of the named review in the widget | dark |
| v9-widget-review-settled-paint-light.png | cell 1 — the SETTLED PAINT of the same card (island reported loaded) | light |
| v9-widget-review-settled-paint-dark.png | cell 1 — settled paint | dark |
| v9-widget-review-after-reload-light.png | cell 2 — the same review AFTER the third-party page reloaded (reload at 05:51:41.523Z, frame signed itself in again) | light |
| v9-widget-review-after-reload-dark.png | cell 2 — the same review after the reload (reload at 05:51:52.545Z) | dark |
| v9-widget-review-decided-light.png | cell 4 — the review DECIDED from inside the widget (Approve on the card's own bar at 06:13:41.057Z); gate row read resolved/approve at 06:13:53.089Z | light |
| v9-app-own-surface-same-review-light.png | cell 5 — the host comparison: the same gate as the app's own run surface draws it, settled | light |
| v9-app-own-surface-same-review-dark.png | cell 5 — the host comparison, settled | dark |
