# Upload Extension — proof round at 48140c6572caf0bd3a5dc3be12a1016b0ada2ae3

Every frame below was taken on a development boot of this branch head, in a
1440x900 window (the two artifacts-area frames use a taller 1440x1800 window,
which is the browser walk's own window for the type picker). Both palettes were
reached through the product's own topbar theme control; no class was forced on
the document.

The framework's development indicator is hidden by the framework's own means and
proven on pixels: on every frame whose bottom-right 300x300 region is page
ground, that region reads 240.71 flat in light and 6.45 flat in dark. The
product's own "Open development tools" control in the topbar is an artefact of
running on a development boot; it is not counted against any frame.

No agent run was dispatched for any frame. Every cell is [no run], and the
instance's run table held zero rows before and after the round.

## Frames

| frame | cell | palette | verdict |
| --- | --- | --- | --- |
| cell1-file-tab-agent-archive-resolved-kind-and-scope-panel-light.png | CELL1 | light | PASS — kind Agent resolved, the install panel drawn in place with the picker preselected to Workspace: All, Cancel and Install now, no popup |
| cell1-file-tab-agent-archive-resolved-kind-and-scope-panel-dark.png | CELL1 | dark | PASS |
| cell1-file-tab-skill-archive-resolved-kind-and-scope-panel-light.png | CELL1 | light | PASS — kind Skill resolved, same panel |
| cell1-file-tab-skill-archive-resolved-kind-and-scope-panel-dark.png | CELL1 | dark | PASS |
| cell1-file-tab-connector-archive-resolved-kind-and-scope-panel-light.png | CELL1 | light | PASS — kind Connector resolved, same panel |
| cell1-file-tab-connector-archive-resolved-kind-and-scope-panel-dark.png | CELL1 | dark | PASS |
| cell1-file-tab-artifact-archive-resolved-kind-and-scope-panel-light.png | CELL1 | light | PASS — kind Artifact resolved, same panel |
| cell1-file-tab-artifact-archive-resolved-kind-and-scope-panel-dark.png | CELL1 | dark | PASS |
| cell3-github-tab-precondition-no-usable-connection-submit-disabled-light.png | CELL3 | light | PASS for the state it shows — "There is no usable GitHub connection", the copy names where to fix it, Continue disabled |
| cell3-github-tab-precondition-no-usable-connection-submit-disabled-dark.png | CELL3 | dark | PASS for the state it shows |
| cell4-agent-in-the-agents-listing-at-the-chosen-scope-light.png | CELL4 | light | PASS — the uploaded agent's own card inside the window in the agents listing |
| cell4-agent-in-the-agents-listing-at-the-chosen-scope-dark.png | CELL4 | dark | PASS |
| cell4-agents-listing-arrived-uploaded-agent-below-the-fold-light.png | CELL4 | light | the landing the screen navigates to; the uploaded card sits below the fold on this frame, so the frame is named for what it shows and the card is proven on the two frames above |
| cell4-agents-listing-arrived-uploaded-agent-below-the-fold-dark.png | CELL4 | dark | same |
| cell4-skill-in-the-skills-listing-at-the-chosen-scope-light.png | CELL4 | light | PASS — the uploaded skill listed against its own package at Workspace: All |
| cell4-skill-in-the-skills-listing-at-the-chosen-scope-dark.png | CELL4 | dark | PASS |
| cell4-artifact-pack-row-in-the-installed-extensions-list-light.png | CELL4 | light | PASS — the uploaded artifact pack's own row inside the window |
| cell4-artifact-pack-row-in-the-installed-extensions-list-dark.png | CELL4 | dark | PASS |
| cell4-artifact-packs-declared-type-offered-in-the-artifacts-type-picker-light.png | CELL4 | light | PASS — the pack's declared type is offered in the area's own type picker |
| cell4-artifact-packs-declared-type-offered-in-the-artifacts-type-picker-dark.png | CELL4 | dark | PASS |
| cell4-artifact-object-filed-under-the-packs-declared-type-light.png | CELL4 | light | PASS — an object filed under the pack's declared type, the area's own facet carrying it |
| cell4-artifact-object-filed-under-the-packs-declared-type-dark.png | CELL4 | dark | PASS |
| cell4-connector-configuration-surface-after-install-light.png | CELL4 | light | PASS — a conforming connector installed through the upload road, its own configuration surface rendering its declared field |
| cell4-connector-configuration-surface-after-install-dark.png | CELL4 | dark | PASS |
| cell4-connector-without-access-scope-refused-on-the-toast-surface-light.png | CELL4 | light | PASS — one product sentence on the toast surface, fully inside the window, the panel untouched with its selection kept, no inline repeat in the file card |
| cell4-connector-without-access-scope-refused-on-the-toast-surface-dark.png | CELL4 | dark | PASS |
| cell4-agent-extension-settings-page-no-skills-offer-light.png | CELL4 | light | FAIL — the agent's own settings page carries Permissions, Execution, Marketplace, Maintenance and Danger zone, and no Skills offer at all; the skill observable the cell names is not on this surface at this head |
| cell4-agent-extension-settings-page-no-skills-offer-dark.png | CELL4 | dark | FAIL — same |
| cell5-retired-kind-archive-refused-on-the-toast-surface-light.png | CELL5 | light | PASS — the retired kind refused by name on the toast surface, fully inside the window, nothing written, no panel drawn |
| cell5-retired-kind-archive-refused-on-the-toast-surface-dark.png | CELL5 | dark | PASS |
| c5-installed-extensions-list-status-filter-marketplace-and-upload-above-the-list-light.png | C5 (checklist item) | light | PASS — the status filter plus Marketplace and Upload sit above the installed list |
| c5-installed-extensions-list-status-filter-marketplace-and-upload-above-the-list-dark.png | C5 (checklist item) | dark | PASS |

## Not shot

* **CELL2** — the GitHub tab with a repository resolved. This instance holds no
  GitHub connection: its connection table is empty, and a connection is made by
  a person signing in through the connector's own setup page. The browser walk
  stated the skip itself rather than measuring the wrong organization. Not shot.
* **CELL3's first precondition state** ("no owning connector") — carved out by
  name: reaching it needs the GitHub connector inactive across the instance,
  and no reachable organization on this instance lacks it.
* **The skill on a card's own Skills offer** — walked and shot, and it fails:
  see the two settings-page frames above.

## Files

* `measurements.json` — per frame: sha256, bytes, pixels, mean luminance, the
  bottom-right 300x300 region luminance, the palette, and the DOM reading taken
  at the same shutter.
* `dom-readings.jsonl` — one appended reading per shutter, in shot order.
* `dom-readings-attempt1-indicator-visible.jsonl` and
  `dom-readings-attempt2-theme-not-switched.jsonl` — the readings of two earlier
  attempts whose frames were discarded rather than published: the first carried
  the framework's indicator, the second did not actually reach the dark palette.
