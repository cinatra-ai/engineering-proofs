# Proof round 1 — cinatra#3537 at faf7b03371619f3c6f4b1976830bc2521157d79a

The first picture round of the pull request that draws an installed artifact pack on the
Extensions page's installed list like every other kind. The frames were taken on a
development boot of the pushed head, through the product's own navigation:
Configuration in the left sidebar, then the Extensions page, then its status filter.

Scope of this round: the installed list's Active view and its status filter. No agent run
was dispatched; both cells are [no run].

## Frames

| file | cell | view | palette |
| --- | --- | --- | --- |
| cell1-active-json-artifact-card-light-r2.png | CELL1 | Active view, the @cinatra-ai/json-artifact card whole in the window | light |
| cell1-active-json-artifact-card-dark-r2.png | CELL1 | the same card, same scroll position | dark |
| cell2-status-all-light-top.png | CELL2 | status view All, the filter control in the window | light |
| cell2-status-active-light-top.png | CELL2 | status view Active, the filter control in the window | light |
| cell2-status-all-light.png | CELL2 | status view All, scrolled to the artifact cards | light |
| cell2-status-active-light.png | CELL2 | status view Active, scrolled to the artifact cards | light |
| cell2-status-locked-light.png | CELL2 | status view Locked, empty state | light |
| cell2-status-archived-light.png | CELL2 | status view Archived, empty state | light |
| probe-dev-indicator.png | — | throwaway probe of both bottom corners after the framework's development indicator was switched off | light |

The round's reading files (per-file hashes and luminance, one page reading per shutter, the four status views' membership, the list of artifact cards drawn) are kept with the round's working files and are not part of this published set; the readings that matter are quoted below and in the pull request's record.

## Readings taken beside the frames

The boot's own installed-extension rows, read read-only by named columns before the first
shutter: 94 active rows — 30 agent, 29 artifact, 27 connector, 8 skill. The graded package's
own row reads package name @cinatra-ai/json-artifact, kind artifact, status active,
version 0.1.0.

The Active view drew 89 installed cards, 29 of them artifact cards, @cinatra-ai/json-artifact
among them. The All view drew the same 89. The Locked and Archived views drew no cards and
their own empty states instead.

The account band is painted over in every frame. The framework's development indicator was
switched off through the framework's own route before the first shutter, and its box measured
0 by 0 at every shutter. The app's own development-only wrench control in the topbar is the
artefact of taking the round on a development boot and is not a departure of this change.

Recorded, not counted: the installed card's vendor byline carries a build-provenance suffix
beyond the drawn line, the version renders as a build-provenance string rather than the
manifest version, and the spec line sits beside it. These are pre-existing departures of the
installed list that this change does not draw.
