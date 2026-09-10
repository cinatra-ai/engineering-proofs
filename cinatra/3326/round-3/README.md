# Agents executions chart — rotated axis labels clear the legend (proof round 3)

Frames from a development boot at the pull request head 281a20f4a44a, the branch
brought up to date with the default branch a second time. Every bar in every
frame comes from an agent run dispatched through the product's own Run-agent
wizard on this boot; no row was written into the database.

Viewport 1600x1000, device scale 1, full window. Light and dark are the app's
own theme control.

## Cell 1 — one agent, a single bar

| file | theme | mean luminance | chart-card luminance |
|---|---|---|---|
| cell1-single-bar-light.png | light | 230.82 | 200.61 |
| cell1-single-bar-dark.png | dark | 29.73 | 68.80 |

Reading in the chart's own SVG: the rotated tick label "Author Agent" has
bottom 717.75; the "Run count" legend item has top 730.58 — a gap of 12.83 px.
The label ends 35.83 px above the chart container's bottom edge, so it is not
clipped. The clearance the chart reserves reads 3px at this one short label.

## Cell 2 — five agents, five bars

| file | theme | mean luminance | chart-card luminance |
|---|---|---|---|
| cell2-five-bars-light.png | light | 231.97 | 210.73 |
| cell2-five-bars-dark.png | dark | 32.60 | 67.34 |

Every tick label against the same legend top (730.58); the reserved clearance
reads 55px at five bars:

| label | label bottom | gap to the legend | room above the container edge |
|---|---|---|---|
| Agent Code Reviewer | 703.94 | 26.64 px | 49.64 px |
| Agent Lint Policy | 681.31 | 49.27 px | 72.27 px |
| Agent Planner | 670.00 | 60.58 px | 83.58 px |
| Agent Security Reviewer | 714.54 | 16.04 px | 39.04 px |
| Author Agent | 665.75 | 64.83 px | 87.83 px |

No label overlaps the legend and none is clipped by the chart container.

## Notes

- The wrench in the topbar is the app's development-only control, an artefact of
  the development boot this proof round used. It is not part of the change.
- dom-readings.jsonl is append-only: one entry per shutter, in order — four
  shutters, four frames, no re-shoot.
- The five runs each ended in a failed status; the chart counts dispatched runs,
  and each of the five carries a runtime task id, an execution attempt id and a
  trigger row of type immediate.
- The agent set on this boot differs from the earlier proof rounds: the five
  agents installed here are the ones the fresh boot ships with, so the tick
  labels read differently while the geometry under test is the same.
