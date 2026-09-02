# cinatra pull request 2998 — title-mirror proof round (2026-09-02)

Issue 2934. Head `1d33d3acaa2d`. Full record: pull request 2998, comment 5505743463.

Eight frames, full window 1440 by 900 at device scale 2, both colour themes through the
application's own theme control, every frame at rest and in its own file. Each frame carries
its own readings on pixels: the browser-tab string, the drawn trail, the route and the
crumb-to-sidebar gutter. One real run under a real provider, one neutral fixture person.

- `vt-tab-mirrors-trail-run-page-light.png` / `-dark.png` — the run's own page: the trail reads `Agents > Blog Draft Writer Agent (1)` and the tab reads `Blog Draft Writer Agent (1) | Cinatra`, the trail's last crumb plus the product suffix.
- `vt-tab-cold-typed-entry-light.png` / `-dark.png` — the same address typed straight into a fresh browser context that had never navigated inside the application; at rest the tab and the trail read the same words.
- `vt-tab-review-open-gate-light.png` / `-dark.png` — the review page of an open gate: trail `Agents > Agent run > Review`, tab `Review | Cinatra`. The middle crumb reads the fixed word `Agent run` — a departure named in the record and tracked, not a defect of this round.
- `vt-trail-left-edge-regression-light.png` / `-dark.png` — regression smoke on the agents list: the crumb row's left edge is the sidebar's inner edge plus the standard gutter (256 + 32 = 288). This page is not id-bearing and still draws trail `Run agent` against tab `Agents` — the small divergence the round named and deliberately left.

No raw identifier reaches the tab or the crumb words on any frame: every three-or-more-character
substring of the run id and of its five parts was tested against both, with zero hits everywhere.
