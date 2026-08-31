# cinatra PR 3074 — fourth capture

Six frames from two real runs, captured through the application's own theme control in both light and dark. Each frame is a full-page screenshot at 2880x1800.

- `v4-run-made-pill-light.png` — sha256 `b3e39c31206e4a6cc5e603a806e12f46a5a49af92295131f137290517399cc22` — a completed blog-draft-writer run, light theme: the "What this run made" panel pairs its title with a Completed pill, and the artifact detail line wraps across two lines with the file type fully legible and no ellipsis.
- `v4-run-made-pill-dark.png` — sha256 `2d37df65128dc4b9d3e321a7166461ea27a4723b750af5e30b59ad5017d92d6f` — the same run and panel in dark theme: the same Completed reading holds, and the sidebar footer showing the signed-in person is visibly non-blank against the empty ground above it.
- `v4-default-road-before-decision-light.png` — sha256 `d3caa15291d0f809360eab90ffe535f2bd4a42e66e7d5fa8cfe1d96a67d91181` — an author-agent run with its review gate still open, light theme: the step reads completed, the gate reads pending, and the trailing "run made" entry reads upcoming rather than resolved, matching the page's own "Awaiting your decision" state.
- `v4-default-road-before-decision-dark.png` — sha256 `eacee2d26464b2d91ccb0776b845d0d2b0c2bce1a8838fbdcebfee1e780d6f4c` — the same run and gate state in dark theme, with the same step/gate/entry reading.
- `v4-default-road-after-decision-light.png` — sha256 `f0693f456baa8d22955756dc2cf1ebf3e0e933bd5e07c5043d768ea38edccb5c` — the same run after the review decision, light theme: the step, the gate, and the trailing entry all read resolved, and the page no longer shows "Awaiting your decision" — the rail and the page agree.
- `v4-default-road-after-decision-dark.png` — sha256 `ad54f456d4efb077323da6b92745f14b3adcbe74471a8e7f0863dcca9bdac228` — the same post-decision state in dark theme, with the same resolved reading across step, gate, and entry.

`measurements.json` carries the full per-frame reading behind each line above: pixel dimensions, region luminance, the on-page text read at shutter time, and the run identifiers each frame was taken against.
