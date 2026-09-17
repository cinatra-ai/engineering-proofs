# Sixth proof round — the link road end to end at the proved-name head (#3204)

Two cells on the extension install tab's GitHub-link road, both shot fresh at the
candidate head 36e8aadfd0d849c4b00853c991ab58a342d1e71a on a development boot, through
the product's own navigation and the product's own theme control. No run was dispatched;
both cells are [no run].

The one fixture of this proof round: the public repository `cinatra-ai/web-research-skill`
on its default branch `main`. The bare link `https://github.com/cinatra-ai/web-research-skill`
is what is typed — no ref, no branch, no commit.

| Frame | Cell | Theme | Shows |
| --- | --- | --- | --- |
| cell4-github-tab-bare-link-resolved-install-panel-light.png | CELL4 | light | the bare link resolved into the in-card install panel; the provenance ref reads `main` |
| cell4-github-tab-bare-link-resolved-install-panel-dark.png | CELL4 | dark | the same state in the dark palette |
| cell5-installed-extensions-page-fixture-skill-card-light.png | CELL5 | light | the installed card of the fixture skill in the installed list, its provenance reading `from GitHub` and its ref line `main` |
| cell5-installed-extensions-page-fixture-skill-card-dark.png | CELL5 | dark | the same card in the dark palette |
| cell5-installed-extensions-page-row-above-the-list-light.png | CELL5 | light | the row above the installed list — the `Active` picker with `Marketplace` and `Upload` beside it |
| cell5-installed-extensions-page-row-above-the-list-dark.png | CELL5 | dark | the same row in the dark palette |

## CELL4 — the bare link resolved

The panel draws the kind badge `Skill`, the package `@cinatra-ai/web-research-skill` with
version `0.1.0`, the line
`cinatra-ai/web-research-skill pinned at 58b073bc7a2a4ac9626b07e41ecee5e3218d87a2`, and the
provenance line
`cinatra-ai/web-research-skill · main · https://codeload.github.com/cinatra-ai/web-research-skill/zip/HEAD`.
The ref reads `main`, the proved default-branch name, never the stand-in. The picker is
preselected to `Workspace: All`, with `Cancel` and `Install now` beside it, no popup, and
nothing drawn inline with the typed link kept in the field.

## CELL5 — the completed install

The in-card install action was pressed once, on the resolved panel, in the light palette.
The product carried the install through: no refusal was drawn on any surface, the panel
came to rest, and the installed list draws the card `Web Research`, kind `Skill`,
`by Unknown vendor · from GitHub`, its ref line reading `main` beside `ACTIVE`, with the
`Settings` and `More details` panels beside it. The stored row reads kind `skill`,
status `active` and a workspace-level installation; its version string reads `0.0.0` where the
resolved package reads `0.1.0` — the same stored-version departure earlier proof rounds
recorded on this surface, recorded again here and not counted anew.

The skills catalogue does not list the package: the catalogue still counts 24 skills and
carries no `web-research` row. The boot's own log names the reason, and it belongs to the
development boot rather than to the change under the lens: the package loader refuses
in-process import under `untrusted-activation-mode=deny` for a package with no trusted
install record, and the skill prefill job stopped at the first model call because this
boot's public path is closed. The installed-extensions list is CELL5's graded surface; the
catalogue is its observable and is reported as not shot green.

## The frames

Frames are whole windows at 2880x2000 (1440x1000 at twice the pixel ratio), scrolled before
the shutter and never cropped. The account band is painted over in every frame. The
framework's own development indicator was switched off through the framework's own route
before the first shutter and is absent from every frame. The wrench control in the topbar is
the development boot's own artefact and is not counted against any cell.

Two frames were discarded before their cells were judged, because each was named for a state
it did not contain: an installed-list frame whose region resolved to the whole list, and a
second whose card region did not resolve. Neither was overwritten; both were deleted and the
state was shot again under a new name with a new reading.

Measurements, per-shutter readings and the navigation trails are in `measurements.json` and
`dom-readings.jsonl`.
