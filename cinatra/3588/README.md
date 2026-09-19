# Round 1 — a required start field on a run's setup step (cinatra#3588, at f4190d3b)

Four counted frames and one throwaway probe frame, all taken on a development boot
through the product's own navigation: Agents in the sidebar, the Blog Idea Generator
Agent's own card, its Run control, then the run's own page parked on its setup step.
No control that submits the field's value was pressed, so no work step of the run ran.

The account band is painted over in every frame. The framework's development indicator
was switched off through its own route before the first shutter; the probe frame shows
no badge in either bottom corner. The wrench in the topbar is the development boot's own
control and is not part of any claim.

| file | cell | palette | shows |
| --- | --- | --- | --- |
| cell1-blank-required-field-light.png | CELL1 | light | the field's box empty, its label "Brief *", the step's Continue unavailable |
| cell1-blank-required-field-dark.png | CELL1 | dark | the same, in dark |
| cell2-typed-answer-light.png | CELL2 | light | a real sentence in the same box, the same Continue available, no error line |
| cell2-typed-answer-dark.png | CELL2 | dark | the same, in dark |
| probe-indicator-off.png | (probe) | light | the Agents page, used only to look at both bottom corners |

Readings: dom-readings.jsonl (one line per shutter). Measurements: measurements.json.
