# Proof round — run detail, at the pushed head

Every frame is a whole-window picture of a REAL agent run dispatched through the product on this proof boot at the pushed head `13cced4191a3262f5033b2940e59029b7a19ab35`. That head is the forward merge of the default branch onto the previous round's head; none of this pull request's own files changed with it, and this round confirms the same readings at the live head so the proof is fresh.

Both palettes come from the app's own theme control. The round ran on a development boot per the standing dev-boot road; the topbar wrench control ("Open development tools") is that road's artefact and is never counted against any cell. The framework's own development indicator is hidden through the framework's own means and proven on the pixels — the development-portal box measures 0x0 on every reading, and the bottom-right 300x300 device region reads a flat 7 on every dark frame and a flat 241 on every light frame.

The runtime container carries the image whose output-schema composer matches the tree: 14 `additionalProperties` sites in both the container and the worktree source.

## Frames

| file | cell | palette | run | what it shows | verdict |
|---|---|---|---|---|---|
| CELL1-pending-gate-whole-run-detail-light.png | CELL1 | light | 8cb2ffdb | the whole run detail parked on the pending review gate: the rail, the gate header `Review requested` with the pill `Awaiting your decision`, the review targets rendered, the decision bar closing the card, and the prompt window beneath the card | PASS |
| CELL1-pending-gate-whole-run-detail-dark.png | CELL1 | dark | 8cb2ffdb | the same state at rest with the review targets rendered (no placeholder), dark palette | PASS |
| CELL2-completed-run-one-card-findings-list-light.png | CELL2 | light | b8444f23 | a completed run of an agent that declares no review step: the pill `completed`, ONE surface in the detail column, and the structured result rendered inside that one card as the titled list `Findings`; no entry marked current | PASS |
| CELL2-completed-run-one-card-findings-list-dark.png | CELL2 | dark | b8444f23 | the same, dark palette | PASS |
| CELL3-decided-gate-settled-entry-and-prompt-window-light.png | CELL3 | light | 8cb2ffdb | the same run after its gate was decided through the card's decision bar: the settled entry keeps its place and reads the drawing's settlement word `continued`, zero entries marked current, and the prompt window is drawn beneath the decided card, outside its frame | PASS |
| CELL3-decided-gate-settled-entry-and-prompt-window-dark.png | CELL3 | dark | 8cb2ffdb | the same, dark palette | PASS |
| CELL4-two-ordered-steps-waiting-at-first-light.png | CELL4 | light | 6a88c3f3 | a real run whose rail carries two ordered steps, read while it waits at the FIRST: exactly one entry marked current, the second drawn but not highlighted, each entry its ordinal glyph plus one label | PASS on the rail items; see the note on the road below |
| CELL4-two-ordered-steps-waiting-at-first-dark.png | CELL4 | dark | 6a88c3f3 | the same, dark palette | PASS on the rail items; see the note below |

## The checklist, measured on these frames

1. **The prompt window is beneath the card, outside its frame.** On CELL1 and CELL3 the card frame is a `section` with a 16 px radius and a 1 px border; the prompt window's mount sits 16 px below its bottom edge, `promptWindowInsideReviewCardFrame` reads false, and the mount is the last element of the detail column with no siblings after it.
2. **The card ends with its decision bar.** CELL1 draws the header, the review targets and the decision bar inside the one frame and nothing after it; CELL3's decided card ends with its resolution floor.
3. **Every rail entry is one label plus its drawn state.** CELL1 `Setup` / `Review` / `What this run made`; CELL2 `Setup` / `What this run made`; CELL3 `Setup` / `Review` + `continued` / `What this run made`; CELL4 `Select blog idea` / `Review blog draft`. The machine-word probe `/[A-Z_]{6,}/` is empty on every rail entry of every frame; no second line, no reason sentence and no machine code appears anywhere on the rail.
4. **The current-step marker.** Exactly one entry carries it on CELL1 and CELL4; zero on CELL2 and CELL3.
5. **The settled entry reads the drawing's word.** On both CELL3 frames the settlement reads `continued`.

## The CELL4 road — recorded, not substituted

The fleet package that declares two review steps in order cannot reach its first review step on this instance: its account-scope step has no list to pick and its only affordance for making one opens a route that answers 404. CELL4 is therefore shot on the real, attested run of the pipeline package that has stayed parked at the first of its two ordered steps — the state the cell asks for. Nothing was written, seeded or substituted anywhere; the run carries a runtime task id, an execution attempt id and a trigger row.

## Departures recorded, not graded here

- CELL4's entries carry the step ordinal glyph beside the label (`1` `Select blog idea`, `2` `Review blog draft`); the reading reports the glyph and the label as two text nodes of the one entry.
- The gate on CELL1 carries six pinned targets under one header and one rail entry; the drawing raises one gate per artifact.
- The decision bar draws `Comment`, `Reject` and `Approve`; the drawing's affordances are `Continue`, `Regenerate` and `Comment`.
- The note field is labelled with a decision-aware caption naming approve and reject; the drawing's field is one type-agnostic note.
- The decided card on CELL3 still carries the header `Review requested`; the hold pill is correctly gone and the resolution line reads `Approved by ...`.
