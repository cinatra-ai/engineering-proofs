# Proof round — run detail, fix leg 6, at the pushed head

Every frame is a whole-window picture of a REAL agent run dispatched through the product on this proof boot at the pushed head `38b8e77cc1469e572b2b40470e32f0cabd30f6a6`. Both palettes come from the app's own theme control. The round ran on a development boot per the standing dev-boot road of 2026-09-03; the topbar wrench control ("Open development tools") is that road's artefact and is never counted against any cell. The framework's own development indicator is hidden through the framework's own means and proven on the pixels — the development-portal box measures 0x0 on every reading and the dark frames' bottom-right 300x300 device region reads a flat 7 (the light frames a flat 241).

The runtime container carries the image whose output-schema composer matches the tree: 14 `additionalProperties` sites in both the container and the worktree source.

## Frames

| file | cell | palette | run | what it shows | verdict |
|---|---|---|---|---|---|
| CELL1-pending-gate-whole-run-detail-light.png | CELL1 | light | 4038051f | the whole run detail parked on the pending review gate: the rail, the gate header `Review requested` with the pill `Awaiting your decision`, the review targets rendered, the decision bar closing the card, and the prompt window beneath the card | PASS |
| CELL1-pending-gate-whole-run-detail-dark.png | CELL1 | dark | 4038051f | the same state at rest with the review target rendered (no placeholder), dark palette | PASS |
| CELL2-completed-run-one-card-findings-list-light.png | CELL2 | light | b8444f23 | a completed run of an agent that declares no review step: the pill `completed`, ONE surface in the detail column, and the structured result rendered inside that one card as the titled list `Findings`; no entry marked current | PASS |
| CELL2-completed-run-one-card-findings-list-dark.png | CELL2 | dark | b8444f23 | the same, dark palette | PASS |
| CELL3-decided-gate-settled-entry-and-prompt-window-light.png | CELL3 | light | 4038051f | the same run after its gate was decided through the card's decision bar: the settled entry keeps its place and reads the drawing's settlement word `continued`, zero entries marked current, and the prompt window is drawn beneath the decided card, outside its frame | PASS |
| CELL3-decided-gate-settled-entry-and-prompt-window-dark.png | CELL3 | dark | 4038051f | the same, dark palette | PASS |
| CELL4-two-ordered-steps-waiting-at-first-light.png | CELL4 | light | 6a88c3f3 | a real run whose rail carries two ordered steps, read while it waits at the FIRST: exactly one entry marked current, the second drawn but not highlighted, each entry its ordinal glyph plus one label | PASS on the rail items; see the note below on the road |
| CELL4-two-ordered-steps-waiting-at-first-dark.png | CELL4 | dark | 6a88c3f3 | the same, dark palette | PASS on the rail items; see the note below |

## The three subjects of this leg, measured on these frames

1. **The settled entry reads the drawing's word.** On both CELL3 frames the settled entry's text content is `Review` plus the settlement `continued` — the drawing's own word. The machine-word probe `/[A-Z_]{6,}/` is empty on every rail entry of every frame; no second line, no reason sentence and no machine code appears anywhere on the rail.
2. **A structured result renders as a titled findings list inside the one completion card.** CELL2 draws one surface in the detail column; the JSON result is rendered inside it under the heading `Findings` as a list, and the plate pill reads `completed`.
3. **The prompt window is drawn beneath a decided gate.** On CELL3 the prompt window's mount sits 16 px below the card frame's bottom edge, `promptWindowInsideReviewCardFrame` reads false, and the mount is the last element of the detail column with no siblings after it — the same measurement as on the pending gate in CELL1.

## The two findings of the earlier refusal, measured again

- The prompt window is NOT inside the review card's frame: on CELL1 and CELL3 the card frame is a `section` with a 16 px radius and a 1 px border; the mount is 16 px below its bottom edge and is the detail column's last child.
- Every rail entry is one label: CELL1 `Setup` / `Review` / `What this run made`; CELL2 `Setup` / `What this run made`; CELL3 `Setup` / `Review` + `continued` / `What this run made`; CELL4 `Select blog idea` / `Review blog draft`. Exactly one entry carries the current-step marker on CELL1 and CELL4, zero on CELL2 and CELL3.

## The CELL4 road — recorded, not substituted

The round attempted the fleet package that declares two review steps in order (recipients, then drafts). Two real runs of it were dispatched through the product's own wizard on this boot:

- the first walked past both review steps because the account-scope step had no contact list to pick, so neither review was ever raised;
- the second is parked at its account-scope step; its only affordance for making a list opens a route that answers 404 on this instance, so it cannot reach its first review step. That run has no trigger row, so it is not an attested run and NOTHING was shot for it.

Two fresh dispatches of the pipeline package at this head also failed before their gate, both with the same recorded error from the passthrough call (`selectedIdeaJson` not a parseable object after the idea was selected at the pick step). CELL4 was therefore shot on the real, attested run that was dispatched on this same boot and has stayed parked at the first of its two ordered steps ever since — the state the cell asks for. No state was written, seeded or substituted anywhere.

## Departures recorded, not graded here

- CELL4's entries carry the step ordinal glyph beside the label (`1` `Select blog idea`, `2` `Review blog draft`); the reading reports the glyph and the label as two text nodes of the one entry.
- The gate on CELL1 carries six pinned targets under one header and one rail entry; the drawing raises one gate per artifact.
- The decision bar draws `Comment`, `Reject` and `Approve`; the drawing's affordances are `Continue`, `Regenerate` and `Comment`.
- The note field is labelled with a decision-aware caption naming approve and reject; the drawing's field is one type-agnostic note.
- The decided card on CELL3 still carries the header `Review requested`; the hold pill is correctly gone and the resolution line reads `Approved by ...`.
