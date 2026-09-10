# Agents executions chart — rotated axis labels clear the legend (proof round 2)

Frames from a development boot at the pull request head c74f0bf3ca5d, the branch
brought up to date with the default branch. Every bar in every frame comes from
an agent run dispatched through the product's own Run-agent wizard on this boot;
no row was written into the database.

Viewport 1600x1000, device scale 1, full window. Light and dark are the app's
own theme control.

## Cell 1 — one agent, a single bar

| file | theme | mean luminance | chart-card luminance |
|---|---|---|---|
| cell1-single-bar-light.png | light | 232.54 | 209.50 |
| cell1-single-bar-dark.png | dark | 28.63 | 63.01 |

Reading in the chart's own SVG: the rotated tick label "Blog Idea Generator
Agent" has bottom 713.32; the "Run count" legend item has top 730.58 — a gap of
17.26 px. The label ends 40.26 px above the chart container's bottom edge, so it
is not clipped. The clearance the chart reserves reads 64px at one bar.

## Cell 2 — five agents, five bars

| file | theme | mean luminance | chart-card luminance |
|---|---|---|---|
| cell2-five-bars-light.png | light | 232.16 | 212.68 |
| cell2-five-bars-dark.png | dark | 32.48 | 65.87 |

Every tick label against the same legend top (730.58); the reserved clearance
reads 72px at five bars:

| label | label bottom | gap to the legend | room above the container edge |
|---|---|---|---|
| Blog Draft Writer Agent | 690.47 | 40.11 px | 63.11 px |
| Blog Idea Generator Agent | 705.32 | 25.26 px | 48.26 px |
| Blog Image Generator Agent | 713.10 | 17.48 px | 40.48 px |
| Blog Image Prompt Agent | 701.79 | 28.79 px | 51.79 px |
| Blog Pipeline Agent | 677.04 | 53.54 px | 76.54 px |

No label overlaps the legend and none is clipped by the chart container.

## Notes

- The wrench in the topbar is the app's development-only control, an artefact of
  the development boot this proof round used. It is not part of the change.
- dom-readings.jsonl is append-only: one entry per shutter, in order — four
  shutters, four frames, no re-shoot.
- The five runs each ended in a failed status; the chart counts dispatched runs,
  and each of the five carries a runtime task id, an execution attempt id and a
  trigger row of type immediate.
