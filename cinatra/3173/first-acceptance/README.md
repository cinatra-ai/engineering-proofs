# cinatra pull request 3173 — first acceptance capture (2026-09-02)

Issue 2368. Head under test `d571a94bff6d`. Driven on a live Google connection, headless at 1440x900 with device scale 2, full window, both palettes through the product's own theme control. The record for this set is [the first acceptance record](https://github.com/cinatra-ai/cinatra/pull/3173#issuecomment-5503717027).

- `vr3-ac1-listed-with-calendar-badge-light.png` / `-dark.png` — the schedule stored from the connector's own setup screen, listed with its Calendar badge after a page load; the booking-page link text is not rendered in the list.
- `vr3-ac1-list-after-delete-empty-light.png` / `-dark.png` — the list after the host-authorized delete, back to its empty state, with the removal banner.
- `vr3-connected-status-before-chat-half-light.png` / `-dark.png` — the Google connection read as Connected before the assistant half of the round.
- `vr3-connected-status-after-chat-half-light.png` / `-dark.png` — the same connection read as Connected after the assistant half.

Frames held back on purpose, and why: every frame carrying the booking-page link text stays unpublished, because the link is input data rather than product behaviour — that is the pending-state pair and the whole first-round chat set. The calendar-picker pair stays unpublished too: the live option list names other people's calendar addresses. Both readings are measured in full in the record above.

All frames are 2880x1800 pixels, at rest, one file per state, no frame re-shot or overwritten.
