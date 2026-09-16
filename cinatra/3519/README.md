# Proof round 1 — the schedule card's terminal readings

Pull request cinatra-ai/cinatra#3519, candidate head 21a455f75ed5151ca7958a0c217638e0b35fdb46.
Every frame below was taken on a real, dispatched agent run of the Blog Idea Generator
agent, reached through the product's own navigation (Agents in the sidebar, the agent's
own Run control, the run wizard's schedule step "When should this run?").

## CELL1 — a spent one-off

A one-off schedule was set three minutes ahead and confirmed; it fired, the run went on
to its own Idea Context pause, and the schedule became a reading:

* `cell1-spent-one-off-light.png`
* `cell1-spent-one-off-dark.png`

The rows read `Run at 16.09.2026, 05:09` and `Timezone UTC` as plain, legible values.
No picker, no button, no floor: the card carried zero controls at the shutter.

## CELL2 — a stopped recurring schedule

A recurring schedule (repeat every 1 day at a time three minutes ahead) was confirmed,
fired once, and was then stopped with the card's own Cancel schedule and its in-card
confirmation ("Stop this recurring schedule? ... Keep schedule / Cancel schedule"):

* `cell2-stopped-recurring-light.png`
* `cell2-stopped-recurring-dark.png`

The rows read `Repeats Every day at 05:25` and `Timezone UTC`. Again no control and no
floor at the shutter.

## How each frame was taken

* Full application window, 1440 by 1500 at scale 2, through the signed-in session of the
  instance administrator account created for this proof round.
* Light and dark through the application's own theme control.
* The framework's development indicator hidden through the framework's own preference;
  no indicator element was visible at any shutter.
* The account band painted over in every frame.
* The DOM reading (URL, breadcrumb, card phase, rows, control count, box) was recorded in
  the same instant as each shutter and is in `dom-readings.jsonl`.
* `measurements.json` carries the file, sha256, byte count, pixel size, mean luminance and
  the card-region luminance of every frame.

The wrench in the top bar is the application's own development-only control; it is present
because the round ran on a development boot, and it is not part of either reading.
