# cinatra pull request 3192 — design fixtures (2026-09-02)

Issue 3189, first audit leg: the button, the select and the card graded clause by
clause against their own sections in the components drawing. Head `4c5fa1cb726c`
(the two files below are unchanged from `c117cfb26bb8`, the commit that regenerated
them).

These two files **are** the pixel baselines committed on that pull request, copied
byte for byte out of its head — not a separate rendering made for this folder. The
pixel-diff check compares every future render of the fixtures page against exactly
these bytes, so they are the proof and the contract at once.

- `design-fixtures-light.png` — the fixtures page in the light palette, 1280 x 6550.
- `design-fixtures-dark.png` — the same page in the dark palette, 1280 x 6550.

## What the page shows

The fixtures page is the product's own catalogue of its shared building blocks: the
semantic token swatches, the placeholder rows for newer components, and then every
core primitive drawn once at rest. The three blocks this leg graded each get one row
in the "Core primitives" section:

- **Button** — the seven variants in one row: primary, outline, secondary,
  destructive, ghost and the link form.
- **Card** — two cards side by side: the presentation card on the warm cream ground,
  and the new clickable form on the white ground that lifts 1px on hover.
- **Select** — the trigger drawn with the input chrome it now mirrors: white ground,
  7px corner, 32px box.

Everything else on the page is the regression surface. Every other primitive renders
in the same two frames, so a change to a shared block that moved something it should
not have would show up here.

## Why these two files moved

The card primitive now draws a real 1px border where it drew a ring, so every card
grows 2px in each dimension and its content re-lays out by 1px; the select trigger
picks up the input chrome, which makes it shorter, tighter and filled. The button
change is an alias and leaves no residual at all.

The delta was read region by region before it was adopted: 28,041 residual pixels in
light and 28,013 in dark, in the same regions at the same offsets in both palettes —
six card boundaries, the token swatch tiles, the extension card, the card and select
primitive rows, and the table, pagination and empty-state content that re-centres
inside a card that lost 2px of inner width. No region outside the card and select
families moved.

## The graded record

The per-clause tables live on issue 3189: twenty-two clauses, fourteen conforming and
eight fixed, with native-select recorded as not applicable because the drawing has no
section for it.
