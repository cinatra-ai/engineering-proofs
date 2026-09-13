# Proof round 2 — the review card over a real six-target gate (issue 3334, pull request 3433)

Head under proof: `8a2c82c79cd602fe727ca95c40d5d4aa5bd9d442`. Date: 2026-09-13.

## What was shot

One real agent run of the Blog Idea Generator Agent filed six artifacts in one
production, and the lifecycle raised one review gate over exactly six pinned
targets. The gate was still pending at this round, so the same real run of the
previous round was opened again — no new dispatch.

Every frame is the product's own review screen, reached through the product's
own navigation (Agents in the sidebar, then Reviews, then Open review), and
carries that page's breadcrumb `Agents > 3c753ab3... > Review` in the pixels.

Per palette the screen was opened once as a warm-up that is neither a repetition
nor a frame; the three measured repetitions follow it.

## Frames

| file | what it shows |
|---|---|
| `review-card-rep{1,2,3}-{light,dark}-wholepage.png` | the whole review page at the full document height, one per measured repetition and palette |
| `review-card-window-{light,dark}.png` | one window frame per palette, the card in the window |
| `review-card-panels-{light,dark}-scroll{01..06}.png` | the card's target region scrolled through its own six target bodies |

## The readings

Each repetition carries the island request, the response headers and the
document finish, in milliseconds from the page's navigation, read from the
page's own performance entries. All eighteen readings are in
`dom-readings.jsonl` and `island-timings.jsonl`; the measured file digests are in
`measurements.json`.

Across the six measured repetitions the island request left 11.7 to 13.7 s after
navigation, the response headers arrived 3.8 to 3.9 s after the request, and the
island document finished 8.6 to 10.1 s after the request — inside the twelve
second bound in every repetition. No failure plate and no "Try again" control
appears in any repetition, in either palette.

## What the whole-page frame cannot hold

The card mounts its six target bodies inside one region that is height-capped at
380 CSS pixels while its document is 1915 CSS pixels tall, so the region scrolls
inside itself. A whole-page frame of the review page therefore carries all six
immutable target headers — title, type, pinned revision, ownership level,
visibility, MIME and updated time — but only the first target body and the start
of the second. The `panels` frames carry the remaining bodies by scrolling that
region, so all six target bodies are in the pixels across the set. The capped
region is a property of the screen at this head, not of this round.

## Notes on the frames

- The three whole-page frames of a palette are byte-identical: three separate
  openings of the screen drew the same pixels.
- The framework's own development indicator was switched off through the
  framework's own route before every shutter; where a node was still in the
  document it was removed before the shutter, and no badge is in any frame.
- The topbar carries the application's own development-only wrench control. It
  exists only because this round ran on a development boot; it is the road's
  artefact and is not counted against the screen.
- The sidebar's bottom band is painted over in every frame.

## The gate this round photographed

Gate `f3e9c056-e290-4dbe-88a1-4f2f9c2a6ac0`, status pending, six pinned targets,
no disposition and no audit row written — the round decided nothing. The six
pinned revision identifiers on screen match the six rows behind the gate.
