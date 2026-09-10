# Upload screen and scope panel — second proof round (pull request 3323, issue 3204 leg 3)

Head under proof: 7e985ea1ec567dab6da4c4579361817a6aeeb565. Every cell was shot fresh at this head on a development boot, both palettes, through the app's own theme control. No agent run was dispatched — every cell is [no run].

The development-only wrench control in the topbar is the artefact of the development boot road; the framework's own development indicator is hidden by the framework's own means and reads zero-sized in every frame's reading (devPortalBox w=0 h=0).

| frame | cell | palette | verdict |
| --- | --- | --- | --- |
| cell1-file-tab-artifact-archive-resolved-kind-and-scope-panel-light.png | CELL1 | light | shot — resolved kind "Artifact", the install panel with the picker preselected to "Workspace: All", Cancel and "Install now" |
| cell1-file-tab-artifact-archive-resolved-kind-and-scope-panel-dark.png | CELL1 | dark | shot — same readings in the dark palette |
| cell2-github-tab-repository-resolved-pinned-commit-and-scope-panel-light.png | CELL2 | light | shot — repository resolved, pinned at fcef3294624e31eaa64e6af42a64ea8ae1f7de83, resolved kind "Skill", the same install panel |
| cell2-github-tab-repository-resolved-pinned-commit-and-scope-panel-dark.png | CELL2 | dark | shot — same readings in the dark palette |
| cell3-github-tab-precondition-no-usable-connection-submit-disabled-light.png | CELL3 | light | shot — the "no usable GitHub connection" precondition named in the copy, Submit disabled |
| cell3-github-tab-precondition-no-usable-connection-submit-disabled-dark.png | CELL3 | dark | shot — same readings in the dark palette |
| cell4-agent-in-the-agents-listing-at-the-chosen-scope-light.png | CELL4 | light | shot — the uploaded agent in the agents listing at the chosen scope |
| cell4-agent-in-the-agents-listing-at-the-chosen-scope-dark.png | CELL4 | dark | shot — same in the dark palette |
| cell4-uploaded-skill-on-the-agent-cards-own-skills-offer-light.png | CELL4 | light | shot — the uploaded skill offered on the agent card's own Skills offer |
| cell4-uploaded-skill-on-the-agent-cards-own-skills-offer-dark.png | CELL4 | dark | shot — same in the dark palette |
| cell4-artifact-packs-declared-type-offered-in-the-artifacts-type-picker-light.png | CELL4 | light | shot — the pack's declared type offered in the artifacts type picker |
| cell4-artifact-packs-declared-type-offered-in-the-artifacts-type-picker-dark.png | CELL4 | dark | shot — same in the dark palette |
| cell4-artifact-object-rendered-under-the-packs-declared-type-light.png | CELL4 | light | shot — an object of that type filed and rendered under the pack's declared type |
| cell4-artifact-object-rendered-under-the-packs-declared-type-dark.png | CELL4 | dark | shot — same in the dark palette |
| cell4-connector-configuration-surface-after-install-light.png | CELL4 | light | shot — the schema-config connector's own configuration surface after a completed install |
| cell4-connector-configuration-surface-after-install-dark.png | CELL4 | dark | shot — same in the dark palette |
| cell4-connector-without-access-scope-refused-on-the-toast-surface-light.png | CELL4 | light | shot — a connector declaring no access scope refused in one product sentence on the toast surface, the panel unchanged, no inline repeat in the file card |
| cell4-connector-without-access-scope-refused-on-the-toast-surface-dark.png | CELL4 | dark | shot — same in the dark palette |
| cell5-retired-kind-archive-refused-on-the-toast-surface-light.png | CELL5 | light | shot — an archive declaring the retired kind refused by name on the toast surface, nothing written |
| cell5-retired-kind-archive-refused-on-the-toast-surface-dark.png | CELL5 | dark | shot — same in the dark palette |

## Not shot

- CELL3, second precondition state ("no owning connector"): carved out by name. Reaching it needs the GitHub connector inactive across the instance, which would break the live connection CELL2 is shot on; no reachable organization on this boot lacks the owning connector. Not shot.

## Readings beside the frames

- `dom-readings.jsonl` — one appended reading per shutter (theme, resolved kind, resolved package, pinned commit, panel box and availability, picker text, Cancel and Install now text, precondition copy, submit disabled, dialog count, toast text and box, the required region's box, the framework indicator portal box).
- `measurements.json` — per frame: sha256, bytes, pixels, mean luminance, the required region's luminance, cell and palette.
