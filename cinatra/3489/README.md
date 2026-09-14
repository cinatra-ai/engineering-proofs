# Proof round — one step rail on the run page, and the parked step's own control

Pull request 3489. Every frame here was shot on a development boot of the branch at
head `69988cef2afda9b25316c235b01e8465e20306b5`, on a REAL agent run of the Blog Idea
Generator dispatched through the product's own Run-agent wizard with **Run right after
setup**, against a sealed provider. The run's Idea Context pause was answered on the
page; the run then wrote five blog ideas and a JSON artifact and is parked at its
review gate. Run id `869bb866-a5b8-4b1d-a945-60fab9462af8`; runtime task
`3ea3da45-de93-4825-bf1b-01ba701d5019`; execution attempt
`d6550eca-4a94-4def-8fc2-b4548ab9c829`; trigger row `immediate`.

Frames are the whole window at 1440x900, device scale factor 2 (2880x1800 pixels).
The palette is set through the app's own theme control; the framework's development
indicator is switched off through its own route before every shutter and its box is
read as 0 by 0 on every frame; the account band in the sidebar foot is painted over.
The app's own development-tools wrench in the topbar is the road's artefact — the
round runs on a development boot — and is not counted against any cell.

## Frames

| file | cell | palette | what it shows |
|---|---|---|---|
| `cell1-run-page-one-step-rail-light.png` | CELL1 | light | the parked run's page: ONE step rail column — Schedule (settled), Setup (settled), Review (the pause, reached and not settled), What this run made (not reached, no completed mark) — and the run detail beside it |
| `cell1-run-page-one-step-rail-dark.png` | CELL1 | dark | the same state in the dark palette |
| `cell2-parked-step-control-hit-tested-setup-step-showing-light.png` | CELL2 | light | the Setup step selected first through its own rail control, so the run detail shows Setup; the parked step's own control hit-tested at its own bounding-box centre, before the click |
| `cell2-parked-step-control-click-opens-the-review-in-place-light.png` | CELL2 | light | after a real pointer click at that centre: the review opened in place as that step's screen, the location still the run page, the one rail unchanged |
| `cell2-parked-step-control-hit-tested-light.png` | CELL2 | light | a first shutter pair, shot with the review already showing: the control hit-tested at its centre before the click |
| `cell2-parked-step-control-click-opens-the-review-light.png` | CELL2 | light | the same pair after the click — the location and the rail unchanged; superseded by the pair above, which shows the click's own effect |

## Readings

* `dom-readings.jsonl` — one appended reading per shutter: the address and the
  breadcrumb read from the page at the shutter, the count of rail columns and of
  merged inline rails, every rail entry in order with its reached and settled state,
  the hit test at the control's own centre, and the click's own record.
* `measurements.json` — per frame: sha256, bytes, pixels, mean luminance and the
  luminance of the named region (the one rail column for CELL1, the control's own box
  for CELL2's before-frames).
* `run-attestation.txt`, `database-readbacks.txt` — the run's own rows read back from
  the boot's database: the run with its runtime task and execution attempt, its
  trigger row, its two gates, and the pending review gate it is parked on.
* `recorder-dry-reading.json` — the recorder module loaded and its canonical index
  read; nothing was written.

## What the readings say

* One rail column and one merged inline rail on every frame; exactly one `Setup`
  entry and exactly one `Schedule` entry; the entries in order are Schedule (reached,
  settled, with its completed mark), Setup (reached, settled, with its completed
  mark), Review (reached, not settled — the pause) and `What this run made` (not
  reached, not settled, drawn with its numeral and no completed mark). No second
  column.
* CELL2: the topmost element at the control's own bounding-box centre is the control
  itself, and a real pointer click there opened the review as that step's screen while
  the address stayed on the run page and the rail's composition and order did not
  change. The opened surface carries no rail of its own.

## Not shot

Nothing of the two cells was left not shot.
