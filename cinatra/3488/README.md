# Proof round — the review card in a conversation draws no prompt window

These frames were taken on a development installation of the candidate build, on a
real agent run: the Blog Idea Generator agent was asked for in the chat assistant,
ran on the configured model provider, produced five blog ideas and parked at its
review gate. Nothing here is seeded or mocked.

## What each frame shows

- `cell1-chat-review-card-light.png` / `-dark.png` — the conversation with the
  parked review card, first window (1440 x 900).
- `cell1-chat-review-card-whole-light.png` / `-dark.png` — the same conversation in
  a taller window (1440 x 1500), the whole card visible with the thread's own
  composer at the foot.
- `cell1-chat-review-card-floor-light.png` / `-dark.png` — the same conversation in
  a 1440 x 2000 window: the card from its header down to its decision floor
  (Comment, Reject, Approve) and the thread composer below it.
- `cell2-review-page-light.png` — the same gate on the run's own review page,
  first window (1440 x 1600).
- `cell2-review-page-whole-light.png` — the review page in a 1440 x 2400 window,
  the whole card visible including the prompt window at its foot.

## The reading

Inside the conversation the card root carries no prompt window and no send
control; the only prompt window on the page is the thread's own composer at the
foot ("Type a message..."). On the review page — outside a conversation — the same
card does draw its prompt window ("Ask Cinatra about this review, or ask for
changes to the work..."). The card's decision floor is unchanged on both surfaces.

Each frame was taken through the product's own navigation, with the palette set
through the app's own theme control and the framework's development indicator
turned off through the framework's own route. The account band at the foot of the
sidebar is painted over. The wrench in the topbar is the app's own development
tools control; it is present because this is a development installation and is not
part of what these frames are about.

`measurements.json` records every file's sha256, byte size, pixel size, mean
luminance and the luminance of the card region. `dom-readings.jsonl` records the
reading taken in the same instant as each shutter.
