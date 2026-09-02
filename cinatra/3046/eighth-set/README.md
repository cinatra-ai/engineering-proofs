# cinatra pull request 3046 — eighth proof round (2026-09-01)

Issue 3007. Head `7654ce04cc83`. 26 frames, 1440x900 at device scale 2, light and dark. Two real runs of the blog draft writer dispatched from the chat, each watched on four surfaces opened BEFORE its review gate existed and never touched again. Frames carry neutral fixture identities only.

The round is reported exactly as it measured, passes and failures together.

Before the gate exists — the four watched surfaces at rest:

- `v8-conversation-swap-light-before.png` / `-dark-before.png` — run 1's conversation, opened before the gate and left alone.
- `v8-run-page-swap-light-before.png` / `-dark-before.png` — run 1's run page, the same.
- `v8b-conversation-swap-light-before.png` / `-dark-before.png` — run 2's conversation, opened before the gate.
- `v8b-run-page-swap-light-before.png` / `-dark-before.png` — run 2's run page, the same.

The review arriving in place, with nothing pressed:

- `v8b-conversation-swap-light-after.png` / `-dark-after.png` — run 2's conversation 14.4 s after the gate row was written: the review replaced what stood in the same turn, no navigation and no reload. This is the round's PASS.
- `v8b-settled-conversation-light.png` / `-dark.png` — the same card once the decision was given: `Review approved`, no decision controls left.

What did NOT arrive, shot as measured absences:

- `v8b-run-page-on-schedule-step-no-review-slot-light.png` / `-dark.png` — run 2's run page drew no review at all; it had followed the run to its schedule step.
- `v8b-run-page-on-schedule-step-at-run-completion-light.png` / `-dark.png` — the same page at the moment the run finished.
- `v8-standing-conversation-answered-ask-card-20s-after-mint-light.png` / `-dark.png` — run 1's conversation 20 s after its gate was written: still only the already-answered question.
- `v8-standing-run-page-answered-ask-card-20s-after-mint-light.png` / `-dark.png` — run 1's run page at the same instant, the same reading.
- `v8b-conversation-card-absent-flash-light.png` / `-dark.png` — run 2's conversation after the review had landed, at an instant where it had left the untouched thread again.

The waiting box while a run is parked:

- `v8-run-completed-placeholder-names-run-still-spinning-conversation-light.png` / `-dark.png` and `-run-page-light.png` — the box names its own run (`23b42f48`) in the picture, and is still working at an instant when the run's own row already reads finished.
- `v8-run-completed-stale-ask-card-run-page-dark.png` — the fourth of those surfaces never reached that reading and still drew the answered question.
